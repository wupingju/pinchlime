---
title: 嘗試透過 ChatGPT API 打造了一個「靈感夥伴」
date: 2023-04-15
updated: 2023-04-15
description: 我覺得這個助手有助於把我腦中原本很模糊、不精準的一些片段想法與疑問，轉換成某個更有結構的形式，接著我好像就更容易可以想得更清晰、透徹一點。我覺得這樣的效果很棒！
path: blog/tried-to-build-a-muse-mate-with-chatgpt-api
taxonomies:
  categories: 
    - Tools
  tags: 
    - ChatGPT
    - Ideas
extra:
  image: https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/muse-spark_MVFfyO.webp
---

早上設計了一個新的 ChatGPT 助手「Muse Mate 靈感夥伴」，這篇簡單描述一下他的功能、以及為什麼我想要這個助手。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/muse-spark_MVFfyO.webp" data-fancybox data-caption="muse-spark">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/muse-spark_MVFfyO.webp" loading="lazy" alt="muse-spark" align="center" />
</a>

`圖片來源：Midjourney, prompt: muse spark, abstract, pixel arts, --ar 1200:630 --v 5`

最近我在建構自己的知識管理系統，其中一個重要的步驟是要把我知道的東西記錄下來。

例如，我已經大概知道什麼是 GTD ，為了讓自己未來能夠持續累積跟 GTD 有關的想法或問題，我得要先把我知道的部分記下來。

我想到兩種紀錄的方式，例如我可以直接 Google 一下，或者看 wikipedia ，再貼上最滿意的答案。我也可以用自己的話慢慢講出我對 GTD 的理解、疑惑、經驗等等。

這兩種方式各有優缺點，前者很快，但我會感覺我只是在搬運而已，我搬的東西未必是我真的知道的東西，最有可能的狀況是我搬了以後，我以為我知道了，結果反而喪失好奇心。

而後者雖然可以確保我更深刻的想過以及理解，但缺點就是非常耗腦力，一想到要寫這麼多東西就會想放棄。

我發現，我想要的是更好的融合方案，這時我又想到 ChatGPT ，我打算透過 ChatGPT 設置一個專門的助手，他的任務是協助我快速記下我知道的事情，並且提供我一些相關的問題，讓我可以透過「回答問題」的方式補充我的想法。

有了這個念頭以後我就開始嘗試 prompt ，算是蠻順利的就完成了一個效果還不錯的版本。

<!-- more -->

---
### Muse Mate 簡介


透過這個助手，我可以快速輸入我想要處理的「主題」，以及一些相關資訊，接著 ChatGPT 就會基於我輸入的資訊，給我一份類似小助手的統整報告。

例如，我想要了解一些關於「心流」的資訊與想法，我提到：

* 主題：心流
* 領域：生產力理論
* 我知道的事： 我理解的「心流」概念與「專注」類似，每當一個人進入心流的狀態，他可以高效率完成高品質的任務 
* 我不知道的事： 我不確定我理解的是否正確、我不確定心流是否有其他含義
* 我好奇的事：該怎樣穩定達到心流？


把這些資訊都丟給 ChatGPT 以後， ChatGPT 這樣回我：

> 好的，根據你提供的訊息，以下是我的回答：
>
> 心流是一種人們在完全投入某項活動並專注於將自己的技能與挑戰相匹配時可能進入的狀態，通常具有以下特點：目標明確、反饋及時、專注度高、自我感受良好。相比於只是專注，心流同時強調的是進行活動時自身能力與挑戰難度之間的平衡，是一種人們能夠感受到完全投入和專注的快樂，進而高效率地完成任務的狀態。
>
> 如果想要穩定達到心流狀態，可以通過以下幾個方面來實現：1）在進行任務前清晰訂立目標，確定需要完成什麼，並訂立相應的計劃；2）對完成任務的進展情況實時進行監控和調整，以達到高效率的效果；3）找到正確的平衡點，在挑戰和自身能力之間保持平衡，確保挑戰與自己的能力相匹配；4）專注於任務，專心一致，防止外界干擾干擾思緒。
>
> 接下來來問你一些問題：
>
> 1. 你如何理解專注？專注和心流有何區別？
> 2. 你是否經常體驗到心流的狀態？如果是、可以分享一次成功進入心流狀態的經歷嗎？
> 3. 在日常生活或工作中，你通常會如何達到心流狀態？
> 4. 你是否認為心流對於提升產品效率有一定的幫助？能否舉一個具體的例子來說明？

我覺得效果很不錯！

他既有回答我的問題，得到一部分 Google 或 Wikipedia 的效果，同時也提出了一些相關的、我感興趣的、能很快產生想法的問題，透過這些問題，我可以更快速的延伸並記錄「我知道的事」以及「我的想法」，在紀錄（回答）的過程中，我容易產生更多想法。

---

### 我設定的 prompts

以下是我使用的 prompt ，你可以參考看看，或依照這個結構，替換成更符合你需求與期待的範例。

```
System prompt：

我想要你扮演一個能協助我產生靈感與問題的專家，你會針對我提供給你的資訊，詢問我幾個相關的關鍵問題，讓我能夠透過這些問題，進行更深刻的思考。

例如，當我提供給你下列 【 】 內的資訊：
【 { Topic： GTD 理論 }
{ Related Field： Productivity theory }
{ 我知道的事： GTD 理論是一個生產力理論 }
{ 我不知道的事：  }
{ 我好奇的事： GTD 適合的場景是什麼？GTD 想解決的問題是什麼？} 】

你會先回答我有詢問的問題，並且再問我幾個問題，例如下列「 」 內的範例：

「GTD（Getting Things Done）理論是一個生產力管理方法，旨在幫助人們更有效地安排和組織他們的工作和生活。GTD適合的場景是任何需要提高生產力、減少壓力和增加工作效率的情況。GTD的核心目標是幫助人們實現更高效的工作方式，並在不增加壓力的情況下完成各種任務。

我想問你幾個問題：

你為什麼對 GTD 理論感興趣？
你如何在日常生活或工作中應用 GTD 理論？
你怎麼看待 GTD 理論與其他生產力方法（如四象限法、番茄工作法）之間的區別與優缺點？
你在應用 GTD 理論時，遇到哪些挑戰？你如何克服這些挑戰？
你覺得 GTD 理論可以跟哪些管理方法或生產力方法相輔相成？」

你會以繁體中文 zh-hant 提供回答
```

第二段則是 user prompt

```
User prompt：

以下是我這次提供的資訊：
【 { Topic： 心流 (FLOW) }
{ Related Field：Productivity theory }
{ 我知道的事： 我理解的「心流」概念與「專注」類似，每當一個人進入心流的狀態，他可以高效率完成高品質的任務 }
{ 我不知道的事： 我不確定我理解的是否正確、我不確定心流是否有其他含義 }
{ 我好奇的事： 該怎樣穩定達到心流？} 】

請你先回答我有詢問的問題，並且再問我幾個問題：
```

---

### 搭配 Keyboard Maestro 更有效率

另外我也有搭配 Keyboard Maestro 這個工具來加速我輸入這些內容的效果，我只要按一個熱鍵，就會跳出一個視窗讓我輸入當下這個主題相關的資訊（如下圖一），接著 Keyboard Maestro 就會幫我依照我設定好的格式產出文字讓我複製，例如下圖二。 很推薦 Keyboard Maestro！

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/muse-mate-km-prompt_FC0pEC.webp" data-fancybox data-caption="muse-mate-km-prompt">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/muse-mate-km-prompt_FC0pEC.webp" loading="lazy" alt="muse-mate-km-prompt" align="center" />
</a>
<br>

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/muse-mate-km-prompt-2_G5vo41.webp" data-fancybox data-caption="muse-mate-km-prompt-2">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/muse-mate-km-prompt-2_G5vo41.webp" loading="lazy" alt="muse-mate-km-prompt-2" align="center" />
</a>
<br>

而我再把這段文字丟給助手後，他產出的回覆如下，覺得提問的效果還是蠻不錯的！

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/muse-mate-km-answer_s8QejI.webp" data-fancybox data-caption="muse-mate-km-answer">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/muse-mate-km-answer_s8QejI.webp" loading="lazy" alt="muse-mate-km-answer" align="center" />
</a>

---

### 小結

雖然對結果還蠻滿意的，不過這樣做仍會有一些問題（也都是 ChatGPT 的老問題）：

1. 對於我完全不熟悉的領域，我沒有辦法去驗證他講的內容的正確性，所以他的描述僅供參考，但問題的思路值得學習。
2. 他的已知資訊停留在 2021 年，因此我最容易感興趣、好奇的新資訊，他都無法掌握，回答的品質就會有些下降。


但整體來說，我覺得這個助手有助於把我腦中原本很模糊、不精準的一些片段想法與疑問，轉換成某個更有結構的形式，接著我好像就更容易可以想得更清晰、透徹一點。我覺得這樣的效果很棒！之後使用一陣子再持續迭代看看有沒有更好的用法。