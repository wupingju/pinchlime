---
title: 測試 Heptabase Journal 的「拖曳到白板」功能
date: 2022-06-08
updated: 2022-06-08
description: 整體來說，我很喜歡這次的小更新，設計上很直覺也合理，期待後續有更多隨之產生的 workflow
path: snapshots/what-i-tried-today/tested-heptabase-journal-dragging-to-whiteboard
draft: false
taxonomies:
  kinds: 
    - What I Tried Today
  tags: 
    - Heptabase
    - Journal
---

* 今天 v0.152.0， Journal 功能的內測更新，提高了 dragging to whiteboard 體驗。

* 具體來說，目前的實踐方式有兩種：

  * 假設在 Journal 編輯器上，透過 @ 或 \[\[ 建立卡片，或連結某張卡片。那麼我會得到的結果是，這個編輯器介面上的 block ，本身就是一個卡片的連結，此時將這個 block 拖曳到白板上時，得到的體驗是我期待的結果，就是顯示在白板上的卡片對應到的就是 journal 裡的這個項目，且在白板會自動展開，也會顯示 journal 對應的日期資訊在 Card Info 裡面。

  * 直接將某個文字 block 以及底下的列表文字拖曳到白板上，此時在 journal 中原本的列表文字會收起，而白板上則會呈現展開的內容。我覺得這是很有趣的設計，有點像是 journal 速記完以後，他在 journal 上的意義就是一個帶有時間序的「項目」。但白板上則是重新展開的內容。

* 整體來說，我很喜歡這次的小更新，設計上很直覺也合理，期待後續有更多隨之產生的 workflow 。