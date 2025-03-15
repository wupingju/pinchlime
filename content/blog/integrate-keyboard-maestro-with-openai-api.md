---
title: 在任何輸入框都可以一鍵翻譯：我用 Keyboard Maestro 搭配 OpenAI API 做的腳本
date: 2025-03-04
updated: 2025-03-04
path: blog/integrate-keyboard-maestro-with-openai-api
description: 這篇想簡單介紹昨天我跟 Claude 協作的一個小工具，準確來說是一個 Keyboard Maestro 的腳本，它的用處是可以在 Mac 任何可以複製貼上文字的輸入框，都能呼叫 OpenAI 的 API ，根據你設定好的 prompt 去處理文字。
taxonomies:
  categories: 
    - Tools
extra:
  page_type: blog
---


這篇想簡單介紹昨天我跟 Claude 協作的一個小工具，準確來說是一個 [Keyboard Maestro](https://www.keyboardmaestro.com/main/) 的腳本，它的用處是可以在 Mac 任何可以複製貼上文字的輸入框，都能呼叫 OpenAI 的 API ，根據你設定好的 prompt 去處理文字。

簡單的範例請參考我的 [Twitter 貼文](https://x.com/WuPingJu/status/1896704678119006467)或 [Threads 貼文](https://www.threads.net/@wu_pingju/post/DGwXcfHSKIr?xmt=AQGzBFj0AS-ExZqkOb3qFCF8NoidOnQPTv7BYmcVZ4LGpw)。

---

## Keyboard Maestro 是什麼？

Keyboard Maestro 是一個 Mac 上的老牌工具，他裡面有非常多可以自定義的 “Actions” ，然後你可以像是堆積木一樣把這些 Actions 組合在一起，再透過你想要的方式去觸發這些 Actions。這些包含觸發條件與 Actions 的組合，在 Keyboard Maestro 裡面叫做 “Macro” ，我都叫他「腳本」。

舉例來說，除了本文要介紹的之外，我最常用的腳本有下列這幾個：

- 輸入 hhh ，就會自動轉換為 Heptabase （還有類似的數十個 snippets）
- 按下 Cmd + F2 ，就會觸發 Todoist 的熱鍵，讓我記錄新的任務
- 按下 Cmd + F5 ，就會為我打開 Finder 中的截圖資料夾，讓我可以馬上到我想要的位置去找東西。

在這邊就不多介紹 Keyboard Maestro 可以怎麼用，網路上有非常多的資料與範例，歡迎有興趣的人自己參考研究。

---

## 一鍵翻譯文字的腳本介紹

你可以到這個 Google Drive 的[連結](https://drive.google.com/file/d/1OBmoUWui3eUXDMX5cUbnmHNEpNu3Fcrp/view?usp=sharing)下載這個腳本。假設你已經安裝了 Keyboard Maestro，你可以直接執行這個檔案，它就會直接導入到你的 Keyboard Maestro 裡面。

以下分成幾張截圖分別介紹這個腳本，裡面紅色的區塊是我建議跟我一樣的程式小白不要亂動的地方，黃色的區塊要請你自行填入資訊，而綠色的區塊則是你可以根據自己的需求去研究設定，當然也可以維持原狀就好。

---

第一張圖：

1. 可以改 Macro 名字與圖示。
2. 可以更改觸發的熱鍵，除了按鍵以外也有其他觸發方式，歡迎自行研究。
3. 這邊的意思是：腳本會幫你按下 Cmd + C （複製），並且等 0.2 秒，然後把複製到的內容，設定為 `to_translate` 這個變數的內容。

備註：所以在實際使用時，要先框選你要處理的文字，再按下熱鍵，這樣腳本按下複製時才能複製到東西。

<br>
<a href="https://image-webp.pinchlime.com/CleanShot%202025-03-04%20at%2019.13.17@2x_DToRWf.png" data-fancybox data-caption="integrate-keyboard-maestro-with-openai-api-1">
  <img src="https://image-webp.pinchlime.com/CleanShot%202025-03-04%20at%2019.13.17@2x_DToRWf.png" loading="lazy" alt="integrate-keyboard-maestro-with-openai-api-1" align="center" />
</a>

---

第二張圖：

1. 請在這邊填入你的 OpenAI API key，如果不清楚這是什麼，歡迎先上網找教學！
2. 請在這邊輸入你想使用的模型，[這邊可以看到目前有的模型](https://platform.openai.com/docs/models)，如果是嘗試使用，我推薦先用 gpt-4o-mini ，因為很便宜！
3. 請輸入你想要這個助手做的事情在 System Prompt 裡面，如果你沒有想法只是想翻譯看看，你可以先隨意輸入類似這樣的文字：You are an expert in English and fluent in Mandarin. You will translate user input to English while maintaining the original meaning accurately. 

這樣做的效果，就是會把你框選的文字翻譯成英文。（你當然也可以反過來改寫成翻譯為中文，或者是其他用途。）


<br>
<a href="https://image-webp.pinchlime.com/CleanShot%202025-03-04%20at%2019.20.57@2x_r0hwwP.png" data-fancybox data-caption="integrate-keyboard-maestro-with-openai-api-2">
  <img src="https://image-webp.pinchlime.com/CleanShot%202025-03-04%20at%2019.20.57@2x_r0hwwP.png" loading="lazy" alt="integrate-keyboard-maestro-with-openai-api-2" align="center" />
</a>

---

第三張圖

1. 第一格是我請 Claude 幫我規劃的 Shell Script ，他在做的事情大概是這樣：
   - 先引用你在前面填入的 API 與 System Prompt 資訊、以及導入你複製的內容（要給 OpenAI 處理的內容）
   - 後續再實際送出 API 請求給 OpenAI ，然後從 OpenAI 回傳的內容裡面截取出你唯一需要的部分。
   如果你有更好的寫法，歡迎跟我分享！如果你跟我一樣什麼都不懂，應該就不需要去動它，或者你也可以複製一個 Macro 然後自己找 AI 一起改成你想要的樣子。

2. 這邊的意思是執行完後等個 0.5 秒，比較不會因為時間差導致無法正確產出成果。歡迎根據你的測試自行調整。
3. 這邊的意思是「用貼上的方式」插入「這個框框裡面的文字」，而「這個框框裡面的文字」就會是第一步驟的 Script 裡面產出的內容。 Keyboard Maestro 提供了各種可能性，這邊是用貼上，也可以選成用模擬打字的，或者是直接用 “Display Text” 這個 Action 跳出一個框框顯示 OpenAI 回傳的文字。歡迎自己玩！


<br>
<a href="https://image-webp.pinchlime.com/CleanShot%202025-03-04%20at%2019.24.49@2x_kaZlvQ.png" data-fancybox data-caption="integrate-keyboard-maestro-with-openai-api-3">
  <img src="https://image-webp.pinchlime.com/CleanShot%202025-03-04%20at%2019.24.49@2x_kaZlvQ.png" loading="lazy" alt="integrate-keyboard-maestro-with-openai-api-3" align="center" />
</a>

---

基本上，只要你設定了黃色的三個區塊，就可以在某個可以打字的地方，選一段中文文字，然後按熱鍵執行看看，成功的話就會翻譯成英文了。

接著，你可以再繼續根據你的需要微調修改，可以改 prompt 讓他效果更好，也可以測試不同模型的做法。我覺得以翻譯來說，用 gpt-4o 是可以兼顧品質跟成本的好選擇。

如果你有其他更厲害的做法，歡迎跟我分享你的成果！