---
title: Pin 起來的 Changelog
path: changelog/
draft: false
date: 2022-04-20
updated: 2022-04-21
template: changelog.html
---

這邊放置 Pin 起來網站的 Changelog。

Changelog 主要是講「這個網站」本身的變化，包含新增、調整、或刪除，因此與[所有文章歸檔](/archive/)的內容不同，在 changelog 頁面只會有與網站本身相關的內容。

版本號的格式，主要是參考「[語意化版本 (Semantic Versioning)](https://semver.org/) 這個有趣的規範，[x,y,z] 裡面， x 是主版號， y 是次版號， z 是修訂號。

但因為本網站不是軟體，所以我對於這三個項目的定義有點不一樣，跟「 API 是否相容」無關。

我的定義如下：
- 主版號：表示部落格有了大幅度的改版，例如更換架設方式、網域、部署方式等。以我的技術能力來看，應該很長一段時間都會停在版本 1 。
- 次版號：表示部落格有新增功能，這邊的功能指的是某些特定欄位、頁面、超連結等，讓讀者可以更好使用、閱讀更多內容的都算是新增功能。
- 修訂號：表示部落格既有功能有修改內容，例如 css 樣式的調整、既有頁面或段落的連結調整、或者分類類別的調整等。

以下是依時間倒序排列的 changelogs ，歡迎瀏覽！

---

## [1.6.0] - 2022-04-24

### Added

- 新增了電子報專屬的[「所有電子報歸檔」](/newsletters/archive) 頁面，參考[「所有文章歸檔」](/archive) 的製作方式，依照時序排列發布過的電子報們。

### Changed

- 微調 archive.html ，把[「所有文章歸檔」](/archive)裡面的內容限定在「部落格」的文章，排除掉「電子報」類型的文章。覺得兩者的文體不太一樣，電子報應該可以有自己的歸檔頁面。（微調方式是把 `{% set all_section_pages = get_section(path="_index.md") %}` 改為 `{% set all_section_pages = get_section(path="blog/_index.md") %}` ，另外也把這段往下拉到 {% block main %} 裡面，避免抓到 base.html 的內容。


---

## [1.5.0] - 2022-04-23

### Added

- 嘗試透過 Logseq 內建的 Export graph 功能，建立一個靜態的 wiki 架構網站，並且順利部署在 Netlify 上面，也順利設定了子網域 [https://wiki.pinchlime.com](https://wiki.pinchlime.com) ，之後再來慢慢更新。

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