---
title: 我為什麼又想用 Docusaurus 架一個子網站？
date: 2023-02-11
description: Docusaurus 看起來直接用「預設基本款」就能達到這種雙欄式的文檔瀏覽介面，完全打中我的需求。
path: snapshots/why/why-do-i-want-to-build-another-website-by-docusaurus
taxonomies:
  categories:
    - Tools
  tags: 
    - Docusaurus
    - Static Websites
    - Zola
    - SEO
extra:
  image: https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/docusaurus-social-card_WKa2xI.jpg
---

前幾天發現 [Docusaurus](https://docusaurus.io/) 這個似乎是由 Meta (Facebook) 推出的靜態網站產生工具後就很喜歡，中間有思考了一下我真的要這樣做嗎？

最終還是決定：要。

這篇簡單記錄一下原因以及心得。

<!-- more -->
---

### Docusaurus 給我的好印象

由於有使用過 [Zola](https://www.getzola.org/) ，也非常喜歡，所以原本都不太研究其他靜態網站產生器了，但前陣子看到 [Astro](https://astro.build/) 這個工具後有點心動（這邊先略過不提），而這幾天看到 Docusaurus 後，更是燃起一股想嘗試的衝動。

原因有三個：

**一、Docusaurus 主打的雙欄式 “Docs” 架構是我一直想要的網站呈現方式**

我一直都很喜歡 [Brian Lovin 的個人網站](https://brianlovin.com/) ，尤其是網站裡的 “ Stack “ 頁面，可以列出不同的工具，然後再一個一個介紹，而使用者在瀏覽時不會一直跳轉分頁，可以快速查閱瀏覽，我覺得這樣的體驗很棒。

但我在 Zola 系統底下，好像沒辦法做出這樣的網站，一方面可能是 Zola 本身就沒有提供這樣的功能，另一方面是我的前端能力也還非常不足，連怎麼「開始」都沒有頭緒。

而 Docusaurus 看起來直接用「預設基本款」就能達到這種雙欄式的文檔瀏覽介面，完全打中我的需求。

**二、Docusaurus 看起來非常好上手**

我看了一下 Docusaurus 的官方文件，整個網站的架構很單純、要設定的東西也沒有很多，而且官方文件寫得非常清楚好懂。有了 Zola 經驗的我，覺得 Docusaurus 甚至好像更簡單。

**三、Docusaurus 看起來很友善 SEO**

我一直都蠻在意網站的 SEO ，因為我喜歡我自己寫的內容，也會因為讀者喜歡我的內容而感到開心，而除了 Twitter 以外，搜尋仍是目前我網站的重要流量來源，因此我會希望我寫的內容最好都是「搜尋引擎友善」的。

就我理解，靜態網站大多都很友善 SEO ，而 Docusaurus 還有[一個頁面在談 SEO](https://docusaurus.io/docs/seo) ，另外我隨便測試了幾頁 Docusaurus 的頁面，搜尋跟 Lighthouse 跑分的表現都很不錯，因此我覺得 SEO 這關好像可以過關。

（去年五、六月在架自己的個人 wiki 時，我曾用 Logseq 以及 Dendron 這兩個筆記工具的 Publish 功能建立網站，但他們的 SEO 表現都不太好，因此我當時最終還是選擇[用熟悉的 Zola 建立子網站](@/blog/built-pinchlime-notes.md)。）

總之， Docusaurus 看起來是個值得嘗試的工具，因此從昨晚開始，我就直接開始架了。

---

### 我想拿這個子網站放什麼？

由於我 1 月才剛把前一個「筆記與想法快照」的子網站搬回主網站，我這幾天也在思考，我真的有必要建立一個子網站嗎？它跟筆記與想法，或者說現在的「[Snapshots](/snapshots/) 頁面們」又有什麼不同？

想了想，我覺得性質還是不太一樣。

當時的筆記與想法子網站，是為了解決那時的我「無法持續輸出內容」的問題而建立的嘗試性專案，後來這個問題真的順利解決了，透過 Snapshots 這種「略少於一篇 blog 文章，略長於一串推文串」的內容形式，我開始可以大量紀錄與分享自己的想法。

不過，有一部分的內容我仍然找不太到地方放：**我收集的各種東西們**。

例如，我有在使用的工具、我有訂閱的服務、我看過的書、我精選的文章，這類比較像是「列表」的東西，我一直覺得不太知道該怎麼放在 Pin 起來網站上。

假設每個列表都用一個頁面處理，那列表裡的東西，又該怎麼開設？該怎麼分類與整理？我有需要幫每個我在用的產品都建立一個頁面嗎？若要，好像會太瑣碎，若不要，又會讓各種整理「我在用的產品」的文章變得太長，很難閱讀。

總之，每次想到這個問題，我都想不太到好解方，因此我先前有建立的工具箱頁面也好一陣子沒有維護，而有許多放在 inbox 裡面的內容也找不到地方放。

但看到 Docusaurus 以後，我感覺這個問題有解了。

Docusaurus 的介面很適合處理這種列表類型的頁面，例如 [PJCHENder 未整理筆記](https://pjchender.dev/) 就是我看了以後非常欣賞的 Docusaurus 範例，裡面透過側邊欄放置了各種語法或主題的筆記內容。昨天就是看到這個網站後我就決定，好，我要開始做了。

而簡單規劃後，這個新的網站在定位上，不會與之前的「筆記與想法」網站衝突，因為它不會放各種零散的想法，它只會放各種零散的「items」，例如各種產品、服務、文章，並且在這些 items 上面，放置我在 Pin 起來網站上面相關的文章，作為導連的用途。

---

### Docusaurus 真的很容易使用

在開始架站後，一切都非常順利，我只用了一兩個小時，就把這個新的子網站架好並上線了，後續就再慢慢把我想放的內容放上去就好。（可能要花幾個禮拜）

雖然我還有很多功能都沒有用，但只用基本功能就已能達到我八九成想做的事情，整個體驗非常好。

整個體驗再次證明，對我來說，使用趁手的工具去做想做的事，真的是非常有滿足感的事。

PS. Docusaurus 的吉祥物恐龍真的很可愛！

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/docusaurus-social-card_WKa2xI.jpg" data-fancybox data-caption="docusaurus-social-card">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/docusaurus-social-card_WKa2xI.jpg" loading="lazy" alt="docusaurus-social-card" align="center" />
</a>