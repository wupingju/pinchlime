---
title: Keyboard Maestro
description: 
date: 2023-05-15
updated: 2023-05-15
path: library/keyboard_maestro
draft: true
---

## 簡介
Keyboard Maestro 是一個老牌的 Mac 效率工具，可以讓你自訂各種熱鍵組合以及腳本，很難用短短的文字描述他的功能，因此以下舉例說明目前我有哪些腳本：


1. Text snippets ，例如像是 Heptabase 這種比較難打的字，我可以只要輸入 ;hb ，他就會自己跳出 Heptabase 。
2. 輸入當前時間，例如我只要打 ;now 就會馬上變成現在的時間，只要輸入 dte ，就會轉換成當天的日期。
3. 串接多個功能，例如我有一個腳本是，透過 VSCode 打開某個檔案、輸入某個變數，接著他就會把我預設好的格式，帶入我輸入的變數，貼到我指定的位置給我。
4. 幫我轉換格式，例如我有一個腳本是在背景直接取消當前剪貼板的文字的格式，再貼上給我，因此即使這個 app 沒有支援這種操作，還是可以給我無格式的內容。
5. 甚至可以串接 terminal 輸入指令，例如我有一個指令是幫我把圖檔轉換成 webp 格式，我只要按一鍵，輸入圖檔名稱，他就會幫我完成這些操作。
，擴充性幾乎無極限，越用越好用。比方說可以設定text snippets，所以像是DEVONthink這麼難打的字，我可以自己設定像是;dt 這樣的字串，打出來就可以自動產生我要的字。

另外我最常用的功能之一是「只貼上純文字」，因為在複製資訊時常常會連格式一起複製下來，但我要的只有那串字而已，此時可以簡單設定熱鍵，當你按下某組「貼上熱鍵」時，Keyboard Maestro 會自動完成「檢查剪貼板內容-->去除剪貼板相關格式-->貼上到目前的文件」這樣的事情。

以上都只是最基本的使用方式，我還拿它來當作快捷鍵的起動器，搭配各種 app 的 url schemes ，就可以直接進入我想要的頁面或者是資料夾，可以說，只要你想要做的事情，Keyboard Maestro 幾乎都有辦法做到。

---

## 我怎麼使用 Keyboard Maestro ？
