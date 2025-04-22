---
title: 我目前會用 AI 做的事，與不會用 AI 做的事
date: 2025-04-22
path: blog/do-and-dont-with-ai
description: 我預期隨著 AI 功能愈來愈強，會用 AI 做的事也會愈來愈多。但我也認為，即使 AI 變得再強，有些事我還是不會用 AI 來完成。
taxonomies:
  categories: 
    - Tools
extra:
  page_type: blog
---

> 這篇文章會持續更新，紀錄我現在會用 AI 做的事以及不會用 AI 做的事。我預期隨著 AI 功能愈來愈強，會用 AI 做的事也會愈來愈多。但我也認為，即使 AI 變得再強，有些事我還是不會用 AI 來完成。

---

## 我目前會用 AI 做的事

### 翻譯 - 中翻英

`使用工具：OpenAI API + Keyboard Maestro`

我在日常生活與工作中大量使用 AI 協助我翻譯，這件事對我來說非常有價值，因為他大幅縮短了我閱讀外語資訊需要的時間與精力。

我最常用的翻譯方式有兩種，第一種是在使用英文溝通時中翻英，使用的方式可以參考「[在任何輸入框都可以一鍵翻譯：我用 Keyboard Maestro 搭配 OpenAI API 做的腳本](@/blog/integrate-keyboard-maestro-with-openai-api.md)」這篇文，目前使用的模型是 gpt-4.1。

我很常用俗稱「晶晶體」的中英交雜方式輸入我想講的話，然後再透過這個工具翻譯為英文，這樣做的好處是我可以大幅保留我想要留下的正確脈絡文字，把其他比較不熟悉的文法或用字交給 AI 處理。

例如，假設上面那段話我想要確認「保留」跟「脈絡」要使用 "preserve" 跟 "context" ，我就會直接把這段話交給 AI 翻譯：「我很常用俗稱「晶晶體」的中英交雜方式輸入我想講的話，然後再透過這個工具翻譯為英文，這樣做的好處是我可以大幅 preserve 我想要留下的正確 context 文字，把其他比較不熟悉的文法或用字交給 AI 處理。」

翻譯出來的結果是：I often use a mix of Chinese and English, commonly known as "JingJing-ti," to input what I want to say. Then I use this tool to translate it into English. The advantage of this method is that I can greatly preserve the context I want to keep, while letting the AI handle the grammar and words I'm less familiar with.

---

### 翻譯 - 英翻中

`使用工具：沉浸式翻譯`

在工作上，或者是工作外的閱讀時間，假設我看到大量英文內容，我也會先透過上述工具翻譯為中文快速預覽。假設是比較長篇的內容，我則會透過[沉浸式翻譯](https://immersivetranslate.com/en/)這個瀏覽器的延伸程式翻譯全文。安裝後我只要按下快捷鍵或者是瀏覽器側邊的按鈕，就會馬上把當前的頁面翻譯完畢，而且翻譯的內容是一段一段，原文與中文交雜的版本，例如下圖這篇來自 OpenAI 的 [Reasoning best practices](https://platform.openai.com/docs/guides/reasoning-best-practices#reasoning-models-vs-gpt-models) 範例。

<br>
<a href="https://image-webp.pinchlime.com/immersive-translate_7SxNsa.png" data-fancybox data-caption="Immersive-translate">
  <img src="https://image-webp.pinchlime.com/immersive-translate_7SxNsa.png" loading="lazy" alt="Immersive-translate" align="center" />
</a>
<br>

我覺得這種逐段翻譯呈現的體驗非常好，因為他滿足我兩個需求：
1. 能夠透過中文快速掌握原文想講的內容
2. 假設有我感興趣的段落，再仔細閱讀英文

即使快速翻譯的內容比較不精準，但我閱讀中文的速度還是比英文快非常多。沉浸式翻譯大幅增加了我閱讀的效率，真的是很棒的工具。

我有訂閱沉浸式翻譯的付費版本，基本上可以無限制使用翻譯（還是有每月使用上限，但我從來沒碰過上限），如果你也想訂閱沉浸式翻譯的 Pro 版本，輸入折扣碼 PJWU 可以享有 95 折優惠！


---

### 推理（Reasoning） - 分段產製卡片標題

`使用工具：ChatGPT Plus`

我透過 ChatGPT 的 Projects 功能做了一個「卡片標題產生器」，他的用法是，當我貼上一段文章的文字，他會把這些內容分拆，然後逐段提供適合的卡片標題給我。整體用起來的感覺有點像是 Heptabase 的 insight generator，但由於我可以自訂 prompt ，也可以在 projects 裡面使用更進階的模型，所以我更喜歡用這個助手。

當我得到這些分段的標題，我就可以快速判斷我是否要閱讀這段內容。若閱讀完後覺得內容確實很有價值，我就會再把內容製作成 Heptabase 裡面的卡片。

<br>
<a href="https://image-webp.pinchlime.com/atomic-card-generator_ErKYah.png" data-fancybox data-caption="Atomic-card-generator">
  <img src="https://image-webp.pinchlime.com/atomic-card-generator_ErKYah.png" loading="lazy" alt="Atomic-card-generator" align="center" />
</a>
<br>

我從 o1 就開始這樣做，現在在 OpenAI 推出 o3 模型以後效果更好。我選擇用 o 系列推理模型的原因是，我要求他自行判斷該怎麼分拆文字，而不是依照固定字數或段落區分，我認為這涉及到一定的推理能力需求，所以 o 系列的表現會比 4o 或 4.1 更好。

--- 

### 推理（Reasoning） - 討論方案

`使用工具：ChatGPT Plus`

假設我需要決定某件事，而且是我沒有把握的事，我可能會找 ChatGPT 討論。我會簡單描述這件事的前情提要、我目前的想法、我期待得到的結果（可能是建議或者是提醒）。

我還沒有每件事都找 ChatGPT 問，也不會完全採用他的方案，但這種多一個人可以討論的感覺還挺不錯的。

在 o3 模型推出後，他閱讀圖片的能力更好了，因此我有時會直接把我要問的脈絡截圖丟給他，然後再問我想問的問題。


---

### 深度研究（Deep research）

`使用工具：ChatGPT Plus`

我非常喜歡 ChatGPT 的深度研究功能，雖然我使用的頻率並不高，但是那種「我想用的時候就可以馬上用」的感覺非常好。

我曾寫過幾篇關於 Deep research 的心得，歡迎參考：
- [讓我開始思考未來的 ChatGPT o1 Pro & Deep research](@/letters/34-o1-pro-and-deep-research-first-impression.md)
- [有了 Deep Research 後，我還需要 Heptabase 嗎？當然要，更需要了！](@/letters/35-i-still-need-heptabase.md)
- [分享一個 ChatGPT Deep Research 搭配 o1 Pro 搭配 Heptabase 的工作流](@/letters/36-a-deep-research-o1-pro-heptabase-workflow.md)


---

### 寫簡單的程式

`使用工具：ChatGPT Plus & Claude Pro`

假設我想要改部落格的樣式、增加一些小功能，我就會找 Claude 與 ChatGPT 一起討論作法。我也有找他們問過 Google Sheets 的函式和 App Script，不過我的使用頻率並不高，大約一個月一兩次而已。

我目前沒有在使用 Cursor, Windsurf 或者是 Github Copilot 這些工具。


---

## 我目前還不會用 AI 做的事

### 寫作

這邊指的寫作是指寫部落格文章、寫信、寫社群的貼文。我曾經嘗試過幾次讓 AI 彙整我給的一些卡片或摘要，請他寫出一篇文章，但每次我都覺得「那不是我的文字」，所以就作罷。

但我對這件事慢慢轉向開放態度，假設我真的能夠訓練出非常像我的 AI ，也許我會開始嘗試與他一起寫作。

---

### 建立論述、說服別人

若我自己有一些疑惑，我可能會與 AI 討論，但如果是別人的疑惑，或者是別人與我意見不一致，我不會拿 AI 的答案要求別人接受。

因為我知道目前使用者輸入的內容會大幅影響生成式 AI 的回覆內容，假設我詢問「某件事情是否正確」，通常 AI 會偏向回覆「能證明這件事正確」的內容。反過來說，另一方只要詢問「某件事是否錯誤」，AI 也可以給出很多支持錯誤的內容。

加上生成式 AI 仍無法避免幻覺，假設我無法確保一件事是我完全理解並正確的，我就無法拿來說服別人，但假設我自己已經很理解，也有信心是正確的，那麼我也能夠很快說明清楚，這時也不需要 AI 的協助。

---

### 聊天或討論心事

我好像從來沒有想要跟 AI 討論心事，一方面是因為知道他就是基於我的「分享」來「算出」最適合給我的回覆，換句話說他根本不理解內容，只是變出文字而已。另一方面是我已經很習慣記下我的想法或心情，並藉由打字的過程簡單自我對話。再另一方面是因為我沒有太多煩惱或心事，所以我仔細想了一下，好像從來沒有跟 ChatGPT 「聊天」過，都只有拿來問問題或處理文字而已。


---

### 詢問我認為 AI 知識量不足的問題

雖然我會問 AI 問題，但我在問問題之前會先想一下這個問題是否是 AI 擅長的問題。假設我判斷 AI 在訓練過程中可能沒有這方面的充足資訊，我就不會問 AI 這方面的問題。

舉例來說，我會跟 AI 認真討論產品開發與成長的問題，但我不會問 AI 關於台灣的法律或稅務的問題。


---

## 小結：這只是個開始

寫這篇文的時候我才發現，我已經蠻頻繁在使用 AI ，雖然不是一直不間斷地與他對話討論，但每天都一定會用到它。我相信這個比重只會愈來愈高，這個清單一定會有愈來愈多「會用 AI 做的事」，我邊寫著這篇文就想到好幾件想嘗試的事了！