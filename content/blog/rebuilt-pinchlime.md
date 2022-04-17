---
title: Pin 起來改版了！從 Wordpress 搬家到 Zola！
date: 2022-04-17
updated: 2022-04-17
draft: true
taxonomies:
  categories: 
    - Pinchlime
  tags: 
    - Wordpress
    - Zola
    - Netlify
    - Github
    - Markdown
---

![](https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/zola-banner_pOklOy.webp)

來跟大家分享以及更新一下，目前看到的這個網站「 Pin 起來 ／ Pinchlime.com 」，在今天（2022.04.17）進行了一次大改版。

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

![](https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/wordpress-com-advanced-plan_GAXFMG.webp)

對我來說，我需要的功能就是能夠產製簡單圖文排版的頁面、版型設計符合我的需求、加上讀取速度夠快就好，而 Wordpress.com 對我來說好像有點大材小用。

### 想多學一點東西，讓網站更符合自己的想像

如果說前面兩點考量是「推力」，那這個考量則是「拉力」。

我一直都對「自己架網站」這件事情很嚮往，在使用 Wordpress.com 之前，幾年前也曾經用 [SiteGround](https://www.siteground.com/) 這個託管服務自己架過 Wordpress 網站，但後來用一用覺得好難、好麻煩，就放棄了。

但幾年後的自己好像更有動力去搞懂這一切，而靜態網站看起來又是相對更簡單一點的東西，所以這樣的動力就帶著我開始嘗試搬家。

---

## 為什麼選擇使用 Zola ？

在決定要開始嘗試搬家後，我先瀏覽了一下不同靜態網站產生器（SSG）的介紹或分享心得，例如 [Jamstack - Site Generators](https://jamstack.org/generators/) 上面就有各種不同 SSG 的簡單描述與連結。

很快地我把備選的範圍鎖定在 [Hugo](https://gohugo.io/) 以及 [Zola](https://www.getzola.org/) 這兩個方案上面。原因是因為看了 [Jekyll vs Hugo vs Gatsby vs Next vs Zola vs Eleventy](https://mtm.dev/static) 這篇文章的簡單比較後，感覺 Hugo 跟 Zola 是相對更簡單上手，而且也是主打速度的方案。

另一方面也是因為，我看了推友 Owen 的 [迁移博客和Wiki到 Zola](https://www.owenyoung.com/blog/migrate-to-zola/) 後，對 Zola 的印象還不錯，而 Hugo 則是普遍看到幾乎都是好評的選秀，所以就選擇兩個都來研究看看。

研究了一兩天後，看了好幾篇比較文，決定選擇使用 Zola ，原因有兩個。

1. Zola 的官方文件更簡單一點

對我來說，[Zola 的官方文件](https://www.getzola.org/documentation/getting-started/overview/) 比 [Hugo 的官方文件](https://gohugo.io/documentation/) 架構更簡潔單純一點。我沒有學過任何的程式語言，所以這可能很偏個人的體感，但我的閱讀心得是 Zola 的文件編排好像更有序一點，Hugo 的文件則是複雜很多，架構也比較不明確，我看了一下發現「好像很複雜」，就有點不敢再繼續下去。

2. 看了別人分享的兩者比較文

因為目標明確，所以我都直接搜尋 Hugo vs Zola 之類的文，結果就找到兩篇都是從 Hugo 搬到 Zola 的分享，分別是：[Migrating to Zola - Blag](https://www.xypnox.com/blag/posts/migrating-to-zola/) 以及 [Karan Sharma | Migrating my blog to Zola](https://mrkaran.dev/posts/migrating-to-zola/) ，兩篇文都提到 Zola 相對 Hugo 更簡單一點，而且前者的文章裡面還有比對 Zola 跟 Hugo 實際上產生的網站架構，我就是看了這篇的比較後直接決定，就先選擇 Zola 用用看吧！

---

## 搬家過程做了什麼事？

決定方向後，就是開始著手進行了。

而我的進行步驟可以分成三個階段：

1. 照著 Zola 官方的 [Getting Started](https://www.getzola.org/documentation/getting-started/overview/) 文件運作一次。在這階段我除了在 mac 上面安裝了 Zola 以外，也學會使用 `zola serve` 這樣的指令，讓我可以直接在 mac 本機的瀏覽器觀看程式碼改變後的效果是什麼。

2. 直接 clone 一份 [Owen 網站的 source code](https://github.com/theowenyoung/blog) 並開始研究它每一個文件的功能是什麼。

3. 開始導入我自己之前的文章，並根據我的需求和想法，調整樣式跟功能。

第一和第二個步驟大概都各花了 1-2 個平日的晚上，但第三個步驟大概花了我整整一個禮拜進行，不過收穫也是最豐富的。

成果可以看[這張我和 Owen 部落格的對比圖](https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/owenblog-pinchlime-comparison_ruMgYD.webp) （因為檔案較大，就不壓縮預覽圖了，可以直接點開看原圖）

左圖是 Owen 的部落格，右圖是 Pin 起來，兩者在 layout 的編排上很相似，我有調整的地方在於：

- 配色、字體
- 少了左邊的 navbar ，多了首頁的 Logo ，並且[新增了最新文章欄位](/blog/added-latest-section-in-sidebar)
- 在點到內文後的側邊欄，也加上了「看更多相關文章」以及「看其他最新文章」的欄位
- 刪除了一些我暫時沒有規劃的 sections ，例如讀書筆記、短想法等等

而在這個過程中，

## 搬家後有達到原本期待的目標嗎？