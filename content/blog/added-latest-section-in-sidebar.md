---
title: 增加了部落格側邊欄的「最新文章」欄位
date: 2022-04-13
updated: 2022-04-13
description: 透過這次修改的經驗，更熟悉 Zola 裡面的 base.html 跟 macro.html 是怎麼互動的，覺得很有邏輯，連我這種完全程式外行的人都能改出自己想要的感覺，相當開心！
path: blog/added-latest-section-in-sidebar
draft: true
taxonomies:
  categories: 
    - Pinchlime
  tags: 
    - Zola
---

這篇文簡單紀錄一下側邊欄的「最新文章」段落是怎麼製作出來的。

原先我的側邊欄是沿用 [Owen 的部落格](https://www.owenyoung.com/) 的架構，分成所有分類、常用連結、標籤三大類，如下圖：

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/original_SmgCWA.webp" data-fancybox data-caption="original">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/original_SmgCWA.webp" loading="lazy" alt="original" align="center" />
</a>

但我今天突然想到，我想讓這個側邊欄有更多的連結，例如可以放上最新的文章，或者是未來把電子報也放進來，就可以放入最新幾期的電子報。

有了這個想法以後，就聯想到， Owen 的部落格裡面好像有類似的功能：「以下是我最新的 5 篇文章」。

於是我就開始看他的這個功能是怎麼實現的。

<!-- more -->

### Owen 的 blog

按圖索驥後發現 Owen 的部落格在 index.html 裡面有一個區塊是：

```rust
<h2>{{trans(key="label_new_posts_list_title",lang=lang) | markdown(inline=true) | safe}}</h2>
<section class="articles">
{% set all_blog_pages = get_section(path="blog/_index"~file_lang_path~".md") -%}
{% for page in all_blog_pages.pages | slice(start=0,end=5)  %} 
  {{ macro::post_max(page=page) }}   
{% endfor %} 
```

我的理解是，這一段的白話說明是：

- 先顯示在 config.toml 裡面的 "label_new_posts_list_title" 對應的字串：「以下是我最新的5篇文章」。
- 設定 "all_blog_pages" 這個變數成為 "blog" 資料夾裡面的 .md 檔案。
- （slice 還看不懂，但知道是抓 5 篇）。
- 然後導入 macro:post_max 這個 macro。

但 Owen 的設定裡面，這段語法是在 index.html ，也就是在首頁出現。我想要的則是在 Sidebar 出現，因此要來找找 Sidebar 的設定在哪。

---

搜尋了一下關鍵字後，發現 Sidebar 在 Owen 的 blog 裡面是在 base.html 這份文件裡面出現，因此找到對應的段落後，把剛剛那段代碼插入，是順利出現這個「最新文章」的區塊了，但卻顯示成為全文預覽的樣子：

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/sidebar-1_g8AJAB.webp" data-fancybox data-caption="sidebar-1">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/sidebar-1_g8AJAB.webp" loading="lazy" alt="sidebar-1" align="center" />
</a>

這時觀察了一下，發現可能是語法裡面這段造成的：

```rust
  {{ macro::post_max(page=page) }}   
``` 

所以又跑去找這段在寫什麼。

---

### 自己改改看

此時在 macros.html 這份文件裡面找到了 {% macro post_max(page) %} 相關的代碼，發現他有些複雜，已經超出了我的理解範圍，此時看到有另外一個 macro 叫做 post_min ，因此就直接把原始語法的 post_max 改成 post_min ，結果還真的發揮作用了：

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/sidebar-2_cpy1MJ.webp" data-fancybox data-caption="sidebar-2">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/sidebar-2_cpy1MJ.webp" loading="lazy" alt="sidebar-2" align="center" />
</a>

此時畫面的感覺已經很像我想要的樣子了，只有那個 "Updated on..." 跟我想的不太一樣，但此時再回去看 macros.html 裡面的 post_min 就相對好懂很多：

```rust
{% macro post_min(page) %}
<a href="{{ page.permalink }}">{{ page.title }}</a> <span class="muted text-sm">Updated on {{ page.updated }}</span>
{% endmacro post_min %}
```

這段代碼的意思應該是指：

```rust
{% macro post_min(page) %}
<a href="{{ 頁面連結 }}">{{ 頁面標題 }}</a> <span class="muted text-sm">Updated on {{ 更新時間 }}</span>
{% endmacro post_min %}
```

所以我想拿掉或想調整的就是後段的字而已，但我又不想要讓網站上其他用到 macro post_min 的段落一起改動，因此我就新增了一個 macro post_side ，並且調整為：

```rust
{% macro post_side(page) %}
<a href="{{ page.permalink }}">{{ page.title }}</a>
{% endmacro post_side %}
```

這時就差不多長成我要的樣子了：

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/sidebar-3_qCecNr.webp" data-fancybox data-caption="sidebar-3">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/sidebar-3_qCecNr.webp" loading="lazy" alt="sidebar-3" align="center" />
</a>

後來還亂調整了一些小地方，讓這個區塊跟上下能長得更像一點，在這邊就不多提了！

---

### 小結

透過這次修改的經驗，更熟悉 Zola 裡面的 base.html 跟 macro.html 是怎麼互動的，覺得很有邏輯，連我這種完全程式外行的人都能改出自己想要的感覺，相當開心！

之後再來試試看製作一個電子報的 section ，並且把最新的電子報內容丟上來！