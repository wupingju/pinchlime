---
title: Raycast - 讓你更專注的高效率啟動器
date: 2022-04-02
updated: 2022-04-02
path: 2022/04/02/raycast-introduction/
description: Raycast 在我短短體驗的心得看來，是個更親人、更好入門，但功能卻不打折的超級啟動器，能減少很多繁瑣的流程，讓自己更專注於完成那些想進行的任務。
extra:
  page_type: archive
---

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/raycast_A44cKa.webp" data-fancybox data-caption="raycast">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/raycast_A44cKa.webp" loading="lazy" alt="raycast" align="center" />
</a>

## 為什麼想嘗試 Raycast？

一直以來都很喜歡 [Alfred](https://www.alfredapp.com/) 這個方便好用的啟動器，但最近在好幾個地方都看到有人推薦 [Raycast](https://www.raycast.com/) 這個軟體，有的人甚至說有了 Raycast 後他就不再用 Alfred 了，這就讓我想嘗試看看 Raycast 是否真的那麼厲害。

若不太熟悉 Alfred 的人，可以把它想成 Mac 上面「威力加強版」的 Spotlight ，透過熱鍵啟動後，就會跳出一個簡單的輸入框，在這個輸入框可以輸入關鍵字搜尋自己電腦裡的檔案、可以直接搜尋特定網站、可以串接各種不同的工具、可以直接輸入指令執行更多複雜操作。

而 Raycast 在我短短體驗的心得看來，是個更親人、更好入門，但功能卻不打折的超級啟動器，能減少很多繁瑣的流程，讓自己更專注於完成那些想進行的任務。

<!-- more -->

## Raycast 介面簡介

在官網安裝 Raycast 後，會有簡單的教學引導，並且設定熱鍵，在這邊我建議可以先設定成為 Option + Space 之類的按鍵，若熟悉後真的覺得比 Spotlight 讚，就可以到 Mac 內建的設定把 Spotlight 關掉，並且把 Raycast 設定為 Command + Space。

一開始打開 Raycast 後，如果從來沒用過這類軟體，可能會被一堆指令嚇到，反而不知道可以幹嘛、該幹嘛，就被嚇跑了，所以我建議直接先打開偏好設定（Command + ,）（或點選 menubar 的圖示選 Preferences），接著你會看到一個簡單的設定介面，在 General 分頁可以設定啟動快捷鍵，而主要的功能設定都在 Extensions 分頁，如下圖。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/raycast-extensions_rcrvLB.webp" data-fancybox data-caption="raycast-extensions">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/raycast-extensions_rcrvLB.webp" loading="lazy" alt="raycast-extensions" align="center" />
</a>

在這邊簡單介紹一下裡面每一欄的意思，第一欄 Name 指的是某一類型的指令（Command）、擴充功能（Extension）或者群組（Group），而重點的設定在第三欄的 Alias 以及第四欄的 Hotkey。第五欄的 Enabled 則是可以勾選「要不要開啟這項功能」。

**Alias** 可以理解成為「啟動快捷字」，例如，我把 “Define Word” 查字典這項功能的快捷字設定為 de ，此時我只要打開 Raycast 並輸入 de ，它就會自動啟動這個功能，我就可以在後面輸入我要查詢的單字。

而 **Hotkey** 則是一個全系統的快捷鍵，同樣以查字典為例，假設我把它設定為 Control + Command + D ，那麼我在任何介面輸入這組快捷鍵時，就會自動跳出 Raycast 查單字的介面，此時我也可以迅速輸入單字來查找。

所以說，有些類型的功能可以用 Alias 來啟動，有些則是可以用 Hotkey ，我覺得偏向「搜尋」類型的都可以用 Alias ，這樣不用紀錄太多熱鍵，而偏向「系統功能」類型的可以用 Hotkey ，因為最快最直接，久了以後會直接形成肌肉記憶，增加使用 Mac 的效率。

另外，我很建議一開始使用 Raycast 可以**先把自己「看不懂」的功能全部都關閉**（在 Enabled 欄位取消勾選），這是因為這些東西即使你不小心在 Raycast 裡面搜尋到了，也不會用、不敢用，反而會覺得很複雜，此時不如先用最基本的功能，再慢慢嘗試自己有興趣的項目，上手會更順利。

## 我怎麼使用 Raycast？

Raycast 的功能一篇文章絕對說不完，因為它有豐富的擴充功能市場，從 Extensions 介面點選那個＋號就可以進去瀏覽。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/raycast-extensions-store_4JjW52.webp" data-fancybox data-caption="raycast-extensions-store">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/raycast-extensions-store_4JjW52.webp" loading="lazy" alt="raycast-extensions-store" align="center" />
</a>

而除了擴充功能外，內建的也已經足夠強大，對我來說可能可以分成「可以替代 Spotlight 的功能」以及「可以替代其他效率工具的功能」兩種類型。

### 可以替代 Spotlight 的功能

- 應用程式快捷啟動
- 檔案搜尋
- 字典查詢
- 計算機

這些功能如果有在用 Spotlight 應該不陌生，但是 Raycast 的體驗更好一些，以應用程式搜尋來說，可以用勾選的方式排除掉那些「不想搜到」的應用程式，也可以直接設定 alias 或 hotkey 來讓搜尋啟動更有效率。

而以檔案搜尋來說，搜到檔案後也可以按 command + K 開啟更多指令，例如 Show in Finder / Open With 等等，讓檔案的「使用」更流暢。

最令我驚豔的應該是計算機的功能，除了基本的計算之外，也可以做到即時的匯率換算，像是只要輸入 1 usd in twd ，就會馬上回給我目前的匯率 28.68 ，這部分除了法幣外，也可以換算比特幣或以太幣等密碼資產。除此之外，計算機還可以用 “today + 4 days” 這樣的語法去算出簡單的日期，或者換算不同時區的時間。

### 可以替代其他效率工具的功能

**系統管理與視窗管理**

在 System 項目裡面，可以幫各種常用的系統功能設置快捷鍵，例如離開座位不想被同事看螢幕的 “Lock Screen” 功能，或者是想找一下桌面資料的 “Show Desktop” 功能，或者想專注在眼前視窗，就可以選擇 “Hide All Apps Except Frontmost” 把其他視窗都隱藏起來。

而在 Windows Management 的項目裡面， Raycast 就內建了二三十種不同的視窗管理選項，以我來說我就設定了下圖這些：

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/raycast-windows-management_NNkiKe.webp" data-fancybox data-caption="raycast-windows-management">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/raycast-windows-management_NNkiKe.webp" loading="lazy" alt="raycast-windows-management" align="center" />
</a>

這個意思是比如說，我只要按下 Option + 上，就能迅速將目前的視窗擴展到整個螢幕的大小，按下特定快捷鍵，就可以將視窗設定為左右對半、左右三分之二、左右三分之一、或者是將螢幕切成四格。

這種快捷的視窗管理，只要嘗試過後就絕對回不去，我最常見的使用情境就是把瀏覽器放在左半邊或左三分之二，然後把筆記軟體放在右半邊或右三分之一，對照著記筆記。如果螢幕夠大（27吋以上），也很推薦分成三等份來使用。

我原先是透過 BetterTouchTools 來進行視窗管理，但現在覺得整合在 Raycast 一起使用就好了。

**剪貼簿與快捷字串（snippets）管理**

在 Raycast 裡面也可以存取系統的剪貼紀錄，或者是設定特定快捷字串，例如最常用的可能是把自己的 email 或者實體地址設定一個啟動字串，例如 ;@ ，只要輸入這兩個字母，就會自動貼上你設定好的文字。

對某些比較輕度使用的人來說， Raycast 這樣的功能就很夠了，不用再使用更專業的剪貼簿管理軟體或者快捷字串管理軟體。

**與其他服務的串接**

在 Raycast 官網的介紹裡，這應該是強項，例如串接 Github, Asana, Jira, Linear, Zoom 等等，我不是工程師，所以目前沒有用到這些串接，但我在擴充功能市場裡面有找到我常用的 Raindrop ，簡單設定好後，就可以快速查找我書籤庫裡面的書籤了（目前還無法「添加」）。

其他還有看到像是 Spotify, Slack, Notion 等各種服務的串接，基本上只要有開放 API 的應該都可以在 Raycast 建立擴充功能。

有興趣逛逛的人，可以到 [Raycast 官網的 Store 頁面](https://www.raycast.com/store)瀏覽！

## Raycast 要付費嗎？

介紹了這麼多，本文最重要的資訊是， Raycast 目前是可以免費使用的，而且基本上是全功能無限制使用。

對，從官網的 [Pricing 頁面](https://www.raycast.com/pricing)可以看到， Raycast 目前規劃的付費功能只會限定在團隊版本，比個人版本多出了一些共享連結、共享 snippets 或共享擴充功能的功能，但如果是自己要使用的話，目前來看是一切免費，真的是相當佛。

所以如果之前沒有用過任何付費的效率工具（如 Alfred / Keyboard Maestro / BetterTouchTool ），那麼 Raycast 非常適合作為入門的第一款。

## 小結

對我來說， Raycast 可以提供的功能大多都能在其他工具上面找得到，但它的整體介面比起那些功能強大的操作工具，還要簡潔明快一些，也很容易設定，所以應該更有機會推廣給從來沒接觸過這些工具的新朋友。

只要謹記，一開始進去以後，不要被一堆功能嚇跑，先關掉大部分功能，慢慢找自己有興趣的功能來用，越用越習慣後就能更上手了。

而上手後，可能也更能夠體會「好的效率工具能讓自己專注於任務本身」這樣的境界吧！
