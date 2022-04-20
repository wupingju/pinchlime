---
title: Pin 起來的 Changelog
path: changelog/
draft: false
date: 2022-04-20
updated: 2022-04-20
---

這邊放置 Pin 起來網站的 changelog。

跟[所有文章歸檔](/archive/)不同的地方在於， changelog 主要是講「這個網站」本身的變化，無論是新增、調整、或刪除，都會盡量放在這邊。

---


## [1.2.0] - 2022-04-20

### Added

- 開始更新 Pin 起來的 Changelog 頁面。

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