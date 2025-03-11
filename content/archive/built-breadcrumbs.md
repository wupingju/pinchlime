---
title: 透過 ChatGPT 建構麵包屑導航
description: 我覺得這次很順利完成目標的原因是，我在第一次的 prompt 就提供給 ChatGPT 還算完整的資訊。（我使用的是 2023 年 5 月的 GPT 4 模型）例如，我提供了我的頁面結構、我期待的內容、我跟他說明當我使用某個參數時我會得到怎樣的內容、最後我也給他「macro」的結構大概是怎樣的，剩下就請他發揮。
date: 2023-05-17
updated: 2023-05-17
extra:
  page_type: archive
---

## 我想解決的問題

我前幾天透過 ChatGPT 製作了一版麵包屑導航的功能，就是在目前畫面上方的 Library 等連結。

不過，當我測試後，我發現這個版本有點不符合我的需求。因為我習慣會透過 `path` 這個參數來自定頁面的路徑，例如，我的 Heptabase 頁面的路徑是 library/toolbox/featured/heptabase，但我希望設定成 Library/heptabase。

我想這樣設定的原因是，假設未來我移動了這個頁面的層級，我希望他的 URL 仍是維持固定不變，這樣即使先前有人連結到這個頁面，連結都不會跑掉。

但我發現，這個版本的麵包屑程式碼會跟我自訂 path 的行為衝突，因為當我自訂 path 以後，麵包屑只抓取 path 的路徑，就會讓導航列變成 Library > Heptabase ，而漏了中間的另外兩個層級。

---

## 我想像的解決方案
我前兩天嘗試了透過 ChatGPT 修改都失敗，後來重看了 [Zola 的官方文件](https://www.getzola.org/documentation/templates/pages-sections/)，裡面提到一個有趣的變數叫做 `relative_path: String;` ，這個變數可以讓我取得當前頁面的相對路徑，因此，即使 path 被我自訂了，我還是能夠抓取原始的路徑。這下子我覺得有機會建構導航了，就開始跟 ChatGPT 合作。

---

## 我與 ChatGPT 的對話

### 我提供的資訊

我把我掌握的資訊、以及我可以提供的範例都一起丟給 ChatGPT ，完整的 Prompt 如下：

```
我正在使用 Zola 的 Tera 模板，現在我想要為我的 pages 設置麵包屑連結，

我的頁面結構如下：
以 /library/toolbox/featured/keyboard_maestro.md 來說，我有為他設置特定的 path : library/keyboard_maestro ，因此他的 path 會是 library/keyboard_maestro

但我期待的是得到如下的麵包屑架構：

Library > Toolbox > Featured > Keyboard Maestro

我有以下參數可以使用：

當我使用 {{ page.relative_path }} ，我會得到 library/toolbox/featured/keyboard_maestro.md ，我想這個可以透過 get_page 拿來設置 Keyboard Maestro 本身的超連結。

當我使用 {{ page.ancestors }} ，我會得到 [_index.md, library/_index.md, library/toolbox/_index.md, library/toolbox/featured/_index.md] ，我想這些可以讓我透過 get_section 來設置 Library > Toolbox > Featured 等幾個超連結

請為我設置一段 macro ，你可以參考下列 macro：

{% macro breadcrumbs(current_section) %}
<div class="pt" style="padding-bottom: 1rem;">
  {% for path in current_section.ancestors %}
    {% if path != "_index.md" %}
      {{ macro::breadcrumb_link(path=path) }}
      <span>></span>
    {% endif %}
  {% endfor %}
  {{ macro::breadcrumb_link(path=current_section.path) }}
</div>
{% endmacro breadcrumbs %}
```

### ChatGPT 的回覆：

ChatGPT 回覆如下：

> 在 Zola 的 Tera 模板中，我們可以使用 get_section 或 get_page 來根據路徑獲取頁面或者部分的資訊。以下是一個簡單的 macro 範例，它可以解析 page.ancestors 和 page.relative_path 來產生你需要的麵包屑：

<br>

```rust
{% macro breadcrumb_link(path) %}
  {% set section = get_section(path) %}
  <a href="{{ section.permalink }}">{{ section.title }}</a>
{% endmacro breadcrumb_link %}

{% macro breadcrumbs(page) %}
<div class="pt" style="padding-bottom: 1rem;">
  {% for path in page.ancestors %}
    {% if path != "_index.md" %}
      {{ breadcrumb_link(path=path) }}
      <span>></span>
    {% endif %}
  {% endfor %}
  {% set page_title = get_page(page.relative_path).title %}
  <a href="{{ page.permalink }}">{{ page_title }}</a>
</div>
{% endmacro breadcrumbs %}
```

> 這裡的 breadcrumb_link macro 會將路徑傳遞給 get_section 來獲取該部分的資訊，然後生成一個麵包屑連結。麵包屑連結的名稱由該部分的 title 決定，而連結的目標則由 permalink 決定。

> 在 breadcrumbs macro 中，我們首先對 page.ancestors 進行迭代。對於每個祖先路徑，我們檢查它是否為 _index.md。如果不是，則我們使用 breadcrumb_link macro 生成一個麵包屑連結。最後，我們使用 get_page 來獲取當前頁面的 title，並生成一個指向當前頁面的麵包屑連結。

> 請注意，你需要確保每個部分的 _index.md 檔案都設置了 title 屬性，否則這些麵包屑連結可能不會正確顯示。同時，確保你的路徑都是以 _index.md 結尾的。

<br>

我測試了這段 macro 後，接著就是將 Zola 呈現的錯誤訊息再貼回給 ChatGPT ，並且持續調整，大概經過 5 次的調整後，一切都順利完成了。

現在即使我設定頁面的 `path` 連結為特定的內容，麵包屑的導航還是會準確抓到這個頁面自身、上層的所有 section ，並且幫他們建立連結。

---

### 最終的程式碼
在這邊也分享一下最後的成果。

一共有兩段 macro：

```rust
{% macro page_breadcrumb_link(path) %}
  {% set section = get_section(path=path) %}
  <a href="{{ section.permalink }}">{{ section.extra.bread_name }}</a>
{% endmacro page_breadcrumb_link %}
```

```rust
{% macro page_breadcrumbs(page) %}
<div class="pt" style="padding-bottom: 1rem;">
  {% for path in page.ancestors %}
    {% if path != "_index.md" %}
      {{ macro::page_breadcrumb_link(path=path) }}
      <span>></span>
    {% endif %}
  {% endfor %}
  {% set current_page = get_page(path=page.relative_path) %}
  <a href="{{ page.permalink }}">{{ current_page.title }}</a>
</div>
{% endmacro page_breadcrumbs %}
```

然後我在 library_page.html 這個 template 模板裡面，透過這段程式碼來呼叫這兩段 macro：

```rust
{% block breadcrumbs -%}
{{ macro::page_breadcrumbs(page=page) }}
{% endblock breadcrumbs %}
```

一切都很順暢的運作，且比原本的 macro 語法還要簡潔很多。

---

## 我學到的事

我覺得這次很順利完成目標的原因是，我在第一次的 prompt 就提供給 ChatGPT 還算完整的資訊。（我使用的是 2023 年 5 月的 GPT 4 模型）例如，我提供了我的頁面結構、我期待的內容、我跟他說明當我使用某個參數時我會得到怎樣的內容、最後我也給他「macro」的結構大概是怎樣的，剩下就請他發揮。

但假設我單純請他為我建構一段 Zola 的 macro ，（我有測試了一下單純用「我正在使用 Zola 的 Tera 模板，現在我想要為我的 pages 設置麵包屑連結，請你為我建構對應的 macro 以及 html 程式碼：」來請他協助，但效果差非常很多。

我猜想，一方面因為 Zola 是很冷門的架構，另一方面是這個需求稍微有點複雜，所以若能給他較完整的資訊，表現就會好很多。