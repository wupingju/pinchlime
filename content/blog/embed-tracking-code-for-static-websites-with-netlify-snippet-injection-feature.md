---
title: 透過 Netlify 的 snippet injection 功能為靜態網站輕鬆埋設追蹤碼
date: 2023-01-24
description: 這樣做的好處是可以讓自己的網站原始碼保持乾淨，不用把各種追蹤或 A/B test 的設定代碼全都加到網站的程式碼裡面。
path: blog/embed-tracking-code-for-static-websites-with-netlify-snippet-injection-feature
taxonomies:
  categories: 
    - Tools
  tags: 
    - Netlify
    - Static Websites
---

過年期間，來清倉一些之前想要寫，但沒時間寫的小題目。

這篇文適合的對象是那些對靜態網站（static sites）有興趣，期待被多推一把的人。

<!-- more -->
---

### 什麼是 Snippet Injection

我是透過 Zola \+ Github \+ Netlify 的互相搭配來建構目前這個 Pin 起來網站，Netlify 非常的簡單好用，我這個完全的程式外行也可以透過文件跟教學逐步探索相關功能。

其中一個我很喜歡、也很容易使用的是 “Snippet Injection” 功能，不確定中文的正式用法是什麼，我先稱他為「程式碼片段注入」。

他的概念是可以讓你的網站在 Netlify 上面部署完成後，再為你把指定的程式碼片段，「加入」你的 html 網頁檔案裡面，可以加入的片段是 `<head>` 尾段以及 `<body>` 的尾段。

---

### 為何要額外進行 Snippet Injection？

就我目前初步的理解，這樣做的好處是可以讓自己的網站原始碼保持乾淨，不用把各種追蹤或 A/B test 的設定代碼全都加到網站的程式碼裡面。

另一個好處是，要改動或移除追蹤設定都可以更簡單，甚至可以分給不同人來處理，例如行銷團隊可以自行設定追蹤碼，而不需要透過工程師團隊。

等於說，程式碼片段注入的功能，把不同事情模組化，進而更容易拆分與組合。

---

### 該怎麼設定？

在 Netlify 上面[有詳細的說明](https://docs.netlify.com/site-deploys/post-processing/snippet-injection/)，不過我先以最簡單的 Google Analytics 的追蹤碼來示範好了。（我沒有用 GA 追蹤，目前是[使用 Umami 這個主打隱私的追蹤服務](@/blog/started-using-umami-cloud.md)，但 GA 應該更多人使用。）

步驟一：先找到你要注入的 GA 追蹤碼。這部分請自行透過 GA 查找，以截圖的範例來說，大概會是長成下面這樣：


<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/google-analytics-code_JeKjzs.webp" loading="lazy" alt="google-analytics-code" align=center />

步驟二：在 Netifly 的 Site settings ，選擇 “Build & deploy” 選單，並且選到 “Post processing” ，裡面就有 Snippet injection 的功能了。

可以看到截圖，目前我只有設定 Umami Cloud 的程式碼注入，不過他並不是只能設定一個而已，完全可以同時注入多組程式碼。

因此可以點選 “Add snippet” 的按鈕。

<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/netlify-snippet-injection-1_VHYwHh.webp" loading="lazy" alt="netlify-snippet-injection-1" align=center />

步驟三：參考截圖，先在第一個選單選擇 Insert before </head> （這個意思是，這段程式碼會植入在網頁檔案的 `<head>` 區塊裡面，放置在 `</head>` 的位置之前。

這是因為 GA 是要求把追蹤碼放在 Head 區塊，所以才這樣設定，若其他程式碼有不同的功能，則也有可能放在其他的區塊。

而選擇要放的位置後，接著就是幫這個 script 命名，並且貼上步驟一拿到的追蹤碼，原封不動貼上就好，然後就可以按下 Save 了。

<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/netlify-snippet-injection-2_Kawvpq.webp" loading="lazy" alt="netlify-snippet-injection-2" align=center />

對，這樣就大功告成了，基本上整個流程會運用到的關鍵技能就是：

* Click
* Copy
* Click
* Paste
* Click

---

### 成果檢視

在設定完成後， Netlify 幾乎是馬上生效，我回到網站上面打開「開發者工具」後，點開網頁的 <head> 區塊，就可以順利找到被注入的 Google 追蹤碼了。

<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/successfully-injected_mYAe6C.webp" loading="lazy" alt="successfully-injected" align=center />

---

### 後記

我覺得如果跟我一樣，是完全程式外行人，剛開始接觸靜態網站時，拿這個功能練習一些設定會很有成就感，因為非常簡單，而且效果可以直接顯示出來。

甚至可以在剛照著教學把空白範例網站部署到 Netlify 時，就馬上設定追蹤，應該會對於理解不同程式碼段落都在幹嘛很有幫助。

推薦有興趣的人都可以玩玩看！

（若之後學到更多 Snippet Injection 的用法再來分享。）