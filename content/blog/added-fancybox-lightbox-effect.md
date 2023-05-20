---
title: 網站新增了 Fancybox 的圖片燈箱功能
date: 2023-05-20
description: 由於最近開始重拾相機，因此也想要站內能夠好好地呈現圖片、照片，於是就來研究一下有哪些選項。我稍微看了一下 Fancybox 的安裝與設定說明，發現好像蠻簡單的。實際試了也發現很容易做、效果很不錯，所以就直接設定了。
path: blog/added-fancybox-lightbox-effect
taxonomies:
  categories: 
    - Pinchlime
  tags: 
    - Zola
    - Fancybox
---

這兩天又幫網站新增了一個小功能：圖片燈箱彈窗。效果可以直接點擊下圖參考：

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/fancybox_HOCpt7.webp" data-fancybox data-caption="fancybox">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/fancybox_HOCpt7.webp" loading="lazy" alt="fancybox" align="center" />
</a>

### Why？

我不確定有沒有人特別注意到，網站之前一直沒有這個功能，若你點擊站內的圖片，不會有任何的效果。這造成的「問題」是，許多圖片為了符合內容區塊的寬度，都會被縮得比較小。雖然按開啟圖片到另一個分頁可以解決這個問題，但不太直覺。

由於最近開始重拾相機，因此也想要站內能夠好好地呈現圖片、照片，於是就來研究一下有哪些選項。

### How？

我原本以為這個只要加幾行 CSS 就好，所以就問 ChatGPT 該怎麼做，結果他推薦我使用 [Fancybox](https://fancyapps.com/fancybox/) 這個 Library ，我稍微看了一下安裝與設定說明，發現好像蠻簡單的。實際試了也發現很容易做、效果很不錯，所以就直接設定了。

我的作法是：

步驟一： 在 base.html 的 `</head>` 標籤前增加一段 code：

```javascript
<script src="https://cdn.jsdelivr.net/npm/@fancyapps/ui@5.0/dist/fancybox/fancybox.umd.js"></script>
    <link
      rel="stylesheet"
      href="https://cdn.jsdelivr.net/npm/@fancyapps/ui@5.0/dist/fancybox/fancybox.css"
    />
```

步驟二： 依照 Fancybox 的[文件說明](https://fancyapps.com/fancybox/getting-started/)，把 <img> 改成他規定的寫法，例如，我原本某張圖片是：

```javascript
<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/limitless-opportunities_NMXjPk.webp" loading="lazy" alt="limitless-opportunities" align=center />
```

就要改成：

```javascript
<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/limitless-opportunities_NMXjPk.webp" data-fancybox data-caption="limitless-opportunities">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/limitless-opportunities_NMXjPk.webp" loading="lazy" alt="limitless-opportunities" align="center" />
</a>
```

這樣就完成了！

步驟三：

接著我就是請 ChatGPT 協助幫我轉換格式，如下圖，因為這是很簡單的工作，我就直接用更快的 GPT-3.5 ，效果很好！省了我超多時間，總共轉了一百多張圖。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/translate-to-fancybox_gox5zo.webp" data-fancybox data-caption="translate-to-fancybox">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/translate-to-fancybox_gox5zo.webp" loading="lazy" alt="translate-to-fancybox" align="center" />
</a>



---

### Next

Fancybox 還有其他比較進階的用法，例如 Slideshow, Toolbar 等等，這些就之後再來嘗試用用看，至少目前純圖片可以有燈箱的效果，我就非常滿意了！