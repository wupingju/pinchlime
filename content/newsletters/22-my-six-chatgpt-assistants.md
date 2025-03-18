---
title: 我的六個專屬 ChatGPT 助手
date: 2023-03-05
description: 整個過程測試下來，我發現目前若要大量串接使用 API 協助我，「prompts 的設定方式」還是很重要的，不僅可以更有效率得到自己想要的內容，也可以省下寶貴的 tokens 。但更重要的應該還是釐清自己的需求是什麼，先有某個很想要解決或尋求幫助的任務，再來考慮如何請 AI 幫忙，就會更省力也更容易達成目標。
path: newsletters/my-six-chatgpt-assistants
extra:
  page_type: newsletter
  issues: 22
---

## 閒聊

Hi 大家好，週四的時候 ChatGPT 的 API 版本正式推出，我原先以為要再等幾個月才會有這個東西，沒想要就這樣咻一下就出現了。

出現後我發現我還沒有做好心理準備，這讓我這幾天都處於緊張＋興奮的疊加狀態，緊張在於我好像還沒有辦法完全駕馭與掌握 API 帶來的好處，但興奮則在於，有各種各樣的創意與參考範例不斷迸發出來。

過了幾天，我的緊張略降，興奮仍在，因此今天這期也會圍繞著這個主題，分享一下我目前怎麼理解與使用 ChatGPT 的 API 。

<!-- more -->
---

## 什麼是 API ？

API 的全名是 Application Programming Interface ，翻譯叫做「應用程式介面」。我不是工程師，第一次認真聽到 API 這個詞應該是在 2019 年的[星箭廣播 EP15](https://blog.starrocket.io/posts/star-rocket-podcast-ep15-api/) 上面，很推薦跟我一樣不是工程師的人可以再去複習一下。

但如果要以我現在的理解來翻譯的話，可以將 API 理解成「一種有特定格式的溝通方式」，舉例來說， ChatGPT 的 API ，就定義了一些基本規則，你在跟他溝通前，必須填寫你選用的模型、你要請他處理的 message ，他會根據你填寫的內容，回傳特定類型的資料給你。

溝通的本質是交換，A 方根據規則給 B 方資料，B 方根據規則回傳資料給 A 方。不同的應用程式或服務，都可以規定「別人該如何給自己資料」以及「自己會如何回傳資料給別人」。

這樣做的好處是，規則固定後，等於限定了可以溝通可以請求的項目，所以「可以做什麼、不可以做什麼」也都更明確了。這樣的好處是降低了溝通成本，不用不斷試錯或無效溝通。

再舉個例子，大家都知道法院是去告人或者是為自己辯護的地方，所以不會去那邊購物。以這個類比例子來說，法院只有開放訴訟相關的 API ，如果你帶著購物清單到法院，告訴法官你想要買東西，法官也無法理解你的需求，因為你的需求與法院的功能不符合。

而回到 ChatGPT 的 API ，在正式開放後，全世界所有人都可以透過 OpenAI 訂出的規則來「使用」ChatGPT ，這帶來的好處是：

1. 可以在 ChatGPT 官網以外的地方也使用 ChatGPT
2. 可以更客製化地使用 ChatGPT ，因為哪些東西可以自訂都變得更明確了。

---

## 我製作 ChatGPT 助手的初步經驗

在 ChatGPT API 開放的那天，很快地就看到一些我熟悉的工具串起 API 的嘗試，例如 Popclip 、 Drafts 、Bob 等等。

其中，從 Popclip 的程式碼裡面我發現，要串這個 API 好像不難耶！然後再看了一下 OpenAI 的文件，發現好像有機會自己做做看，因此當天就做了一個 Shortcut 版本的助手，詳情可以參考[不懂程式也可以輕鬆透過 Apple Shortcut 串接 ChatGPT](@/archive/chatgpt-api-shortcut.md)這篇。

這個經驗對我來說很重要，是我第一次串 API ，雖然還是透過 Shortcuts 這種 no-code 工具，但還是有種自己很棒的感覺。

而且嘗試成功一次後，後續就可以在 ChatGPT API 有開放的規則裡面，繼續嘗試各種不同的變化版本。

因此昨天一整天我又試著透過 Shortcuts 以及 Apple Notes ，[達成可以記憶對話脈絡的版本](@/archive/tried-tried-to-build-a-chatgpt-assistant-who-can-remember-contexts-via-shortcuts.md)。

不過嘗試以後我發現，以目前 ChatGPT API 開放的溝通方式來說，還沒有特別適合保存對話脈絡，如果要這樣做，要嘛需要大量人工介入，要嘛需要耗費大量 tokens ，而且還有一個「單次處理內容不得超過 4096 tokens」的限制，很難簡單繞過。

因此如果有維持對話脈絡、或者是更「聊天感」的需求，目前覺得還是透過 ChatGPT 網頁版，或者是其他不需要用自己 API key 的方式更好。（我想這個「**目前**」應該最快幾個禮拜，最慢幾個月內，就會很不一樣了。）

但在嘗試過程中，我也找到目前對我來說， ChatGPT API 最有幫助的地方：**處理單次的特定需求。**

這也是今天電子報的主題，我的六個專屬 ChatGPT 助手。

---

## ChatGPT API 的自訂欄位

在 [ChatGPT API 文件](https://platform.openai.com/docs/guides/chat/introduction)裡面有提到，一次 API 請求裡面可以包含三種不同的角色，分別是「system」、「user」與「assistant」，三者的功能分別如下：

### System

System 的地方填入的內容會規範這個助手的行為方式，例如最通用的「You are a helpful assistant」，或者是各種 prompts，像是「你是一個擅長 Javascript 的資深工程師」、「你是一個擅長鼓勵稱讚別人的友善助手」之類的。

不過我只有簡單設定了一些 system 規則，有時效果不是特別理想，也還沒有測出 system 設定的限制以及 best practices 。

### User

在 User 欄位填入的內容則是使用者的「指令」，也就是「你想要 ChatGPT 做什麼、怎麼做」之類的設定。

我實測的結果、以及看了一些國外 Twitter 分享的結果是，User 這邊指令的重要性比 System 更高，比方說我想要 ChatGPT 省話，所以嘗試在 System 設定「你是一個話不多的助手，若 user 沒有問你問題，你就不必回覆多餘內容」，結果沒用，他還是在我測試「我最喜歡的寶可夢是伊布」時，回傳我一堆關於伊布的資訊。

但相反地，我若在 User 的指示說：「以下對話，若我沒有詢問，你不必回覆多餘內容」，然後再接「我最喜歡的寶可夢是伊布」，他就會說「知道了，我會記得你最喜歡的寶可夢是伊布。」

所以 User 欄位的前綴詞設定（以及建立通用規則）會是專屬助手的關鍵。

### Assistant

在 Assistant 欄位填入的，是你想要本次對話裡面就帶到的對話脈絡與必要資訊。

舉例來說，假設你在 Assistant 欄位裡面填入「user: 我最喜歡的寶可夢是伊布」，然後在當次的 user 內容填入：「請問我最喜歡的寶可夢是什麼」，ChatGPT 應該就會回應你「是伊布」，因為你已經把某個關鍵資訊餵給 Assistant 了。

不過我對於這個功能的使用還不多，只有在維持脈絡的那個版本，把 Assistant 欄位拿來放置「過去對話的紀錄」。

介紹完這三個基本概念，就可以來分享一下我的幾個助手有哪些、分別是怎麼設定的。

---

## 我的六個專屬助手

我目前有六個常設的助手，以下是他們的名字與基本功能：

* Q&A mode
  * 最一般的助手，拿來處理各種各樣的一般性問題或者需求。
* Summarizer
  * 可以將我提供的文字，摘要成列點文字給我。
* Challenger
  * 可以針對我提供的文字，盡量提出問題。
* Creator
  * 可以針對我提供的主題，列點提出相關的子議題。
* Editor
  * 可以將我提供的文字，編輯成更通順的版本。
* Explainer
  * 可以將我提供的文字，去除掉艱深的用字與術語，轉化成最簡單的說明版本給我。

以下簡單介紹他們的效果與設定方式。

### Q&A mode

描述：他是最一般的助手，拿來處理各種各樣的一般性問題或者需求，我必須要把我要做的事情都定義清楚。

功能：但他有一個好處是，我透過 Keyboard Maestro 這個工具，串了一個動作。我可以在任何編輯界面，呼叫這個助手，他就會接續執行「處理我的請求 → 貼上回覆文字」的動作，換句話說，我可以在任何介面都使用這個助手。例如下圖，我就是直接在 Heptabase 裡面使用它。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/QA-mode-demo_j5m15z.gif" data-fancybox data-caption="QA-mode-demo">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/QA-mode-demo_j5m15z.gif" loading="lazy" alt="QA-mode-demo" align="center" />
</a>

所以這個助手對我來說優點是方便性，我可以隨時在打字打到一半時，直接請求 ChatGPT ，他就會回傳給我我期待的內容。

---

### Summarizer

描述：他可以將我提供的文字，摘要成列點文字給我。

設定方式：

* System：你是一個擅長整理摘要的助手，你會將一段文字去除不重要的形容詞與修飾文字，只留下重要的資訊，並且以列點的方式提供。提供的語言為繁體中文。
* User：請你使用繁體中文，以 markdown 格式，以列點的方式，提供給我下列文字的摘要： {{ 我複製的文字 }}

兩者加起來的效果是，他會幫我摘要某段特定的文字，並且回傳列點的摘要給我。

例如，下面這個截圖範例是請他摘要 Paul Graham 的 [The need to read](http://paulgraham.com/read.html) 這篇文章，大概花了 10 秒左右就回傳列點摘要給我。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/summarizer_demo_DLnBa2.webp" data-fancybox data-caption="summarizer_demo">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/summarizer_demo_DLnBa2.webp" loading="lazy" alt="summarizer_demo" align="center" />
</a>

由於我會使用這個助手的情境大多在於網路閱讀時，因此我採用彈窗的方式來提供輸出後的資料給我，讓我可以直接閱讀。

---

### Challenger

描述：他可以針對我提供的文字，盡量提出問題。

設定方式：

* System：你是一個擅長提問的助手，你會針對一段內容，提出可能的疑慮或問題，以促進更完整的思考。
* User：請你使用繁體中文，針對下列文字提出可能的問題： {{ 我複製的文字 }}

這個助手應該是六個助手裡面我個人最喜歡的一個，他的功能是質疑、挑戰我的論點。

比方說，我今天在寫文章時如果寫了「未來的世界裡面， AI 就像電力一樣，是每個人生活中不可或缺的基礎設施」，接著，我就直接請挑戰者出動。

他的回應如下：

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/challenger-demo_BPTuU8.webp" data-fancybox data-caption="challenger-demo">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/challenger-demo_BPTuU8.webp" loading="lazy" alt="challenger-demo" align="center" />
</a>

可以看到，由於我只給了一句斷言直述句，所以他的回覆也偏向泛泛之言，但已經很足夠。

假設我給了更完整的論述，他的表現會更好，例如，我繼續餵給他上面 Paul Graham 那篇 [The need to read](http://paulgraham.com/read.html) ，他就提出了下列問題。在我看來，他提問的內容都還不錯，有兩個 what 的問題，但也有兩個 why 的問題。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/challenger-demo-2_Wi5Rff.webp" data-fancybox data-caption="challenger-demo-2">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/challenger-demo-2_Wi5Rff.webp" loading="lazy" alt="challenger-demo-2" align="center" />
</a>

這個挑戰者助手不僅對於我的思考與寫作有幫助，也能讓我讀到某些文章的特定段落時，詢問 ChatGPT 對方的論理邏輯是否有哪邊怪怪的，進而讓我可以思考更多。

---

### Creator

描述：可以針對我提供的主題，列點提出相關的子議題。

設定方式：

* System：你是一個擅長產生想法的助手，你會把一個主題拆解成相關的幾個子題目。
* User：請你使用繁體中文，針對下列主題，提供相關的子議題： {{ 我複製的文字 }}

這個助手的功能是幫助我發想可能的相關議題，例如，我想寫一個「 AI 有助於我寫作電子報」的題目，請 Creator 協助我發想。

他給我的內容如下：

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/creator-demo_EoJ0bh.webp" data-fancybox data-caption="creator-demo">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/creator-demo_EoJ0bh.webp" loading="lazy" alt="creator-demo" align="center" />
</a>

我覺得這個助手可以在我只有初步想法時，快速丟更多想法給我，讓我去組織架構出合理的框架與內容細節。不過也許他的名字不該叫 Creator ，之後再來調整看看。

---

### Editor 

描述：可以將我提供的文字，編輯成更通順的版本。

設定方式：

* System：你是一個擅長編輯文字的助手，你會將一段文字編輯成語意通順、沒有錯漏字的版本，以讓讀者更容易理解內容。
* User：請你使用繁體中文，協助我編輯下列文字成為更通順的版本： {{ 我複製的文字 }}

這個助手的功能是幫助我編輯邏輯比較鬆散、凌亂的文字。有的時候我會快速記下一些想法，這些想法可能是很意識流的內容，不見得有組織。而組織看起來有邏輯的文字剛好是 ChatGPT 的強項，因此我也很喜歡這個助手。

例如，我前幾天曾經在睡前記下一段文字：

> Programming 是一種思維方式，能夠套用到任何事物的處理上
>
> 而 AI 的好處是可以用自然語言進行 programming ，但他還是需要有各方面的 domain knowledge
>
> 那我該如何提升各方面的 domain knowledge ，取得經過驗證的資訊？又該由誰來驗證？

而經過 Editor 巧手修改後，這段文字變成下列內容：

> Programming 是一種具有廣泛運用的思維方式，可以幫助我們更有效地處理各種事務。透過程式設計，我們可以將複雜的問題分解成小部分，進而處理。而 AI 則是透過自然語言方式進行程式設計，使得使用者不需要懂得完整的程式語言即可以利用 AI 進行各項工作，大幅提升了工作效率。
>
> 但要讓 AI 更好地發揮作用，還需要有豐富的各方面 domain knowledge。因此，想要提升自己的 domain knowledge，可以透過多閱讀相關書籍、研究專業文章、聆聽更多有經驗的人分享等方式，不斷學習與累積。同時，也可以參與相關的社群或研究團隊，與其他人進行交流，互相學習。

雖然這段文字不見得是我會想要的，但有個人幫忙潤稿還是很好。這個功能也可以用在網路閱讀時、或者是直接看機器翻譯內容時，可能會看到一些不通順但又很想真正理解的段落，就可以請 Editor 助手出動協助。

---

### Explainer

描述：可以將我提供的文字，去除掉艱深的用字與術語，轉化成最簡單的說明版本給我。

設定方式：

* System：你是一個擅長解釋複雜文字的助手，你會將一段比較難理解的文字，轉化成簡單的句子與概念，以讓讀者更容易理解內容。你的目標受眾是 12 歲的學生。
* User：請你使用繁體中文，避免使用專業術語，盡量透過舉例與比喻，解釋下列這段文字在說什麼： {{ 我複製的文字 }}

這個助手的功能是幫助我解釋複雜的概念，有時讀到一些比較難的、充滿專業術語或概念的文章時，可能會看不懂、無法理解，這時就可以請 Explainer 幫忙。

例如，我直接請他解釋[比特幣白皮書](https://bitcoin.org/bitcoin.pdf)的摘要，原始文字如下：

> **Abstract.** A purely peer-to-peer version of electronic cash would allow online payments to be sent directly from one party to another without going through a financial institution. Digital signatures provide part of the solution, but the main benefits are lost if a trusted third party is still required to prevent double-spending. We propose a solution to the double-spending problem using a peer-to-peer network. The network timestamps transactions by hashing them into an ongoing chain of hash-based proof-of-work, forming a record that cannot be changed without redoing the proof-of-work. The longest chain not only serves as proof of the sequence of events witnessed, but proof that it came from the largest pool of CPU power. As long as a majority of CPU power is controlled by nodes that are not cooperating to attack the network, they'll generate the longest chain and outpace attackers. The network itself requires minimal structure. Messages are broadcast on a best effort basis, and nodes can leave and rejoin the network at will, accepting the longest proof-of-work chain as proof of what happened while they were gone.

他回覆給我的內容如下：

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/explainer-demo_oHFEQ3.webp" data-fancybox data-caption="explainer-demo">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/explainer-demo_oHFEQ3.webp" loading="lazy" alt="explainer-demo" align="center" />
</a>

我覺得雖然還有像是「哈希」或者是「雙重支付」這樣的術語，但已經比單純用翻譯還要好理解一些，當然，也可以逐段請他說明，這樣更可以保持完整的脈絡。

---

## 整個過程中我學到的事

在製作這些助手的過程中，我持續在做的是這幾件事：

1. 我思考了我的需求，釐清有哪些是有機會透過 AI 幫忙、我也想要有 AI 幫忙的事情。
2. 我持續調整我的設定值，想辦法讓 AI 給出最符合我想法的回答方式與答案。
3. 我盡量拆解我的工作流程，讓他們成為足夠原子化的情境。

透過這幾個步驟，我慢慢可以讓 AI 介入我的工作流程。有賴於 API 的推出以及幾個 no code 的工具（shortcuts, keyboard maestro 等等），我可以隨時呼叫 ChatGPT 提供幫助。

整個過程測試下來，我發現目前若要大量串接使用 API 協助我，「prompts 的設定方式」還是很重要的，不僅可以更有效率得到自己想要的內容，也可以省下寶貴的 tokens 。

但更重要的應該還是釐清自己的需求是什麼，先有某個很想要解決或尋求幫助的任務，再來考慮如何請 AI 幫忙，就會更省力也更容易達成目標。

接下來我會持續調整這些助手的設定，也已經有好幾個新的助手想法了，例如 [piglei 提出的 AI vocabulary builder](https://twitter.com/Piglei/status/1631943319109656576) ，或者是安排任務優先序的助手等等，若你想一起討論 prompts ，或者是你也有一些很有趣的助手想法，都歡迎跟我分享討論！

最後也分享一下推友 [Reorx](https://twitter.com/novoreorx) 製作的 [ChatGPT API 資訊彙集](https://github.com/reorx/awesome-chatgpt-api)，裡面有很多有趣的專案！