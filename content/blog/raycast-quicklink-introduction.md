---
title: 透過 Raycast 的 Quicklink 迅速連動 Drafts
date: 2022-04-04
path: 2022/04/04/raycast-quicklink-introduction/
description: Quicklink 的功能並不限於搜尋網站而已，而是可以用來處理各種能透過 URL scheme 運作的工具。
taxonomies:
  categories: 
    - Tools
  tags: 
    - Raycast
    - Drafts
    - Workflows
---

今天要繼續來分享一下，前幾天 [初次介紹 Raycast](@/blog/raycast-introduction.md) 時沒有特別留意＆著墨的功能 Quicklink。

先前情提要一下，我原先主要是透過 Apple notes 紀錄我的工時 （[關於紀錄工時的好處請看這篇](https://pinchlime.substack.com/p/record-your-work-hours?s=w)），用法很簡單，就是每天開啟一則 note ，然後做完什麼事就記上去對應的時間跟事情，例如「0930–0945 安排今日待辦工作」。

不過近期覺得 Apple notes 太不穩定（容易當掉且同步會失敗），決定還是透過自己更熟悉的 [Drafts](https://getdrafts.com/) 來紀錄我的每日工作時間。 本來打算透過 Keyboard Maestro 搭配 Drafts 的 [URL Schemes](https://docs.getdrafts.com/docs/automation/urlschemes) 來快速紀錄，但轉念一想，現在我已經開始用 Raycast 了，為何不試試看？

因此簡單摸索了一下 Raycast ，就發現裡面 Quicklinks 這個功能相當好玩。


<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/raycast-quicklink_vNO8bi.webp" data-fancybox data-caption="raycast-quicklink">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/raycast-quicklink_vNO8bi.webp" loading="lazy" width="622" height="878" alt="raycast-quicklink" align="center" />
</a>

<!-- more -->
---

## Quicklink 可以做什麼？

這個功能乍看之下，是可以預設好要搜尋的網站（例如下圖是預設在 Google 搜尋），此時自己在 Raycast 輸入的字串就會跑到 {Query} 這個位置中，進而可以直接取得搜尋後的內容。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/raycast-google-query_9thLA0.webp" data-fancybox data-caption="raycast-quicklink">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/raycast-google-query_9thLA0.webp" width="768" height="471" alt="raycast-quicklink" align="center" />
</a>

例如我將 Google 搜尋的 quicklink 設定關鍵字為 “gg” ，所以當我在 Raycast 輸入 gg 時，就會跑出一個 [Query] 的格子（如下圖）。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/raycast-query-preset_duWafL.webp" data-fancybox data-caption="raycast-quicklink">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/raycast-query-preset_duWafL.webp" width="768" height="390" alt="raycast-quicklink" align="center" />
</a>

假設我在這邊輸入 Pin 起來，並按下 enter 送出，那麼 Raycast 就會在我設定的瀏覽器，幫我到 Google ，搜尋「Pin 起來」。

但我測試了一下就發現，這個 Quicklink 的功能並不限於搜尋網站而已，而是可以用來處理各種能透過 URL scheme 運作的工具。

---

## Drafts 的 URL schemes

這邊先暫且跳過 URL schemes 的介紹，直接拿本文要講的 Drafts 來舉例好了，我在 Raycast 新增了一個 Quicklink ，網址（Link）的地方直接填入 [Drafts 規定的格式](https://docs.getdrafts.com/docs/automation/urlschemes#append)。

例如「append」是：

```
drafts://x-callback-url/append?uuid=UUID-TO-VALID-DRAFT&text=TEXT-TO-ADD
```

這段看似亂碼的 URL 概念是說，在「UUID-TO-VALID-DRAFT」這邊替換成特定 draft 的 UUID （可以在 drafts 裡面按右鍵檢視並複製），然後「TEXT-TO-ADD」這段字則是「你要加入的字」。

所以假設我某則 Draft 的 UUID 是 12345678 ，而我輸入了

```
drafts://x-callback-url/append?uuid=12345678&text=媽我在這 
```

那麼輸入後，在我這則 Draft 的最後一行就會馬上出現「媽我在這」 這幾個字。

---

## Quicklink 搭配 Drafts

聰明的你一定想到了，假設我把這段 URL 加入 Raycast 的 Quicklink ，但把「TEXT-TO-ADD」這邊替換成 {Query} ，那就變成我在 Raycast 輸入這個 quicklink 的快捷指令後，再輸入我想要紀錄的東西，就會自動把這個東西傳送到該則特定的 draft 裡面。

所以以我原先想要達成的「紀錄工時」這件事來說，我不用再點開 Apple note 並且點擊到該則筆記的尾端，輸入我剛剛做的事情，我只要呼叫 Raycast ，並且輸入我指定的啟動字串（dl），再填入我要速記的工時紀錄，就會直接幫我把這串文字記到那則 draft 了。

繼續延伸的話，只要能取用 URL scheme 的工具，例如 Obsidian, DEVONthink, OmniFocus, Fantastical 等等，應該都可以透過 Raycast 的 quicklink 來跳轉、添加以及搜尋吧！
