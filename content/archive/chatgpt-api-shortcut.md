---
title: 不懂程式也可以輕鬆透過 Apple Shortcuts 串接 ChatGPT
date: 2023-03-02
updated: 2023-03-06
description: 只要你是蘋果（主要是 macOS ）的用戶，就可以透過官方免費的 Shortcuts 這個應用程式來串接 ChatGPT 的 API 。而且作法很簡單，你開啟這個 Shortcut 後，只要設定 API key （可以想成是密碼），以及你想要的快捷鍵，就可以開始使用了。
path: blog/chatgpt-api-shortcut
extra:
  image: https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/chatgpt-say-hi_37nm4M.webp
---

> 2023.03.06 這個 shortcut 更新到了 v2 版本，新的連結在這： [ChatGPT shortcut v2](http://bit.ly/3ZJYOTH) ，更新了讓使用者自訂 System 跟 User 內容的地方，歡迎到最後一段的「進階設定」看說明！

<br>

---

今天 OpenAI 推出了 [ChatGPT API](https://openai.com/blog/introducing-chatgpt-and-whisper-apis) ，透過這個 API ，各式各樣的應用程式與服務都可以開始使用與 ChatGPT 相同的模型。

我不會自己寫程式，但今天早上看到有人分享了[在 Popclip 這個 app 上串接 ChatGPT API 的方式](https://forum.popclip.app/t/a-popclip-extension-for-chatgpt-updated/1283/16)，我一下就安裝使用成功了。由於它的程式碼很短，看起來也不難懂，於是下午就邊對照著程式碼、邊看 OpenAI 的 API 文件，想要看看有沒有方式用更簡單的方式來串 API 。

結論是，可以！我參考了網路上的[一個舊版 GPT 串接的教學影片](https://www.youtube.com/watch?v=CN0SZ33x0bE)，自己模仿試出了一個「Shortcut 捷徑」。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/chatgpt-shortcut_zhvdqo.gif" data-fancybox data-caption="chatgpt-shortcut">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/chatgpt-shortcut_zhvdqo.gif" loading="lazy" alt="chatgpt-shortcut" align="center" />
</a>

只要你是蘋果（主要是 macOS ）的用戶，就可以透過官方免費的 Shortcuts 這個應用程式來串接 ChatGPT 的 API。而且作法很簡單，你開啟這個 Shortcut 後，只要設定 API key （可以想成是密碼），以及你想要的快捷鍵，就可以開始使用了。


在教學前，有幾件事需要說明一下：

1. 這個方式會需要你自己去申請 OpenAI 的 API key ，目前應該是註冊後三個月內會有 18 美元的額度可以使用，但用完後若要持續使用就必須付費。所以你可以視用量決定要不要付費。

2. 目前 ChatGPT 的 API 還沒有很簡便的方式去達到「網頁版 ChatGPT 的持續對話效果」，不過我還是有自己做了一個「[可以記憶對話的 chat mode 版本 shortcut](@/archive/chatgpt-api-shortcut-chat-mode.md)」，歡迎你也去參考玩玩看。

3. 不過目前這個 Shortcut 並沒有持續對話的功能，簡單來說，每一次對話都是獨一無二的，他回答完就會忘記之前的對話，所以功能沒有網頁版那麼強。

4. 那為什麼要用這個？我覺得有個很大的好處是，你在任何地方都可以開啟這個視窗，不用再特別登入 ChatGPT 的頁面。而且目前看起來 API 用戶不會遇到系統過載無法上線的問題。

以下是簡單的圖文說明：
<!-- more -->

---

## 如何安裝與設定？

### 步驟一：取得 API Key

如果你已經有 OpenAI 帳號，那就到[後台](https://platform.openai.com/) ，若你沒有帳號，或者想新註冊一個，那就到 [API 頁面](https://openai.com/blog/openai-api)選 Sign up ，登入後，選右上角選單的「View API keys」，然後選擇畫面中央的「Create new secret key」。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/generate-api-key_MjXCsD.webp" data-fancybox data-caption="generate-api-key">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/generate-api-key_MjXCsD.webp" loading="lazy" alt="generate-api-key" align="center" />
</a>

產生後，先找個地方把這串亂碼記錄下來，未來沒辦法再重看一次這串 key 。（真的不見了也沒關係，你隨時可以刪掉舊的 keys，產生新的。）

---

### 步驟二：下載 Shortcut

[我的 Shortcut 連結在這邊](http://bit.ly/3ZJYOTH)，點開後，點選下方的 Get Shortcut ，接著一路點選 Add ，然後會看到一個視窗跳出來，請你輸入 API Key ，這邊就請你把步驟一申請到的 API Key 輸入進去。這邊可以放心，我不會知道你的 API Key。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/import-apikey_CowYG5.webp" data-fancybox data-caption="import-apikey">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/import-apikey_CowYG5.webp" loading="lazy" alt="import-apikey" align="center" />
</a>

若你沒有看到 API Key 的輸入介面，可以編輯第一個「Text」的欄位，直接貼上 API Key 就可以囉！


---

### 步驟三：設定你的啟動熱鍵

接著，請你點選左上角的選單，然後設定你的「Shortcut 啟動熱鍵」，意思是你只要透過熱鍵，就可以隨時叫出這個 ChatGPT shortcut。我覺得透過熱鍵啟動最方便，但如果你想透過其他方式啟動也可以。

如果你沒有別的想法，建議你可以用跟我一樣的 Control \+ Option \+ C 。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/set-a-shortcut_aS30cY.webp" data-fancybox data-caption="set-a-shortcut">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/set-a-shortcut_aS30cY.webp" loading="lazy" alt="set-a-shortcut" align="center" />
</a>

大功告成！你已經完成設定了，就這麼簡單！

---

## 如何使用這個 Shortcut ？

若一切順利，你按下熱鍵後，就會跳出一個輸入視窗，在這個視窗你可以輸入「你想要請 ChatGPT 做的事」，就像你平常使用 ChatGPT 的方式一樣。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/input-window_DlrWQZ.webp" data-fancybox data-caption="input-window">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/input-window_DlrWQZ.webp" loading="lazy" alt="input-window" align="center" />
</a>

不過因為輸入框框比較矮，如果你不太習慣這樣輸入，你也可以先在別的地方打好字，再複製貼上。

貼上後點選 Done ，然後等一下下， ChatGPT 就會產出結果給你了！

（在過程中他可能會請求你的系統權限，可以按下同意。）


<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/chatgpt-say-hi_37nm4M.webp" data-fancybox data-caption="chatgpt-say-hi">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/chatgpt-say-hi_37nm4M.webp" loading="lazy" alt="chatgpt-say-hi" align="center" />
</a>

我猜想，會想使用這個 shortcut 的人應該都是想要在自己熟悉的軟體或服務，例如 Word, Google Docs, Gmail 等等裡面使用。

因此我有預設直接把 ChatGPT 產的結果**複製到剪貼板**。所以你在產出結果後，可以直接關閉視窗，然後到你想要的地方貼上結果。

---

## 進階設定 - 自訂助手的行為模式與指令

這個 shortcut 在 2023.03.06 更新到 v2 版本後，你將可以很輕鬆的設置 "System" 以及 "User" 的指令。

這是什麼呢？歡迎看我寫的另外一篇文： [我的六個專屬 ChatGPT 助手](@/newsletters/22-my-six-chatgpt-assistants.md)

簡單來說，設定這樣的指令能讓你更好地控制 ChatGPT 的產出，有點像是你把平常在 ChatGPT 網頁版的「訓練方式」直接刻到這個助手的設定值裡面，接下來每次都不用再重新訓練。

舉例來說，你可以設定一個「摘要助手」，並且將 System 與 User 的值改成下列內容：

`System：你是一個擅長整理摘要的助手，你會將一段文字去除不重要的形容詞與修飾文字，只留下重要的資訊，並且以列點的方式提供。提供的語言為繁體中文。`

`User：請你使用繁體中文，以 markdown 格式，以列點的方式，提供給我下列文字的摘要： {{ user-input }}`

這樣設定以後，你只要輸入給他一整段文字，他就會回傳給你摘要過後的內容。


設定方式很簡單，你只要找到 Shortcut 裡面這兩個紅框框起來的位置，填入你想設定的內容就好。

不過記得， User 的地方不要刪掉原本那個橘色的「user-input」，這樣 ChatGPT 才會準確讀到你貼上的內容。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/change-system-and-user-variables_yoxVNt.webp" data-fancybox data-caption="chatgpt-say-hi">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/change-system-and-user-variables_yoxVNt.webp" loading="lazy" alt="chatgpt-say-hi" align="center" />
</a>

若設定成功了，你就可以依樣畫葫蘆，複製一個 shortcut ，再設定成其他的助手，你也可以更改 shortcut 的名字，讓他們更好辨識。

---

### 寫在最後

1. 由於這個 shortcut 很簡單，所以完全歡迎大家自己改造使用或分享。

2. 如果你有更好的 shortcut 作法，都歡迎寄信到 pj@pinchlime.com ，或著在 [Twitter](https://twitter.com/WuPingJu) 上跟我分享。

3. 目前這個版本因為有了自訂的空間，我也已經完成了[可以持續對話的 Shortcut 版本](@/archive/chatgpt-api-shortcut-chat-mode.md) ，因此短期內應該不會再更新，但未來若 API 有更多可能性，我還是會透過我的電子報分享，所以歡迎你[訂閱我的電子報或部落格文章](https://pinchlime.com/subscribe/)。

祝大家使用愉快，希望能夠為你帶來幫助。