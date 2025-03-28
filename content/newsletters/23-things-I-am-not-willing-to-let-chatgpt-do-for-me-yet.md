---
title: 那些我還不願意讓 ChatGPT 代我做的事
date: 2023-03-12
description: 從 ChatGPT 問世後，我一直深刻感覺、也很認同，生成式 AI 是在為我賦能。以 ChatGPT 來說，他讓我用更少的時間做我原本就會做的事、讓我更容易做到我原本不會做的事，也讓我把我原本就擅長的事做得更好。
path: newsletters/things-I-am-not-willing-to-let-chatgpt-do-for-me-yet
extra:
  page_type: newsletter
  issues: 23
---

經過這兩週的 ChatGPT API 嘗試，我感覺我越來越熟悉他的能與不能，這種感覺很好，因為無效率的嘗試次數降低了，一次就成功的嘗試次數增加了，最好的地方是，若對結果不滿意，我也可以更快地調整參數與指令，接著就有很高的機率表現得更如我預期。

今天這期電子報，就來分享一些這方面的經驗。

<!-- more -->
---

## 我目前的 ChatGPT 使用情境

我目前會把 ChatGPT 用在下列任務上：

* 特定領域的問答助手 （盡量只詢問有標準答案的問題，不詢問關於特定人、事件或公司的問題）
* 解釋我不熟悉的概念給我（盡量請他針對某段文字解釋，而不要直接問他「ＯＯＯ是什麼意思？」）
* 協助我發散思考，例如發想某個命名或標題、發想某個主題的子想法
* 協助我收斂思考，例如給他某些想法，請他提煉出其中的共同或關鍵要素
* 協助我照樣造句，我給他某個固定規格的段落，請他替換其中的主題，產出相應的版本（只在工作上使用）
* 使用別人開發的工具，做更特定的任務，例如[翻譯電子書](https://github.com/yihong0618/bilingual_book_maker)。

若稍微歸納一下，我在上述任務裡面用到的是 ChatGPT 的幾個能力：

* 具有堪稱全方位的基礎知識，因此許多我不懂的事情可以請他給一個最基礎的基本介紹與說明。
* 具有模仿、批次處理大量文字的能力，因此我可以給他規格，讓他照著規則辦事，處理那些結構類似，只要替換概念就好的文字。
* 具有壓縮與解壓縮文字的雙向能力，因此可以請他發散，也可以請他收斂。
* 具有多語言的能力，因此可以請他翻譯。

但這裡面的每一項，即使真的要請他做，也都還有個但書是：千萬不能夠完全照單全收，因為他有可能會出錯、會胡謅。

換句話說，要請 ChatGPT 實際參與工作流程，還有一個核心的條件是：

**自己要能夠驗證 ChatGPT 產出的內容。**

---

例如，要請他解釋給我我不懂的東西，我必須先清楚知道他給的解釋可能有錯，我若需要進一步瞭解更多，必須要自己研究及驗證。

例如，要請他產出特定規格的文字，我必須要能夠看出，他產的內容裡面有哪些是好的、是我要的，而哪些是我還需要再改的。

假設我自己無法驗證品質與真偽，就**不該**讓 ChatGPT 做這件事。

還有一些，是我還**不想**要讓 ChatGPT 做的事。

---

## 我還不想要讓 ChatGPT 做的事

### 摘要

上週分享了「[我的六個專屬 ChatGPT 助手](@/newsletters/22-my-six-chatgpt-assistants.md)」，但裡面有一個助手我從製作完成以後，就幾乎沒有用過，這個助手是 Summarizer ，摘要助手。

不僅如此，摘要 YouTube 影片的 ChatGPT 插件，或者是摘要 PDF 或網路文章的工具，我目前也都還沒有開始使用它們，我覺得原因有兩個：

1. 目前 ChatGPT 的 API 有 tokens 的上限，所以一但原始的資料太長（大約超過 3000 字或 1500 個中文字），摘要就會比較不精準，要嘛漏掉某些段落，要嘛是基於某些拆分摘要再組合的方式進行，但我擔心那樣子做的摘要會有偏誤。但原始資料若很短，我可以很快速讀並產生想法，也不見得需要摘要。

2. 機器摘要的內容，比較沒辦法留下深刻的印象。這有點像是學生時代在課本上畫線一樣，我以為畫線就像魔法，可以把原本不懂的段落變成我懂的東西。但不管是畫線，或者是 ChatGPT 摘要的內容，在我看起來都好像是某種「離我有點近，但我卻碰不到核心」的東西。我感覺這是因為，摘要（壓縮）後，喪失了論理的基礎，缺乏了情感的累積，因此我沒辦法共鳴摘要後的內容，沒辦法吸收成為自己的東西。

但我也不是完全抗拒或反對摘要這件事，我認為他在某些特定場景下是很有幫助的，例如為了應付學校的考試或報告，必須在很短的時間內得到一些資訊。或是原始的文字裡面冗言贅字真的太多，卻又想要在裡面得到某些關鍵資訊。

總之，若目的不在於「取得洞見」或「學習」，而有其他純資訊整理的需求，那麼摘要助手應該還是很有幫助的。另外，假設取得摘要後，自己還是對摘要後的內容產生了共鳴與想法，進而記下自己的筆記，這樣的摘要功能我也覺得很有價值，只是目前我還比較少使用。

---

### 寫作

另一件還不想讓 ChatGPT 做的事情是寫作，這邊指的是部落格或 Twitter 這些，我想滿足自己表達／表現需求而產製文字的場景。

昨天看到推友 Reorx 的「[用 AI 工具快速撰写分享型推文](https://reorx.com/makers-daily/006-a-gpt-ai-based-workflow-for-content-creation/)」這篇文，裡面有一段話很有共鳴：

> 使用 AI 生成并不能帮助我去思考或深入了解问题。写作是一个创造性的过程，我享受它所带来的成就感，甚至挫败感，它们都能使我得到成长。但我依然非常喜欢 GPT AI，因为它会持续优化我的生产力，帮助我分担非创造性劳作，让我能投入更多时间在创造性工作上。

我自己很享受寫作的過程，這過程中當然也會有寫不出東西或覺得寫很爛的挫敗感，但更多的是收穫，而且這樣的收穫會持續積累，積累的不只是實際上產出的內容歸檔紀錄，更是自己在思考決策不同事物上的經驗與能力。

在使用 ChatGPT 這幾個月來，我發現他沒辦法模仿我的文字。即使我丟了一些文字給他，但他產出的內容還是跟我想像中「我應該要寫的文字」有所差距。有點像是「只得其形，不得其意」的感覺。

另外，若仰賴 ChatGPT 寫作，我也會喪失「以寫作的方式思考」這個能力。我有許多文字都是邊寫邊想而產生的，有時會將小塊的文字們組合在一起，但即使是小塊的文字，還是屬於自己從腦袋中冒出來的想法。

這樣的過程若不再由我自己操刀進行，那麼寫出來的東西應該也會越來越無感吧。

---

### 溝通

溝通是另一個我還不打算交給 ChatGPT 做的事，無論是開啟還是回應，無論是正面或負面的情緒，我感覺這部分的文字是別人如何看待與回應我的重要元素，因此這部分的文字還不能夠讓 ChatGPT 代勞。

不過，我倒是覺得可以請 ChatGPT 針對比較棘手的情境與溝通需求先擬定草稿，並且協助自己沙盤推演。這樣做的好處是多了一個友善的助手能夠幫忙自己分擔精神上的壓力，並且提供一些可能的解決方案。即使這些方案未必能用，但有機會讓焦點從「焦慮」轉為「想出一個更好的解決方案」。

但我日常生活中大多數的溝通情境都沒這麼棘手，即使遇到了，也有信任的夥伴能夠討論，所以還沒有開始仰賴 ChatGPT ，但未來若 tokens 的限制開放了，ChatGPT 能夠承載更多對話脈絡，我覺得溝通這一塊應該也有機會派得上用場。

另外，若是已經有某種固定的人設要扮演，而溝通的目標比較在於緩解對方情緒或提供初步的行動指引（而不在於更進階的談判、或者共同探索解決方案），那麼 ChatGPT 應該是非常適合也擅長的。例如大多數電商的客服，可能就是一例。

---

## 小結：賦能的前提，是要了解 ChatGPT 的能與不能

從 ChatGPT 問世後，我一直深刻感覺、也很認同，生成式 AI 是在為我賦能。

以 ChatGPT 來說，他讓我用更少的時間做我原本就會做的事、讓我更容易做到我原本不會做的事，也讓我把我原本就擅長的事做得更好。

這可能是我這麼沈迷於瞭解他的能耐、了解別人的用法、以及自己盡可能嘗試不同用法的原因。了解了越多，再搭配自己的能力與需求，就有機會釋放他的能力，讓他在可被驗證、受控的範圍內，為自己提供幫助。

我相信每個人的使用情境與需求都不太一樣，在不同人的情境中，我會請他做的事，可能是別人還不願讓他做的事，反之亦然。所以我也很好奇大家有哪些事已經會固定讓 ChatGPT 做、哪些事還不會，又有哪些事很期待未來可以讓他做。

希望有機會得到大家的回饋與分享！

---

最後也預告一下，我現在越來越不管之前為電子報設下的規則什麼的，總之就是盡量寫一些我也喜歡或有感的東西出來。不過我還是有許多「純資訊分享」類型的東西想要分享，但實在擔心再塞下去會資訊過載，因此接下來打算在每週週間也多開一期，單純彙整資訊。

期待下週就能夠開始發送這樣的內容！