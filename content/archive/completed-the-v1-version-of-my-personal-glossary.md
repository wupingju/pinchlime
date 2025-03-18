---
title: 完成了站內的 Glossary 個人詞庫 v1 版本
date: 2023-01-27
description: 我想要透過這個功能，讓我在使用比較專有的詞彙時，能夠更清楚知道自己到底在講什麼，避免使用自己其實不太熟悉的酷炫詞彙。
path: blog/completed-the-v1-version-of-my-personal-glossary
extra:
  page_type: archive
---


大約在兩個多禮拜前，我寫下了「[我打算在網站上建立的「個人詞庫」是什麼？](@/archive/what-what-is-the-personal-glossary-section-i-plan-to-build-on-my-website.md)」這篇 snapshot，當時就想著過年期間要來把這個詞庫的 1.0 版本蓋起來。

這兩天順利完成了！來分享一下紀錄。

<!-- more -->
---

## 我的個人詞庫簡介

這個個人詞庫在 Pin 起來這個網站裡面，跟「blog, newsletters, snapshots」一樣，屬於的是「section」層級，意思是他可以有自己獨立的主頁設定、也可以為同類型的內容設置獨立的內容範本。

目前設置的版本裡面，大致上的內容與之前發想的類似，甚至更少。一定會有的內容只有標題、日期、至少一個定義，就這樣。


而其他選填的內容則包含：

* Alias 別名：例如 cryptocurrency 可能有加密貨幣、密碼貨幣、密碼學通貨等等，這部分主要是希望使用者在透過搜尋查找內容時，也有機會找到對應的內容。

* Related to：與之相關的概念。

* Backlinks：有連結到這個詞彙的頁面。

* My thoughts ：我對這個詞彙的任何想法。


我覺得未來肯定會有更多擴充，但目前的版本應該先這樣就好。


而在一番調整與設定後，目前的成果會類似下圖這樣：


<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/glossary-demo_jg0m8o.webp" data-fancybox data-caption="glossary-demo">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/glossary-demo_jg0m8o.webp" loading="lazy" alt="glossary-demo" align="center" />
</a>


由上往下的結構是：

* 標題
* 別名區塊
* 定義區塊
* Backlinks 區塊
* Contact 區塊

其中「標題」跟「別名」都是在文件的 metadata 區域設定的，而「定義區塊」則是透過 Zola 的 shortcode 功能建立的，反向連結則是透過 「[部落格加上了 Backlinks 的功能](@/blog/supported-backlinks.md)」 這篇提到的功能建立的。

---

## “Definition I Collected” 區塊的建構方式

裡面我最喜歡的新嘗試是透過 shortcode 這種簡單的「自定義區塊」來建構出類似「template」的效果。

先前的我跟 shortcode 其實不太熟，因為 Zola 官方提供的說明太簡潔了，之前幾次嘗試都用不太好。

但近期我好像越來越開竅一些，因此就來挑戰看看，最後也順利成功！

我設置的 shortcode ，都放在「glossary.html」這個檔案裡面，原始碼長這樣：

```html
<div>
    <h3 style="font-weight: 500;">Definition I Collected</h3>
    <blockquote>
      <p>{{ body | safe }}</p>
      <div style="display: flex; justify-content: right;">
        <p>
        <span>Source:&nbsp;</span>
        {% if link %}
        <a href="{{ link }}">{{ source_name }}</a>
        {% else %}
        {{ source_name }}
        </p>
        {% endif %}
        </div>
    </blockquote>
</div>
```

裡面的概念大致上可以白話翻譯如下：

* 有我自訂的固定文字與樣式設定，例如 h3 的標題 “Definition I Collected” ，或者是 “Source” 的超連結，以及整個區塊都被我設定為「blockquote」的類型。

* 其中有幾個「變數」，分別是 `{{ body }}`, `{{ link }}`, `{{ source_name }}` ，這三個東西是我後續每則詞彙定義都可以填入的內容。

* 另外我也設置了一個 if 的邏輯，意思是，假設我有填入 link ，它才會去讀取這個連結並幫我設置超連結，否則就只會單純呈現來源的內容而已。


設置完這段 shortcode 後，接下來我在每篇詞彙的內容裡面，只要插入類似下面這段 shortcode ，就會自動渲染成我定義好的樣式與架構了：

```rust
{% glossary(source_name="ChatGPT and the Future of Domain Expertise",link ="https://interconnected.blog/chatgpt-and-the-future-of-domain-expertise/") %-}

Things you know that others don’t.
<br>
那些你知道「別人不知道的事」。

{% end %}
```

這段內容的翻譯如下：

* glossary 是 shortcode 的名稱

* 後面的括號裡面，必須放置除了 `{{ body }}` 以外「必要」的變數，以這個 glossary shortcode 來說， `{{ source_name }}` 是必要的變數，而 `{{ link }}` 則是選填的變數。

* 而在首行與末行之間的內容，就是 `{{ body }}` 的內容了，不用再特別設定。

* 所以說，當我填入上面這些內容後， Zola 在編譯建構網頁時，就會自動幫我把我自訂的變數帶入預先設定好的 shortcode template ，並且跑出我預先規劃的樣式。

透過這個 shortcode，我就可以把 Source 的連結放在右下角，然後讓這個定義有種小卡片的感覺。

---

## 透過 Github 協作更新定義


另一個我首次設定的功能是在頁尾加入每個詞彙的 github edit 連結。

我想加入這個功能的原因是，我覺得「詞彙的定義」比較不是來自於我自己的想法，而且我沒有打算花時間去窮盡研究所有定義版本，因此極有可能有「更好的解釋版」，因此我想要引入某種程度的協作。

不過我還尚未跟任何人透過 git 協作過，因此也不知道最後會變成怎樣，也許根本沒人想用、也許哪天我覺得太麻煩就拔掉了也說不定，總之再觀察看看！

---

## 後記：期待能更有意識地理解與使用詞彙


回到當時建立個人詞庫的初衷，我想要透過這個功能，讓我在使用比較專有的詞彙時，能夠更清楚知道自己**到底在講什麼**，避免使用自己其實不太熟悉的酷炫詞彙。

同時，我也希望透過這樣的功能，能夠讓自己的個人知識體系更完整、產生更多有價值的連結。


期待後續的個人詞庫演進與心得分享！