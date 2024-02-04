---
title: 如何透過 Pagefind 在 Zola 產生的靜態網站裡加入搜尋功能
date: 2023-01-14
updated: 2023-01-14
description: 在經歷過多次失敗後，我想到，何不問問 ChatGPT 呢？
path: blog/how-to-add-a-search-function-to-zola-generated-static-websites-via-pagefind
taxonomies:
  categories: 
    - Tools
  tags: 
    - Pagefind
    - Zola
    - Netlify
    - Static Websites
    - Search
extra:
  image: https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/pagefind_MyUsEp.webp
---

這篇文是在一個非常滿足的狀態下寫完的。

我沒有想到，僅僅四天前我才在「為何我想為網站加上搜索功能？」這篇文裡半放棄地說：

> Pagefind 對目前的我好像還是有點太進階了。
>
> 我能夠照著它的教學，在我電腦裡的網站 directory 成功生成 index，但我不知道該怎樣把這個流程也套用到 Netlify 上面，不知道該怎麼讓網站在自動 build 的同時也可以透過 Pagefind 產生 index ，所以就暫且先放棄。

但今天卻順利把這個功能加到網站裡面了，對於我這個幾乎不會寫程式的人來說，真的是值得紀念的重大進展。

以下簡單紀錄一下，為了幫網站加上站內搜索的功能，我做了什麼、中間遇到什麼挫折，最後又是怎麼辦到的？

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/pagefind_MyUsEp.webp" data-fancybox data-caption="pagefind">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/pagefind_MyUsEp.webp" loading="lazy" alt="pagefind" align="center" />
</a>

（_圖來自 [Pagefind 官網](https://pagefind.app/)_）


<!-- more -->

---

## Pagefind 是什麼？

[Pagefind](https://pagefind.app/) 是我先前在 Twitter 上面偶然發現的網站搜索工具，它主打的是「不需要部署任何後端」，就可以運作在所有類型的靜態網站產生器上面，例如我的網站使用的 Zola ，或者是 Pagefind 介紹頁面上有提到的 Hugo, Eleventy, Jekyll, Next, Astro, SvelteKit 等等。

具體的做法是，當靜態網站產生器們生成了整個網站的靜態頁面後，Pagefind 會幫這些靜態頁面進行索引，然後再透過簡單的預設 UI 介面，讓你可以在自己的網站中，進行搜尋。詳細的介紹可以參考 Pagefind 的首頁。

當時我在看到這個工具後，就默默存了下來，並且想著總有一天要在網站中裝上這個工具。

不過第一次與第二次嘗試都失敗了，因為我不知道該怎樣達成：

* 先在 Netlify 裡面先 build 網站
* 再安裝 Pagefind 進行索引
* 再 deploy 整個網站

---

## 我卡關的地方

我原先的網站更新步驟是：

1. 先在自己的主機編輯 markdown 文件，完成後 commit 並 push 到固定的 Github repo 裡。

2. 設定 Netlify 會自動偵測這個 repo 的更新狀況，假設有新的 commit ，就會觸發預設的 `zola build` 指令，然後就會在 Netlify 的主機裡執行「build」的任務，產出整個網站的所有靜態頁面。

3. 產出所有靜態頁面後，Netlify 會再幫我把這些頁面部署上線，就可以透過瀏覽器正常瀏覽。

以我對 Pagefind 的初步理解，我必須要在第二步驟結束後，想辦法在 Netlify 的主機裡，也下載並執行 Pagefind ，然後執行 Pagefind 裡面的指令，讓他能夠順利找到第二步驟剛 build 完的所有頁面，並且順利產出 indexes ，再讓 Netlify 去 deploy 所有內容。

但我在這邊卡了好久，卡關的核心原因並不是「指令無法生效」，而是我不知道該下什麼指令、該從哪邊、該怎樣去設定。

我嘗試著想透過 Netlify 的後台設定、也嘗試了使用 Netlify 的 [File-based configuration](https://docs.netlify.com/configure-builds/file-based-configuration/) ，試圖找出，該在哪個地方填寫 Pagefind 的相關指令，但都失敗，失敗失敗失敗。

就在快放棄時，推友 [pseudoyu](https://twitter.com/pseudo_yu) 留言給我，分享給我他透過 Github actions ，在 Hugo 產出的靜態網站實作 Pagefind 的方式：可參考[這個 yml 檔案](https://github.com/pseudoyu/yu-blog/blob/master/.github/workflows/deploy.yml)的第 62 & 63 行：

```
name: Run Pagefind
run: npm_config_yes=true npx pagefind --source "public"
```

由於有現成的 code 可以參考，於是我開始走另一條路，嘗試把我的整個 build \+ deploy 的流成，改透過 Github actions & Github pages 來進行。

不過我仍然失敗了，失敗的原因我自己理解是因為，Zola 既有的 Github 部署指令裡面，build 跟 deploy 是合併在一起的，我不知道該怎樣講他們拆開，所以自然也就沒辦法在中間加入 Pagefind 的指令。

---

## 我最後怎麼成功的？

在 Github actions 這條路也失敗後，我原本想放棄了，但還是想說再多亂試個不同做法看看，就這樣試了好多種，我嘗試在 Netlify 裡面設定 plugins ，想說可不可以把 Pagefind 當成 plugin，然後順利運作，結果花了幾個小時，還是失敗。

最後我想到，何不問問 ChatGPT 呢？

於是我問他下列內容：
<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/ask-chatgpt-how-to-edit-netlify-toml_sfSs5D.webp" data-fancybox data-caption="ask-chatgpt-how-to-edit-netlify-toml">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/ask-chatgpt-how-to-edit-netlify-toml_sfSs5D.webp" loading="lazy" alt="ask-chatgpt-how-to-edit-netlify-toml" align="center" />
</a>


結果他回我：
<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/chatgpt-answered-how-to-edit-netlify-toml_gtmRXN.webp" data-fancybox data-caption="chatgpt-answered-how-to-edit-netlify-toml">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/chatgpt-answered-how-to-edit-netlify-toml_gtmRXN.webp" loading="lazy" alt="chatgpt-answered-how-to-edit-netlify-toml" align="center" />
</a>

意思是，在 build 的指令那邊，可以透過 && ，把兩個指令連結在一起執行，這樣就可以達到我想要的「先 build zola，再 index，再 deploy 」的效果。



我照著做以後，真的就成功了，跑了十幾二十次失敗的 Netlify ，終於成功地 index 我的所有靜態網頁們。如下圖紅框內的內容。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/netlify-deploy-log-230114_dUOrSs.webp" data-fancybox data-caption="netlify-deploy-log-230114">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/netlify-deploy-log-230114_dUOrSs.webp" loading="lazy" alt="netlify-deploy-log-230114" align="center" />
</a>

而在確定可以順利 deploy 後，後續要做的事情就簡單很多了，只要照著 Pagefind 上面的教學，把對應的 prebuilt UI 相關程式碼放到網頁上，並且再額外設定一些內容，就順利完成了。

---

## 具體的設定與執行步驟

在這邊也分享一下我的作法，由於使用 Zola 的應該是極小眾，而大家可能分別用不同的方式部署，也未必是透過 Netlify ，因此這部分的步驟就僅供參考，但以我的理解，不同的靜態網站產生器跟不同的部署流程的概念應該都是近似的！


步驟如下：

* 在網站的根資料夾中，設置 netlify.toml 檔案，這個檔案的用途是讓 Netlify 知道，他在 build & deploy 你的網站中，該使用哪些指令、該怎麼設定變數等等。我在這之前都是使用 Netlify 的後台設定，並沒有使用 netlify.toml ，所以這也是第一次轉向採用這個方式。

* 在 netlify.toml 檔案裡面，設定 \[build\] 的相關內容，以我來說是：

```
[build]
    publish = "public/"
    command = "zola build && npx pagefind --source public"

    [build.environment]
         ZOLA_VERSION = "0.16.0"
```

這段程式碼的意思是：

* publish：指定「build」指令產生的內容要放在哪個路徑，我這邊設定的是「public」。

* command：指定我的「build」指令是 `zola build` ，並且透過 && ，連結另一個執行 Pagefind 的指令 `npx pagefind --source public`，關於 Pagefind 的指令可以參考：[Installing and running Pagefind](https://pagefind.app/docs/installation/) 頁面的內容。

* build.environment ：指定我要採用的 Zola 版本，由於我在自己電腦上執行的是 0.16.0 ，所以我就請它也選擇 0.16.0 。

假設一切順利，那麼在 Netlify build 完的網站，就已經會有 Pagefind index 過的檔案了。

而確認沒問題後，接著是在自己的頁面裡面，找個地方放置 Pagefind 的 “[Pagefind UI](https://pagefind.app/docs/ui/)” 相關內容。

這個指的是，Pagefind 已經提供了一套預設的程式碼，只要放入你想要秀出那個搜尋框框的網頁段落，他就可以在那個地方直接運作 Pagefind 的搜尋功能。

我的作法是，在網站裡面新增一個 search.html 獨立頁面，然後把這段程式碼放進來，再加入一些補充說明跟超連結設定，最終的結果就會像是「[Search](/search)」這個頁面這樣了，歡迎大家嘗試搜尋看看。

除了安裝好基本款以外，Pagefind 也提供了一些進階的設定，還有過濾與篩選的功能，這部分等我再研究一陣子，再來分享！

---

## 最終的搜尋效果

全部都處理好後，最終的搜尋效果我還蠻滿意的，可以看到下面的 gif 示意，他的搜尋非常即時，例如我搜尋 pagefind 時，會根據我輸的的字數從 pa → page → pagefind 而產出不同的搜尋結果。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/pagefind-demo_hkBkdd.gif" data-fancybox data-caption="pagefind-demo">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/pagefind-demo_hkBkdd.gif" loading="lazy" alt="pagefind-demo" align="center" />
</a>

不過目前對於中文的支持度稍微差了一些，需要自己強制斷詞，才比較可以搜到想要的結果，但我覺得也很堪用了！

以上分享，如果能幫到大家就太好了，若有遇到任何問題，我不一定能幫忙解決，但很樂意與你一起討論！（建議可以先找 chatGPT 問問。）