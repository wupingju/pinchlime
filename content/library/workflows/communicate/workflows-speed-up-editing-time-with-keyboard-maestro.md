---
title: 利用 Keyboard Maestro 加快 PO 文的速度
date: 2023-01-09
updated: 2023-01-09
description: 整個流程包含輸入，大概只要花不到 30 秒，我只要再把我在 Heptabase 寫好的文字貼上、做些簡單編輯就好
path: blog/workflows/speed-up-editing-time-with-keyboard-maestro
taxonomies:
  tags: 
    - Keyboard Maestro
    - Zola
---

這兩天又開始玩起了 Keyboard Maestro ，除了重新設定一些快速啟動鍵之外，也想來把「建立一篇部落格文章」的流程更加速一些。

在開始使用 Zola 架站後，我變成只要靠一個 Repository（倉庫）就可以管理我所有的 PO 文，但每次要 PO 文前，還是要經過一些繁瑣的小程序，包含：

- 建立一個 markdown 檔案
- 為這個檔案命名，並且要遵守我自訂的命名規則前綴
- 開啟檔案，編輯文件的 front matter 區域，也就是 metadata 等資訊，包含標題、描述、日期、路徑、分類等等

也因為我的分類有大概 10 來種，每次設定完這些東西，大概都要花個 3-5 分鐘，稍微有點麻煩。

但我一直都知道，這種事情最適合交給 Keyboard Maestro 來做了，因此我設定了兩個 Macro，在執行前都會先讓我輸入基本的 title、選 po 文類別、並且填上 slug，但我只要做這些事，它就會自動為我執行下列步驟：

- 在指定的資料夾路徑，創建我指定命名的 markdown 檔案
- 在這個檔案上面，自動依據我前面選擇的類別與 slug，填入基礎的 metadata 資訊到 front matter 區域。

整個流程包含輸入，大概只要花不到 30 秒，我只要再把我在 Heptabase 寫好的文字貼上、做些簡單編輯就好！

這篇短短的 workflow 是第一則利用這個 macro 創立的貼文！
