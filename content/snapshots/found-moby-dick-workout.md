---
title: Moby Dick Workout
date: 2022-05-22
description: Moby Dick 是白鯨記，而 Grossjean 這個測試方法，就是拿白鯨記的完整文字檔，來測試筆記軟體或文字編輯器的效能。
path: snapshots/what-i-found-interesting/moby-dick-workout
taxonomies:
  kinds: 
    - What I Found Interesting
  tags: 
    - Bike
    - Logseq
    - Testing
---

這是推友推薦，在 Bike 的作者 Jesse Grosjean 的網站上[看到的文章](https://www.hogbaysoftware.com/posts/moby-dick-workout/)，或者說一種測試方法，覺得非常有趣。

Moby Dick 是白鯨記，而 Grossjean 這個測試方法，就是拿白鯨記的完整文字檔，來測試筆記軟體或文字編輯器的效能。

具體的測試方法是，透過想測試的軟體打開或 import Moby Dick 檔案（有分 opml 格式以及 .md 格式），然後測試看看下列動作：
1. 打開它，快嗎？
2. 滾動到底部，調整視窗大小，快嗎？
3. 再滾動到中段，調整視窗大小，快嗎？
4. 全選文字，剪下、貼上、undo、redo，你的 app 還行嗎？
5. 在文章中段編輯一些內容，是否會 lag？是否會卡頓？
6. 重複測試步驟 2-5 直到你滿意為止，然後打開 macOS 的 Activity Monitor，看看記憶體的用量你是否滿意。

我嘗試用這個方法測試了 Logseq ，發現，效能不太好。

而 Bike 的效能則是非常好，運行這一些動作都很滑順流暢。這也是最後決定實際用用看 Bike 的原因之一，速度快，真的是很大的優點。