---
title: Pin 起來的 Changelog
description: 這邊放置 Pin 起來網站的 Changelog，主要的內容是描述「這個網站」本身的變化，包含新增、調整、或刪除的內容。
path: changelog/
draft: false
date: 2022-04-20
updated: 2023-01-14
template: changelog.html
---

這邊放置 Pin 起來網站的 Changelog。

Changelog 主要是講「這個網站」本身的變化，包含新增、調整、或刪除，因此與[所有文章歸檔](/archive/)的內容不同，在 changelog 頁面只會有與網站本身相關的內容。

版本號的格式，主要是參考「[語意化版本 (Semantic Versioning)](https://semver.org/) 這個有趣的規範，[x,y,z] 裡面， x 是主版號， y 是次版號， z 是修訂號。

但因為本網站不是軟體，所以我對於這三個項目的定義有點不一樣，跟「 API 是否相容」無關。

我的定義如下：
- 主版號：表示部落格有了大幅度的改版，例如更換架設方式、網域、部署方式等。這個網站完成後是 1.0.0，在 2022 年的最後一天更新到了 2.0.0。
- 次版號：表示部落格有新增功能，這邊的功能指的是某些特定欄位、頁面、超連結等，讓讀者可以更好使用、閱讀更多內容的都算是新增功能。
- 修訂號：表示部落格既有功能有修改內容，例如 css 樣式的調整、既有頁面或段落的連結調整、或者分類類別的調整等。

以下是依時間倒序排列的 changelogs ，歡迎瀏覽！

---

## [2.1.0] - 2023-01-14

- 網站新增了「[搜尋](/search)」的功能！


---

## [2.0.1] - 2023-01-01

- 把昨天沒來得及處理完的一些跑版問題處理完，現在手機上 header 也能正常顯示了。
- 也把之前不知為何固定鎖死的 h1 font-size 調整為可變化的設定。
- 也調整了首頁的呈現內容，把原先設定為「Blog 為主」的呈現方式，調整為一頁單純的 MOC。不知為何，光這個舉動就讓搬回筆記後原本要 16, 17 秒的編譯時間，重新回到 5 秒左右，超讚的。

---

## [2.0.0] - 2022-12-31

- 今天一個起心動念，想把筆記與想法的子網站搬回主網站這邊，就開始動工。經過一整個下午與晚上的調整與導入後，完成了全新的 2.0 版本，把內容分成三個區塊： Blog, Newsletters, Snapshots。
- 我把搬家的紀錄跟簡單心得放在這篇文章：[我把筆記與想法快照的內容都搬回 Pin 起來主網站了](/blog/migrated-notes-and-snapshots-back-to-the-main-site)

---

## [1.10.5] - 2022-12-30

- 今天心血來潮詢問 ChatGPT 一些 css 的問題，就順帶把網站的每篇文章「分開」了，原先每篇文章都會黏在一起，有時比較不好區分不同文章，現在分開後清爽不少！

- 對照圖，左邊是修改後，右邊是修改前：![](https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/separated-articles_1ybAat.webp)

---

## [1.10.4] - 2022-12-24

### Changed

- 根據[這篇紀錄](/snapshots/what-i-tried-today/updated-og-image-settings/)的作法調整了部落格裡對於 og image 的相關設定，讓未來的社群預覽能夠更多變化。

---

## [1.10.3] - 2022-11-27

### Fixed

- 微調 taxonomy_single.html 的排序方式。

今天在上傳新文章後發現在「清單檢視」時，文章的順序有點混亂，好像不是依照倒時序排列。找了一下以後發現找不太到原因（我只知道那一頁是由哪個檔案處理，但不知道為何無法正常排序）。我猜想可能是某種預設的排序方式，但可能在滿足某些條件的狀況下，排序會變。
- 不過我試圖從既有的程式碼裡面挖掘可能的解方，最後測試成功，解決方式是：

```
把原先在 taxonomy_single.html 的
{% for page in term.pages %} 
增加了一段，變成：
{% for page in term.pages | sort(attribute="date") | reverse %} 
```
這樣就好了！

目前看起來，各個頁面都可以依照發布日期正常倒序排列了！

---

## [1.10.2] - 2022-07-10

### Changed

- 效仿 [Owen 的部落格作法](https://www.owenyoung.com/en/changelog/#2022-07-06-desktop-read-mode)，把部落格的內文區塊區隔開來，製造出類似 reader mode 的效果，讓文章的區塊更好閱讀。

- 對照圖：![](https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/reader-mode_9FwDHl.webp)


---

## [1.10.1] - 2022-07-03

### Removed

- 移除了「新 Pin 上線」這個類別的文章，因為我近期發現，這類嚐鮮介紹的內容我大多會直接放在 Snapshot 裡面的「[What I Found Interesting](/kinds/what-i-found-interesting/)」類別裡面。既然這樣，那就把原先的類別簡化一下，把這些都放回 [Tools](/categories/tools/) 類別裡面。


---

## [1.10.0] - 2022-06-19

### Added

- 成功地安裝了網站的評論系統 [Cusdis](https://cusdis.com/) ！目前在每篇文章與電子報底下都可以留言，完全匿名，但會需要由我審核通過才會出現，基本上我的原則是全部都會通過，除非是無意義的灌水或洗版。這部分之後再來訂規則好了，很開心部落格有了這個簡單清爽的留言評論系統。

---

## [1.9.0] - 2022-06-18

### Added

- 網站的數據追蹤系統改為 [umami](https://umami.is/) ，安裝的紀錄可以參考[嘗試安裝 umami 成功](/snapshots/what-i-tried-today/tried-to-install-umami-on-my-websites)這篇文。安裝後也把 Google Analytics 的追蹤碼移除了！

---

## [1.8.0] - 2022-06-04

### Added

- 增加了置頂的 navbar ，把 Logo、文章、電子報、歸檔等主要項目放上去。這樣做的用意是讓讀者在瀏覽時更容易找到內容。然後因為我還不會用漢堡選單的收縮方式，所以暫且用這樣的版本就好。

### Removed

- 刪除原本放在首頁最上方的 LOGO ，因為 navbar 有了
- 刪除原本放在每頁 sidebar 底部的「回到首頁」，因為 navbar 有了
- 調整了 sidebar 的「常用連結」中的電子報，因為 navbar 有了

---

## [1.7.2] - 2022-05-08

### Changed

- 把 Pin 起來的 wiki page 從 Logseq 改為 Dendron 輸出，網址不變一樣是 https://wiki.pinchlime.com （2023.01.02 更新，目前經過兩次迭代，個人 wiki 的內容已經都變成站上的 [Snapshots](/snapshots) 專區的內容了），但內容則換了。也覺得可以把連結放到 Sidebar 上面了。

--- 

## [1.7.1] - 2022-05-02

### Changed

- 微調註腳的樣式，把字級調小，讓註腳的內容跟本文有一點區別性。調整的方式是：
1. 在 ftnt.html 這個 shortcode 裡面，<p> 的地方新增一個 p class。
2. 在 site.css 裡面，定義這個 class 的字級大小。

--- 

## [1.7.0] - 2022-04-30

### Added

- 部落格上線了 footnotes 的功能，具體的說明可以看[部落格新增了 Footnotes 註腳的功能](/blog/added-footnotes-function)這篇文章。


---

## [1.6.3] - 2022-04-28

### Fixed

- 在 base.html 增加了一段 `{% block canonical_url %}{% endblock canonical_url %}` ，並且在 section.html 頂端加上這個 block ，把 paginator 的 section 頁面加上 canonical 的標籤。


---

## [1.6.2] - 2022-04-27

### Changed

- 把 config.toml 裡面， tags 跟 categories 兩個 taxonomies 的 feeds 及 paginator 開關都關閉，覺得我的內容沒多到要用類別來訂閱，所以不需要開那麼多 feeds ，而在取消全文預覽後也不需要分頁，讓整個頁面的架構更單純一些。 

---

## [1.6.1] - 2022-04-25

### Changed

- 把單一 category 或 tag 的頁面改成只有標題與發布日期。考量點之一是避免同樣的預覽內容重複被搜尋引擎檢索，考量點之二是我覺得透過 categories 或 tags 的連結點進來想看文章的人，如果可以一次看到完整的文章列表，可能可以更快找到「更想看」的內容（而不是依照時序，倒序排列的預覽內容）。

改的方式是把原先 taxonomy_single 採用的 macro 由 post_max 改為 post_min ，並把 macro::paginator 拿掉。

### Fixed

- 修復了站內每個頁面的 og:url, og:title & og:descriptoon，原先許多頁面並沒有特別設置，或者路徑有誤。以下是目前站內主要的幾種 og:url 路徑：

```rust
# Pages 的 og:url ：
{% block ogurl %}{% if page.path %}{{ config.base_url }}{{ page.path }} {% endif %}{% endblock ogurl %}

# Sections 的 og:url ：
{% block ogurl %}{{ config.base_url }}{{ section.path }}{% endblock ogurl %}

# Taxonomy List 的 og:url ：
{% block ogurl %}{{ config.base_url }}/{{ taxonomy.name }}{% endblock ogurl %}

# Taxonomy Single 的 og:url ：
{% block ogurl %}{{get_taxonomy_url(kind=taxonomy.name,lang=lang, name=term.name)}}{% endblock ogurl %}
```
感謝 [@Owen](https://twitter.com/OwenYoungZh) 跟我分享這些錯誤，讓我好好地修復了一下。

---

## [1.6.0] - 2022-04-24

### Added

- 新增了電子報專屬的[「所有電子報歸檔」](/newsletters/archive) 頁面，參考[「所有文章歸檔」](/archive) 的製作方式，依照時序排列發布過的電子報們。

### Changed

- 微調 archive.html ，把[「所有文章歸檔」](/archive)裡面的內容限定在「部落格」的文章，排除掉「電子報」類型的文章。覺得兩者的文體不太一樣，電子報應該可以有自己的歸檔頁面。（微調方式是把 `{% set all_section_pages = get_section(path="_index.md") %}` 改為 `{% set all_section_pages = get_section(path="blog/_index.md") %}` ，另外也把這段往下拉到 {% block main %} 裡面，避免抓到 base.html 的內容。


---

## [1.5.0] - 2022-04-23

### Added

- 嘗試透過 Logseq 內建的 Export graph 功能，建立一個靜態的 wiki 架構網站，並且順利部署在 Netlify 上面，也順利設定了子網域 [https://logseq.pinchlime.com](https://logseq.pinchlime.com) ，之後再來慢慢更新。

### Fixed

- 在 base.html 加上了 og:image 的 width & height ，也增加了一個 `<meta name="twitter:image" />` 的設定，目前看起來在 Twitter 分享時總算有縮圖了！也學到可以透過 Twitter 的 [Card Validator](https://cards-dev.twitter.com/validator) 先預覽連結縮圖。
- 在 page.html 改了 og:url 的規則，把原本的 if page.slug 改成 if page.path ，因為我為了讓網址跟之前 wordpress 時期的網址一致，主要都是透過 path 來達成絕對的網址。調整完後打開 inspect 看到 og:url 正確了，但不太確定為何在 Facebook Developers 的偵測工具裡面還是錯誤的。


---

## [1.4.0] - 2022-04-22

### Added

- 在首頁側邊欄上也新增了最新電子報的區塊，抓取最新五篇電子報。

### Changed

- 把首頁側邊欄的最新文章改為 5 篇，以避免太多內容。
- 把「所有文章歸檔」從常用連結移至下方，跟「所有標籤」整合成為「看更多文章」，並且改成「依標籤」以及「依時序」，讓同性質的內容（完整檢索文章）一起出現。
- 把 Changelog 這頁右上的「目錄」拿掉，避免內容過多以後側邊欄變得無法閱讀。拿掉的方式很笨，是複製 page.html 變成一份 changelog.html ，然後本頁的 template 設置成 changelog.html。

### Fixed

- 原本在[關於](/about/)頁面中，[Pin 起來的 新Logo](/2022/02/27/the-new-logo-of-pinchlime/) 的連結設錯了，改回正確的內容。

---

## [1.3.0] - 2022-04-21

### Added 

- 新增了「[所有標籤](/tag-list)」頁面，放置網站上的所有標籤。
- 新增「回到首頁」的按鈕在 base.html ，避免某些「非文章」的頁面因為不是讀 page.html 而無法快速回到首頁。

### Removed

- 刪除原先在首頁側邊欄的「標籤」區塊，因為隨著標籤漸增，該區塊變得難以閱讀。

---

## [1.2.0] - 2022-04-20

### Added

- 開始更新 Pin 起來的 Changelog 頁面，並補上此版本以前的內容。

---

## [1.1.0] - 2022-04-19

### Added

- 增加了側邊欄的 [Pin 起來電子報](/newsletters) 單頁，並放入目前為止的 8 期電子報歸檔。
- 學會在 _index.md 檔案裡面，透過 template & page_template 宣告要採用的 templates ，藉此達到特製的效果。
- 學會了透過 page.extra 的方式增加自訂的 metadata。
- 把前兩者結合，用在電子報相關的文章上面，因此每則電子報點選後，就可以直接看到「第 n 期」這個特殊的屬性。
- 開始在部落格裡埋入 GA 追蹤碼。

### Changed

- 將首頁最下方的「所有文章」改為「看更多文章」，並將連結由「/blog」改為「/blog/page/2」，等於直接連到部落格以文章排序的第 2 頁（第 11 篇文章開始），更貼近使用直覺。
    - 樣式上從靠左，改為透過 `flex` 置中。

---

## [1.0.0] - 2022-04-17

### Added 

- Pin 起來改版，網站全新上線 （可參考[Pin 起來改版了！從 Wordpress 搬家到 Zola！](/blog/rebuilt-pinchlime)）
- 網域自 wordpress.com 移轉至 Google  Domains
- 網站開始部署於 Netlify

---

## [0.4.0] - 2022-04-16

### Added

- 在 page.html 裡增加「看更多＿＿＿分類」以及「看更多＿＿＿標籤」的功能，會根據當前頁面的分類與標籤，自動抓取＿＿＿的文字，並且可超連結到該分類或標籤。

### Changed

- 調整了 site.css ，讓不同地方的 h1, h2, h3 等樣式一致
- Toolbox 分類改為 Tools
- Blog 分類改為 Pinchlime

---

## [0.3.1] - 2022-04-14

### Changed

- 把主要文章欄位的寬度從 44rem 調整為 51 rem ，感覺比較順眼些。
- 新 Pin 上線分類改為 New Pins ，避免變成不知道如何改變的拼音音譯網址。
- 微調 base.html 的 sidebar 樣式。

---

## [0.3.0] - 2022-04-13

### Added 

- 透過新增 macro.html 以及 base.html 來新增側邊欄的「最新文章欄位」（可參考[增加了部落格側邊欄的「最新文章」欄位](/blog/added-latest-section-in-sidebar)）

---

## [0.2.0] - 2022-04-12

### Added

- 成功將最小測試站部署在 Netlify 上，透過 Owen 的協助，學到必須先設定好 base_url 才讀得到 site.css （要設定為 網域名.netlify.app ）

--- 

## [0.1.0] - 2022-04-11

### Added

- 將 [Owen's Blog](https://www.owenyoung.com/) 的 [原始碼](https://github.com/theowenyoung/blog) clone 了一份，並開啟自己的 repository ，開始理解每個檔案的用途及內容，並且刪除掉 Owen 的文章，只放入一篇自己的文章測試最小程度的網站。