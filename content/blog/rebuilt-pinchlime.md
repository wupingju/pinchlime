---
title: Pin 起來改版了！從 Wordpress 搬家到 Zola！
date: 2022-04-17
updated: 2022-04-17
description: 當我之前知道有「靜態網站產生器」（Static Site Generator）這種可以直接把 markdown 文件渲染成網站的東西存在後，我心中就一直想著，總有一天一定要用用看。
path: blog/rebuilt-pinchlime
taxonomies:
  categories: 
    - Pinchlime
  tags: 
    - Wordpress
    - Zola
    - Netlify
    - Github
    - Markdown
    - Static Sites
---

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/zola-banner_pOklOy.webp" data-fancybox data-caption="zola-banner">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/zola-banner_pOklOy.webp" loading="lazy" alt="zola-banner" align="center" />
</a>

來跟大家分享以及更新一下，目前看到的這個網站「Pin 起來／Pinchlime.com」，在今天（2022.04.17）進行了一次大改版。

改版前，這個網站是透過 [Wordpress.com](https://wordpress.com/) 運作的，包含網域的託管，以及內容的管理與撰寫，都是在 Wordpress.com 上面進行。

改版後，這個網站的運作則切成了幾個不同的部分：

- 網站內容的撰寫：透過 markdown 文件進行
- 網站的生成：透過 [Zola](https://www.getzola.org/) 這個靜態網站產生器，將 markdown 文件轉成 html 檔案。
- 網站的部署：將不同頁面的 html 檔案，透過 [Netlify](https://www.netlify.com/) 這個讓人託管網站的網站來部署。
- 各部分的串接：透過 Github 來進行。

為何我要把原本看起來單純的「Wordpress.com 一站式託管」變成這麼複雜的流程？

<!-- more -->

---

## 為何想從 Wordpress.com 搬走？

在大約十天前，我在自己的推特上面寫了[一則推文](https://twitter.com/WuPingJu/status/1511741213141086211)，有提到為什麼想從 Wordpress.com 搬走，主要有三個原因：

> 1. 速度，包含人或非人讀取網站的速度，以及我產出到編輯完成一篇文章的速度。
> 2. 價錢，我想找更經濟實惠的選項。
> 3. 想藉由這個機會學更多一點東西、讓網站更符合自己的想像。

推特講的比較簡單，這邊再補充地更完整一點：

### 讀取與寫作速度的考量

在速度方面，可以分成讀取網站的速度，以及寫作的速度兩點來談，對於原先的 Wordpress.com 方案，這兩項我都不是特別滿意。

讀取速度方面，雖然自己在讀的時候沒有特別感覺慢，但透過 Google 的 [PageSpeed Insights](https://pagespeed.web.dev/) 測出來的結果，通常 Mobile 是 60-70 分左右，而 Desktop 則是 90 分左右，雖然稱不上太差，但總覺得應該還可以更好吧。可是每當我往下看 Google 的建議時，就發現有些東西我很難處理，因為既有的網站是直接用 Wordpress.com 上面別人開發的主題，我也不知道怎麼改起。

而寫作速度的考量更是我在意的重點，原先我在 Wordpress.com 上面產出文章的流程是：

1. 先在自己的電腦上透過 Drafts 以及 iA Writer 這兩個軟體，撰寫與編輯 markdown 文件。
2. 寫好後，透過 iA Writer 的 preview 功能，產出渲染後的 html 格式文字，再把它們複製並貼到 Wordpress 的編輯器裡。
3. 接著，再透過 Wordpress 的編輯器微調文字排版、段落，並且設定網址 slug 或是頁面描述等。最後再發布出去到網路上。

通常流程 1 的部分對我來講都是快樂的，但是 2 跟 3 對我來說就是單純花時間的繁瑣程序，每次 PO 文大概就要花 15-30 分鐘在這上面，所以當我之前知道有「靜態網站產生器」（Static Site Generator）這種可以直接把 markdown 文件渲染成網站的東西存在後，我心中就一直想著，總有一天一定要用用看。

### 價錢的考量

原先我在 Wordpress.com 上面選用的是「進階版方案」，以年計費的話，每個月是新台幣 240 元，一年則是 2,880 元，但坦白說，這個方案裡面諸多功能我幾乎都用不到。如下圖，像是進階設計工具、儲存音訊跟影片檔案的空間，或者是透過網站廣告獲利等等，還有電子郵件支援、使用 Paypal 支付或 Jetpack 等功能，我全部都用不到。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/wordpress-com-advanced-plan_GAXFMG.webp" data-fancybox data-caption="wordpress-com-advanced-plan">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/wordpress-com-advanced-plan_GAXFMG.webp" loading="lazy" alt="wordpress-com-advanced-plan" align="center" />
</a>

對我來說，我需要的功能就是能夠產製簡單圖文排版的頁面、版型設計符合我的需求、加上讀取速度夠快就好，而 Wordpress.com 對我來說好像有點大材小用。

### 想多學一點東西，讓網站更符合自己的想像

如果說前面兩點考量是「推力」，那這個考量則是「拉力」。

我一直都對「自己架網站」這件事情很嚮往，在使用 Wordpress.com 之前，幾年前也曾經用 [SiteGround](https://www.siteground.com/) 這個託管服務自己架過 Wordpress 網站，但後來用一用覺得好難、好麻煩，就放棄了。

但幾年後的自己好像更有動力去搞懂這一切，而靜態網站看起來又是相對更簡單一點的東西，所以這樣的動力就帶著我開始嘗試搬家。

---

## 為什麼選擇使用 Zola ？

在決定要開始嘗試搬家後，我先瀏覽了一下不同靜態網站產生器（SSG）的介紹或分享心得，例如 [Jamstack - Site Generators](https://jamstack.org/generators/) 上面就有各種不同 SSG 的簡單描述與連結。

很快地我把備選的範圍鎖定在 [Hugo](https://gohugo.io/) 以及 [Zola](https://www.getzola.org/) 這兩個方案上面。原因是因為看了 [Jekyll vs Hugo vs Gatsby vs Next vs Zola vs Eleventy](https://mtm.dev/static) 這篇文章的簡單比較後，感覺 Hugo 跟 Zola 是相對更簡單上手，而且也是主打速度的方案。

另一方面也是因為，我看了推友 Owen 的 [迁移博客和Wiki到 Zola](https://www.owenyoung.com/blog/migrate-to-zola/) 後，對 Zola 的印象還不錯，而 Hugo 則是普遍看到幾乎都是好評的選項，所以就選擇兩個都來研究看看。

研究了一兩天後，看了好幾篇比較文，決定選擇使用 Zola ，原因有兩個。

1. Zola 的官方文件更簡單一點

對我來說，[Zola 的官方文件](https://www.getzola.org/documentation/getting-started/overview/) 比 [Hugo 的官方文件](https://gohugo.io/documentation/) 架構更簡潔單純一點。我沒有學過任何的程式語言，所以這可能很偏個人的體感，但我的閱讀心得是 Zola 的文件編排好像更有序一點，Hugo 的文件則是複雜很多，架構也比較不明確，我看了一下發現「好像很複雜」，就有點不敢再繼續下去。

2. 看了別人分享的兩者比較文

因為目標明確，所以我都直接搜尋 Hugo vs Zola 之類的文，結果就找到兩篇都是從 Hugo 搬到 Zola 的分享，分別是：[Migrating to Zola - Blag](https://www.xypnox.com/blag/posts/migrating-to-zola/) 以及 [Karan Sharma | Migrating my blog to Zola](https://mrkaran.dev/posts/migrating-to-zola/) ，兩篇文都提到 Zola 相對 Hugo 更簡單一點，而且前者的文章裡面還有比對 Zola 跟 Hugo 實際上產生的網站架構，我就是看了這篇的比較後直接決定，就先選擇 Zola 用用看吧！

---

## 搬家過程中做了什麼事？

決定方向後，就是開始著手進行了。

而我的進行步驟可以分成三個階段：

1. 照著 Zola 官方的 [Getting Started](https://www.getzola.org/documentation/getting-started/overview/) 文件運作一次。在這階段我除了在 mac 上面安裝了 Zola 以外，也學會使用 `zola serve` 這樣的指令，讓我可以直接在 mac 本機的瀏覽器觀看程式碼改變後的效果是什麼。

2. 直接 clone 一份 [Owen 網站的 source code](https://github.com/theowenyoung/blog) 並開始研究它每一個文件的功能是什麼。

3. 開始導入我自己之前的文章，並根據我的需求和想法，調整樣式跟功能。

第一和第二個步驟大概都各花了 1-2 個平日的晚上，但第三個步驟大概花了我整整一個禮拜進行，不過收穫也是最豐富的。

成果可以看[這張我和 Owen 部落格的對比圖](https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/owenblog-pinchlime-comparison_ruMgYD.webp) （因為檔案較大，就不壓縮預覽圖了，可以直接點開看原圖）

左圖是 Owen 的部落格，右圖是 Pin 起來，兩者在 layout 的編排上很相似，我有調整的地方在於：

- 配色、字體
- 少了左邊的 navbar ，多了首頁的 Logo ，並且新增了最新文章欄位
- 在點到內文後的側邊欄，也加上了「看更多相關文章」以及「看其他最新文章」的欄位
- 刪除了一些我暫時沒有規劃的 sections ，例如讀書筆記、短想法等等

而在這個過程中，除了更了解 Zola 的各種語法與功能，也順帶熟悉了一些 html 及 css 語法，整個過程很有趣，真的有種在「建造自己的網站」的感覺。

在 Zola 以及網站程式碼這邊搞定後，還有「部署」相關的事情需要處理跟學習，好在現在 2022 年了，有許多非常方便又實惠的選項。

---

## 透過 Netlify 自動部署網站

### 在 Vercel 跟 Cloudflare Pages 都部署失敗

在這邊簡單講一下「部署」的意思。

我在前面的流程裡面花最多時間修改調整的是「網站的程式碼文件們」，裡面包含了能影響網站外觀的 css 樣式文件、還有在 Zola 的系統裡面，規範每個頁面會有哪些東西的「templates 文件」（關於 Zola 的教學以後再說）。

而這些文件全部準備好以後，只要在任何資料夾裡面執行 Zola 預設的 ```zola build``` 指令，就會在幾秒內產生可以瀏覽整個網站的 html 檔案們。但這些檔案如果要讓大家透過 https://pinchlime.com 就可以連上的話，則必須要把它們放到網路上，這時就得要透過一些專門幫人「部署」網頁的服務來進行了。

在 Zola 的[官方文件](https://www.getzola.org/documentation/getting-started/overview/) 中，有提供 7 種部署服務的教學，包含 Sourcehut Pages, Netlify, GitHub Pages, GitLab Pages, Layer0, Vercel, Cloudflare Pages 等選項。一開始我也是每個都點開來看看，看哪一個感覺比較簡單，於是就選中了 Vercel 以及 Cloudflare Pages 這兩個選擇。他們看起來都非常簡單，只要註冊好帳號，串連 Github 的倉庫，再選擇用 Zola 架設，就可以順利完成。

但實際測試以後卻發現，這兩個服務目前（2022.04.17）都不太適合用來部署 Zola ，因為他們伺服器安裝的 Zola 版本是 0.13.0 ，但目前 Zola 已經是 0.15.3 的版本了，中間差了好幾代，我的 source codes 好像沒辦法順利安裝在舊版本的 Zola 上面。而即使這兩個服務都可以選擇下載比較新的 Zola 版本，但也還是無法順利安裝，可能 Zola 目前還是太小眾了一些，所以沒有更新地很快吧。

在這邊花了一些時間後，我選上了另一個服務 [Netlify](https://www.netlify.com/) ，這次則是非常非常的順利。

### 透過 Netlify 部署的流程

簡單來說我只做了下面這些事，就順利部署完成了：

1. 註冊 Netlify 帳號
2. 連上我存放 Zola 相關檔案的 Github 帳號以及 repository（程式碼倉庫）
3. 選擇一下要用 Zola 部署這些檔案，並且更改一下 build command 為： zola build
4. 設定一下 Environment variables，新增 ```ZOLA_VERSION``` 並將 value 設定為目前的版本 0.15.3

一切都設定好後，按下 deploy ，就順利生成網站了，此時 Netlify 還會直接配給你一個網址，會是「你選的名字.netlify.app」，這個網址就已經是公布在網路上的，所以可以隨時去查看「正式版」的網站樣子。

而 Netlify 最棒的地方在於，他有自動化部署的功能。因為他串接的是 Github 的倉庫，所以每當我的 Github 程式碼更新時，Netlify 就會自動把新的程式碼重新部署到網路上，因此我也不需要一直跑來 Netlify 手動「更新」，而只要專心處理好我要編輯的文字，然後把它們「push」到 Github 裡面就好。

### 最後一步：移轉網域並重新設定 DNS

在所有檔案都處理好，文章也移轉完成後，我就把 pinchlime.com 這個網域從 Wordpress.com 轉移到了 Google Domains，並且透過一樣非常簡單快速的 Netlify 教學，把這個網域指向了 Netlify 的伺服器。

意思是，在我移轉網域並重新設定 DNS 後，當任何人連結到 pinchlime.com 時，網域的託管商 Google 會跟他說：「Pinchlime.com 搬家了，接下來你要到 Netlify 那邊去找他喔」，然後到了 Netlify 之後，Netlify 則會把我透過自動部署產生的那些 html 檔案們，呈現在大家的面前。

至於 Wordpress.com ，就掰掰啦！（可惜已經先預付費用到 2023 年 1 月了。）

---

## 搬家後有達到原本期待的目標嗎？

回到文章開頭講的搬家想要達成的三個目標：

> 1. 速度，包含人或非人讀取網站的速度，以及我產出到編輯完成一篇文章的速度。
> 2. 價錢，我想找更經濟實惠的選項。
> 3. 想藉由這個機會學更多一點東西、讓網站更符合自己的想像。

現在可以說全部都達到了。

### 讀取與寫作速度的變化

在讀取速度方面，目前的網站透過 [PageSpeed Insights](https://pagespeed.web.dev/) 測出來的結果（如下圖），手機版大概可以在 95 分左右，而桌面版則是 99 或 100 分，跟原本的分數比起來，我已經很滿意了！ 

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/pinchlime-pagespeed-new_3fWdIE.webp" data-fancybox data-caption="pinchlime-pagespeed-new">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/pinchlime-pagespeed-new_3fWdIE.webp" loading="lazy" alt="pinchlime-pagespeed-new" align="center" />
</a>

而在寫作速度方面，原本要在 Wordpress 編輯器上面多花的 15-30 分鐘，現在也不需要了，比方說我目前這篇文章寫完後，只要在 VSCode 編輯器裡面按下 commit + sync ，就會自動把文章同步到 Github ，也就是同步到 Netlify 裡面，然後大約在 30 秒後，就可以在網站上面看到了。

### 價錢的變化

在價錢方面，原先 Wordpress.com 的進階版方案費用是一年 2,880 元，現在透過 Zola + Github + Netlify 的費用是： 0 元！

因為靜態網站的檔案實在太小，目前我整包檔案包含 logo 圖檔在內，只有 11.4 MB 而已，這些空間與流量可以說微不足道，所以 Github 與 Netlify 的免費方案都綽綽有餘。

### 我多學會了什麼？

這一點可以說是最大的收穫，我總覺得透過這十多天密集的研究、設定、處理、創造（沒錯，我也創造了好一些東西，之後再來分享），我自己在能力與知識上也成長了不少，雖然對熟悉前端語法的人來說靜態網站這些東西可能根本就沒什麼，但自己照著文件研究，並實際完成一個網站，真的是非常有成就感的一件事。

期待未來能在這個精心打造的環境裡，產出更多文字，分享給大家！