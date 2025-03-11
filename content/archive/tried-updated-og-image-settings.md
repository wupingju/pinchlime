---
title: 嘗試改變部落格裡 og image 的設定
date: 2022-12-24
updated: 2022-12-24
description: 接下來在社群上分享文章顯示的圖應該會更好看了！
path: snapshots/what-i-tried-today/updated-og-image-settings
taxonomies:
  categories: 
    - Pinchlime
  tags: 
    - Zola
extra:
  page_type: archive
---

最近又開始比較密集分享兩個部落格的文章，不過在 Twitter 上面分享時，通常都只會顯示部落格的 LOGO （如下圖），沒辦法顯示裡面的配圖。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/logo-as-ogimage_MrGaxT.webp" data-fancybox data-caption="logo-as-ogimage">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/logo-as-ogimage_MrGaxT.webp" loading="lazy" alt="logo-as-ogimage" align="center" />
</a>

今天剛好有空，想來調整這部分的設定。

這個部落格的 og-image 設定是放在 base.html 這份檔案裡面，之前的寫法是寫死成固定的圖檔連結，而這次要做的事情是，希望他能夠有些彈性，假設我在文章裡面特別設定了 "extra.image" 的路徑，就要把 og:image 設定為該路徑。但若沒設定，則還是維持原本的 LOGO。

所以我在原先的設定前面新增了

```
{% if page.extra.image %}
```

讓文章裡面若有這個設定，就會影響下面抓的 og:image 內容。

最後也順利成功了！（雖然可能程式碼的結構不是很乾淨，但可以順利通過編譯）

接下來在社群上分享文章顯示的圖應該會更好看了！