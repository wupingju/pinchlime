---
title: 可以持續對話的 ChatGPT Shortcut
date: 2023-03-06
description: 目前 ChatGPT API 還沒有辦法很好的保存對話脈絡。我想到的解方是，讓用戶可以自己選擇，要不要保存本次對話。這樣一來，只有你覺得重要、希望他記憶的對話，才會被記下來持續疊加使用，不僅比較省 tokens ，也更有機會維持更多輪保有脈絡的對話。
path: blog/chatgpt-api-shortcut-chat-mode
taxonomies:
  categories: 
    - Tools
  tags: 
    - ChatGPT
    - Shortcuts
---

## 前言

前幾天分享了 [不懂程式也可以輕鬆透過 Apple Shortcuts 串接 ChatGPT](@/blog/chatgpt-api-shortcut.md) 這篇文，在那之後，我這幾天也都在玩 Shortcuts ，今天就來分享一下新的版本：可以持續對話的 chat mode 版本。

（今天也同步更新舊版的 shortcut 到 v2 ，歡迎你點上面的連結回去看看，我讓他更容易設定成特定的助手，所以舊版的 shortcut 可以視為「單次特化版」，而這篇介紹的則是「記憶脈絡版」。）

這邊簡單說明一下，目前開放的 ChatGPT API 還是最初代的版本，在這個版本裡面使用者可以自訂的內容不多，而且都沒有關於「記憶對話脈絡」的簡易設定方式，因此前一個版本的 shortcut 沒有設定這樣的內容。

但我自己還是很想要有記憶對話脈絡的功能，在特定情況下會很有幫助，因此我還是嘗試了一些不同的方式，最後做出來的這個我覺得算是兼顧簡便以及實用的作法，你只需要有一台有「Shortcuts」這個 app 的蘋果裝置，以及搭配蘋果內建的「Notes」，就可以運作了！

以下是今天的介紹。

<!-- more -->
---

## 最簡單保存對話脈絡的做法：

在 ChatGPT 沒有開放相關功能的情況下，要做到保存對話脈絡，最簡單的方式就是持續疊加先前的對話紀錄上去，例如，今天我跟他說「我有一隻黑貓，名叫 Mimir」，若想要他之後還記得，我就要把這段對話，一起疊加在第二次、第三次、第四次的對話裡面送出。

但這樣做很快就會讓 tokens 爆掉，目前 ChatGPT 開放的單次對話上限為 4096 個 tokens ，若超過，就會無法進行對話。所以目前看到的幾種做法都是只能保存幾次對話，並且限制單次對話的 tokens 數量，藉此達到保存紀錄與實用的均衡。

但是，有些我想要他記得的設定，我就是想要他**一直記得**，若在幾次對話後就被洗掉，也不太方便。

因此我當時想到的解方是，讓用戶可以自己選擇，要不要保存本次對話。

這樣一來，只有你覺得重要、希望他記憶的對話，才會被記下來持續疊加使用，不僅比較省 tokens ，也更有機會維持更多輪保有脈絡的對話。

不過，我覺得這樣還不夠，如果讓用戶隨時都可以檢視、甚至編輯「ChatGPT 現在記得什麼」，應該就更好了吧！

這個 shortcut 可以辦到！

---

## 怎麼做到的？

我在設定時，引入了蘋果內建的備忘錄 Notes 一起協作，我設定了一個 note 叫做 Chat History ，讓他擔任我跟 ChatGPT 之間的橋樑，具體來說流程會變成這樣：

### 步驟

一、
每次對話展開前， ChatGPT 會先去讀取 Chat History 的所有對話，並且把這個資訊放到 API 規定的 "Assistant" 欄位裡。

根據[官方文件](https://platform.openai.com/docs/guides/chat/chat-completions-beta)的說法， Assistant 欄位的功能是用來儲存過去的對話紀錄。

> _The assistant messages help store prior responses. They can also be written by a developer to help give examples of desired behavior._

二、
我將 "System" 欄位設定為「你是一個聰明的助手，擅長回顧對話，對話中的 user 指的是我， assistant 指的是你。」這是讓 ChatGPT 更好地理解他的任務、以及讓他讀懂 Assistant 欄位的內容。

（若你有更好的設定方式歡迎分享給我！）

三、
透過這樣設定，每次 ChatGPT 回答我的問題或指令前，就會先去讀取我們的完整對話紀錄，若是空白就沒有影響，若有紀錄就會參考。

四、
在每次對話結束後，我設定了三個選項，詢問使用者是否要記得這段對話。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/remember-conversation_tPUydb.webp" data-fancybox data-caption="remember-conversation">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/remember-conversation_tPUydb.webp" loading="lazy" alt="remember-conversation" align="center" />
</a>

選項一：是，請你記住，並繼續對話
選項二：不用記住，但我們還是可以繼續對話
選項三：我想要結束段對話

若選了第一個選項， shortcut 會把這段對話都存到 "Chat History" 這則 note 裡面。並且重新開啟一次對話，此時回到第一步驟， Assistant 的欄位就會有更新的對話紀錄了。

若選了第二個選項， shortcut 不會儲存對話紀錄，但還是會重新開啟一次對話，這樣你可以省下寶貴的 tokens ，不會記憶不重要的資訊。

若選了第三個選項，就會結束這次對話（但不會清空對話紀錄。）

---

### 這個方案的優點

我覺得這個方案最好的地方是， notes 非常容易使用，所以你完全可以自己編輯對話紀錄。比方說，在步驟四存下紀錄後，你可以自己去微調編修，把不重要的資訊刪除，只保留你真正想讓 ChatGPT 記得的資訊。

另一個用法是，你完全可以先編輯好一整段你想要他「知道」的資訊，就放在 Chat History 裡面，讓他從現在開始的每一段對話都有充分的脈絡可以運用。（但還是有 tokens 的限制）

我還想到很多玩法，例如維護很多份 notes ，然後製作一些選擇器，讓你啟動對話時可以選擇要 ChatGPT 記得哪段資訊...

總之，我覺得這個方式兼顧了實用性以及方便性，而且不需要寫任何程式都可以自己使用，真的很推薦！

---

### 實際的使用效果

[請看我在 Twitter 上放的影片](https://twitter.com/WuPingJu/status/1632761754769059841)！

---

## 該怎麼設定？

### 步驟一：取得 API Key （若已經有了，可以跳過此步驟）

如果你已經有 OpenAI 帳號，那就到[後台](https://platform.openai.com/) ，若你沒有帳號，或者想新註冊一個，那就到 [API 頁面](https://openai.com/blog/openai-api)選 Sign up ，登入後，選右上角選單的「View API keys」，然後選擇畫面中央的「Create new secret key」。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/generate-api-key_MjXCsD.webp" data-fancybox data-caption="generate-api-key">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/generate-api-key_MjXCsD.webp" loading="lazy" alt="generate-api-key" align="center" />
</a>

產生後，先找個地方把這串亂碼記錄下來，未來沒辦法再重看一次這串 key 。（真的不見了也沒關係，你隨時可以刪掉舊的 keys，產生新的。）

---

### 步驟二：建立一則新的 note 

請你在自己的備忘錄 Notes 裡面開啟一則新的 note ，在第一行輸入「Chat History」。（就這麼簡單）

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/chat-history_e21Dsw.webp" data-fancybox data-caption="chat-history">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/chat-history_e21Dsw.webp" loading="lazy" alt="chat-history" align="center" />
</a>
<br>

---

### 步驟三：下載 Shortcut

接著，請你下載 Shortcut ，[連結在這裡](http://bit.ly/3ZGkkss)，點進去下載後，接著一路點選 Add ，然後會看到一個視窗跳出來，請你輸入 API Key ，這邊就請你把步驟一申請到的 API Key 輸入進去。這邊可以放心，我不會知道你的 API Key。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/import-apikey_CowYG5.webp" data-fancybox data-caption="import-apikey">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/import-apikey_CowYG5.webp" loading="lazy" alt="import-apikey" align="center" />
</a>

若你沒有看到 API Key 的輸入介面，可以編輯第一個「Text」的欄位，直接貼上 API Key 就可以囉！

---

### 步驟四：設定啟動方式，開始使用

你可以在右上角的驚嘆號那邊設定啟動的熱鍵，也可以自己 DIY 設定啟動的方式，例如這幾天就看到有人透過 Siri 啟動，[推友 Ping. 還設定成「敲擊手機背面兩下」啟動](https://twitter.com/pingchn/status/1632682894845186049)，我覺得都很讚！

（對，這個 shortcut 在 Mac 跟 iPhone 上都能使用）

設定完就大功告成了！你可以開始測試看看他能否記得你說過的話、可以開始測試編輯修改你們的對話紀錄、甚至預先依照下列規則輸入你想要他記得的紀錄。

user: 

assistant:
 
歡迎自行試試看！

（在過程中他可能會請求你的系統權限，可以按下同意沒問題。）

---

## 其他自定義的選項

這次的 shortcut 版本，以及舊版本的更新裡面，我都新增了幾個比較常用的 API 變數的設定欄位，若你有興趣調整，可以參考 [OpenAI 的官方文件](https://platform.openai.com/docs/api-reference/chat)，看看這些設定是做什麼用的。你可以設定：

- temperature
- top_p
- max_tokens （我預設為 1,000 ，你若想更省字數可以設定成 300 左右）

設定方式很簡單，找到 shortcuts 裡面的對應欄位，改數字就好！

另外，我也新增了「顯示單次使用 tokens 數量」的功能，這個功能本身不會耗費 tokens ，單純是 shortcut 這端的回傳，我覺得這有助於自己時刻注意自己的 tokens 用量，所以有放入這功能，若你不想要，可以刪除相關的段落。（說明都有寫在 shortcuts 裡面）

---

## 寫在最後

1. 跟上次一樣，完全歡迎大家自己改造使用或分享。

2. 如果你有更好的 shortcut 作法，都歡迎寄信到 pj@pinchlime.com ，或著在 [Twitter](https://twitter.com/WuPingJu) 上跟我分享。

3. 短期內我應該不會再更新 shortcuts ，除非 API 又推出什麼功能，我可能會嘗試看看，但我還會持續探索更多特定需求的 ChatGPT 助手，若你對這些內容有興趣，歡迎追蹤我的 Twitter ，或者[訂閱我的電子報與部落格文章](https://pinchlime.com/subscribe/)。

祝大家使用愉快，希望能夠為你帶來幫助。