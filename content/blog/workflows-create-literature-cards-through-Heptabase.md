---
title: 透過 Heptabase 製作閱讀筆記卡片
date: 2022-06-03
updated: 2022-06-25
description: 我透過 Heptabase 製作閱讀卡片的方式
path: blog/workflows/create-literature-cards-through-Heptabase
taxonomies:
  categories: 
    - Workflows
  tags: 
    - Heptabase
---

我會在 Heptabase 裡面針對已經透過「[我的閱讀、畫線與註記工作流](@/blog/workflows-my-highlighting-and-annotating-workflow.md)」初步處理過的文章，視重要程度，在 Heptabase 裡面開設文獻卡片，命名格式為「articles.文章名稱」

建立卡片後，透過 Keyboard Maestro 直接加入固定的 template 。內容包含三個區塊：
* metadata：包含作者、文章發布日、閱讀日
* 註解區：包含 Quotes,  Highlights, Annotations，並 [透過Heptabase進行漸進式總結](@/blog/workflows-doing-progressive-summarization-through-heptabase.md)
* 筆記區：包含使用 「[我撰寫Literature-notes的方式](@/blog/workflows-how-i-make-literature-notes.md)」 這個方法撰寫的筆記
*  References：包含文章連結、Link from（從哪些地方讀到連到這篇文）、Link to （連到哪些筆記）

在製作閱讀筆記卡片的時候，特別需要注意的是把自己的想法寫下來，形成一則一則的原子筆記。此時我會再把他們列在下方的 “Link to” 區塊，後續即可將這些想法擴寫成自己的 random thoughts 或 evergreen 筆記了。

透過這整個流程，我在「閱讀筆記卡片」裡面，會保有一篇文章的畫線紀錄、我的註解內容，也可以連結到基於這篇文章產生的不同想法，留給未來的自己參考的依據。
