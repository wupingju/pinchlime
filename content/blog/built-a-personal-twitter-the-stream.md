---
title: 建了一個迷你版的個人 Twitter ： Stream
date: 2023-02-25
updated: 2023-02-25
description: 我感覺這個 Stream 是更接近「私人 murmur」的呈現形式。例如，我就只是單純看到某個有趣的產品，但連體驗都還沒體驗、我看到某一句很棒的文字，想要摘要下來，或者有些真的很短，頂多兩三句而已，但又不是那麼想在 Twitter 分享的想法。
path: blog/built-a-personal-twitter-the-stream
taxonomies:
  categories: 
    - Pinchlime
  tags: 
    - the Stream
    - Shortcode
    - Twitter
    - Zola
extra:
  image: https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/my-stream_cM7m3M.webp
---

> 2025.01.05 更新：我決定先關閉我的 Stream 頁面。


---

這幾天下班後都在做一件事：建立我自己的迷你版 Twitter ： [Stream](/stream/2023)，昨晚初步搞定了，來介紹分享一下。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/my-stream_cM7m3M.webp" data-fancybox data-caption="my-stream">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/my-stream_cM7m3M.webp" loading="lazy" alt="my-stream" align="center" />
</a>
<br>
<!-- more -->
---

### 這個 Stream 是什麼？

週二跟朋友聊到 Linus Lee 的 [thesephist 網站](https://thesephist.com/) ，也藉此重新瀏覽了一遍，發現站上有個之前沒特別留意到的 [stream](https://stream.thesephist.com/) 連結，點下去以後發現這好酷，我想要！

它是 Linus 自己用自己寫的程式語言 [Oak](https://oaklang.org/) 建立的頁面，概念上有點類似一個更不吵雜、更個人版本的 twitter 頁面。

Linus 在 [About 頁面](https://stream.thesephist.com/about/)有提到：

* 在 Twitter 上面有其他人在跟「自己想說的話」爭奪注意力
* Twitter 的表現方式很有限。
* Twitter 很適合作為一個「當下」的公共討論場合，但不是一個很適合從未來連結回來的參考依據。

結論是，Linus 想要一個更專門、更專注、更永久的地方，來放這些個人的想法更新。

我看了以後，不管是這個想法，或者是 Linus 的呈現方式，我都很喜歡，而且我也想到另一個朋友 Owen 在他的網站上也有類似的[短想法頁面](https://www.owenyoung.com/thoughts/)。我大概一兩個月會點進去看一次這個頁面，每次都很喜歡裡面這些零散、但不隨便的短想法。

有這兩個我喜歡的範例，我就開始思考，我有沒有機會也弄一個類似的東西。

---

### 它跟原本的 Snapshots 有什麼不一樣？

我首先思考的是，我有需要弄一個這樣的東西嗎？

我的網站上，已經有一個專屬於「短想法」的 Snapshots 頁面，假設要弄個 Stream ，會不會疊床架屋？或者增加我未來在 PO 文前的選擇困擾？

我思考後覺得，這個 Stream 跟 Snapshots 有幾個不一樣的地方：

1. 我想要的 Stream 是一整個頁面的短想法匯集，不是一則又一則的短文章連結。假設這些短想法也弄成一篇一篇的文章，可能會讓整個網站充滿太多字數過少的內容，感覺對 SEO 不太好。同時也會增加我的網站 Repo 的臃腫度，畢竟在目前這個網站上每篇內容就是一個 .md 文件。

2. 我感覺這個 Stream 是更接近「私人 murmur」的呈現形式。在我自己的設定裡，Snapshots 相關頁面雖然內容較短，但還是會想要在社群分享這樣的內容。但仍有一些東西沒那麼適合分享在 Snapshots 。
   - 例如，我就只是單純看到某個有趣的產品，但連體驗都還沒體驗。
   - 例如，我看到某一句很棒的文字，想要摘要下來。
   - 例如，有些真的很短，頂多兩三句而已，但又不是那麼想在 Twitter 分享的想法。

    Stream 這樣的形式感覺能夠承接這些極短的零散想法與紀錄。

3. Snapshots 還是有一些分類跟標籤，但 Stream 的內容我完全不打算分類或上標籤。



在思考完這些差異後，我就開始嘗試實作了。

---

### 我是怎麼建立這個頁面的？



雖然我很喜歡 Linus 的頁面，但我暫時沒有能力跟動機去研究或複製他的做法，因此我想的是如何在既有的網站上製作出類似的樣式與功能。

我想到的是之前曾經在「[完成了站內的 Glossary 個人詞庫 v1 版本](@/blog/completed-the-v1-version-of-my-personal-glossary.md)」這篇裡面有用過的 Shortcode 。



Shortcode 是 [Zola 裡面有的一個功能](https://www.getzola.org/documentation/content/shortcodes/)，可以讓使用者在 markdown 文件裡面插入一些預先定義好的比較複雜的 html 語法，或者是直接讀取資料。我這邊主要使用的是前者。



我最喜歡 Linus 的 Stream 頁面的地方是乾淨簡單，左邊放日期與時間，右邊放想法。於是我就嘗試用 Shortcode 做做看，中間嘗試與調整的過程先不提，做出來的結果大概是長這樣：

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/a-stream_NtjujP.webp" data-fancybox data-caption="a-stream">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/a-stream_NtjujP.webp" loading="lazy" alt="a-stream" align="center" />
</a>

每一則 stream 會分成三個部分：

1. 時間
2. 編號（與連結）
3. 內容

我最喜歡的應該是那個編號與連結的功能。由於我不想要每則 Stream 都有一個單獨的頁面，所以原本還有點煩惱該怎麼在未來引用回來。但後來發現好像可以設置 ID ，因此每一則 stream 就多了一個獨特的定位錨點，可以在未來連結引用。

一切設定好之後，我未來只要在同一篇 .md 文件中，插入像是下面這樣的 shortcode ，就會自動產生一則 stream 的內容：

```rust
{% fleet(num="5",time="Feb 25 00:39",year="2023") %-}
用了兩天多零碎的時間，總算差不多把這個頁面都調整成我想要的樣子了。<br>
目前的感覺是，有一個這樣子可以 murmur 的地方非常讚，它比站上的 Snapshots 更輕便、更私密一些，也因此更能構承載一些零散、破碎的內容，無論是單純放一個連結，或者是丟一段 quote 之類的，都很適合。<br>有一個能夠自由增添內容的網站真的好棒！
{% end %}
```


這裡面的 fleet 是這個 shortcode 的名稱，num 是編號， time 是會呈現在左方的時間，year 是這則 stream 的年份（未來我打算一年更換一篇），然後中間的就是完整的內容。

---

### 一些小小的缺點

實際試過以後，我這樣的實作方式還是有不少缺點：

1. Shortcode 的能力有侷限，比方說我試過以後，好像沒辦法變換「一般段落」或者是「quote」段落，所以我就得要分別設置兩個 shortcodes 。

2. 在 Shortcode 裡面編輯都得要用 html 編輯，所以像是換行或者是超連結這種就要自己寫。

3. 每新增一個 stream ，就要 key 一些變數，像是編號、時間、年份之類的。



不過第三點對我來說不是什麼問題，很容易就可以透過 Keyboard Maestro 簡化輸入的步驟。



另外，我也不確定當內容累積得越來越多（上百則、甚至上千則）時，會不會因為 shortcode 要讀太多次，而拖累了整個網站 build 的速度（目前是 1.2 \~ 1.5 秒的極速體驗）。



但我覺得可以在既有的網站體系裡面，不用多開資料庫、串什麼東西，就可以用純靜態的方式產生這樣的內容，並且還可以連結到每一則 stream 的段落，我還是相當滿意這樣的成果！