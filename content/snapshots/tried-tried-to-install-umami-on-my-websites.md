---
title: 嘗試安裝 umami 成功
date: 2022-06-19
description: 完成後所有數據都可以很直觀地透過 umami 看到，現在我對它非常滿意！如果過一個禮拜沒什麼大問題，應該就會把 Google Analytics 的追蹤碼移除了！
path: snapshots/what-i-tried-today/tried-to-install-umami-on-my-websites
taxonomies:
  kinds: 
    - What I Tried Today
  tags: 
    - Umami
    - Google Analytics
---

因為稍早[嘗試安裝 Cusdis 但失敗](@/snapshots/tried-tried-to-install-cusdis-but-failed.md)，想說一鼓作氣再來試試另一個之前[曾提過的 umami](@/snapshots/why-why-do-i-want-to-try-umami.md)。

這次參考的是 [搭建 umami 收集个人网站统计数据 | Reorx’s Forge](https://reorx.com/blog/deploy-umami-for-personal-website/) 這篇文章，架設過程蠻順利的，基本上是完全照著 Reorx 提供的步驟做就成功了，只有幾個地方與原文稍有不同（或需要補充）：

1. 原文寫的 brew install libpg 應該是 brew install libpq 才對（不是 g, 是 q）

2. 原文所說的「完成后，将 libpg 的 bin 路径添加到 PATH 中，在 .zshrc 或 .bashrc 中添加一行:」這段我本來看不太懂，搜尋一下才知道 .zshrc 跟 .bashrc 大概是什麼，後來我直接在 /home 底下建立了這兩個文件，並且添加那串 libpq 的路徑代碼，才順利完成。

3. 我沒有像 Reorx 一樣修改腳本的名稱，避免被 ublock 擋住。（我覺得如果真的被擋住那也沒差。）

4. 最後，我是透過 Netlify 的 [Snippet Injection 功能](https://docs.netlify.com/site-deploys/post-processing/snippet-injection/)來放置 umami 的代碼，我非常喜歡這個功能，快速好用，相當推薦。

整個過程對不熟悉任何資料庫或部署的我來說，大概花了一個小時完成，完成後所有數據都可以很直觀地透過 umami 看到，現在我對它非常滿意！如果過一個禮拜沒什麼大問題，應該就會把 Google Analytics 的追蹤碼移除了！

