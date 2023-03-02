---
title: 不懂程式也可以輕鬆透過 Apple Shortcuts 串接 ChatGPT
date: 2023-03-02
description: 只要你是蘋果（主要是 macOS ）的用戶，就可以透過官方免費的 Shortcuts 這個應用程式來串接 ChatGPT 的 API 。而且作法很簡單，你開啟這個 Shortcut 後，只要設定 API key （可以想成是密碼），以及你想要的快捷鍵，就可以開始使用了。
path: blog/chatgpt-api-shortcut
taxonomies:
  categories: 
    - Tools
  tags: 
    - ChatGPT
    - Shortcuts
extra:
  image: https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/chatgpt-say-hi_37nm4M.webp
---

今天 OpenAI 推出了 [ChatGPT API](https://openai.com/blog/introducing-chatgpt-and-whisper-apis) ，透過這個 API ，各式各樣的應用程式與服務都可以開始使用與 ChatGPT 相同的模型。

我不會自己寫程式，但今天早上看到有人分享了[在 Popclip 這個 app 上串接 ChatGPT API 的方式](https://forum.popclip.app/t/a-popclip-extension-for-chatgpt-updated/1283/16)，我一下就安裝使用成功了。由於它的程式碼很短，看起來也不難懂，於是下午就邊對照著程式碼、邊看 OpenAI 的 API 文件，想要看看有沒有方式用更簡單的方式來串 API 。

結論是，可以！我參考了網路上的[一個舊版 GPT 串接的教學影片](https://www.youtube.com/watch?v=CN0SZ33x0bE)，自己模仿試出了一個「Shortcut 捷徑」。

<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/chatgpt-shortcut_zhvdqo.gif" loading="lazy" alt="chatgpt-shortcut" align=center />

只要你是蘋果（主要是 macOS ）的用戶，就可以透過官方免費的 Shortcuts 這個應用程式來串接 ChatGPT 的 API。而且作法很簡單，你開啟這個 Shortcut 後，只要設定 API key （可以想成是密碼），以及你想要的快捷鍵，就可以開始使用了。


在教學前，有幾件事需要說明一下：

1. 這個方式會需要你自己去申請 OpenAI 的 API key ，目前應該是註冊後三個月內會有 18 美元的額度可以使用，但用完後若要持續使用就必須付費。所以你可以視用量決定要不要付費。

2. 目前 ChatGPT 的 API 還沒有很簡便的方式去達到「網頁版 ChatGPT 的持續對話效果」，因此我這個 Shortcut 版本也沒有製作這方面的功能，簡單來說，每一次對話都是獨一無二的，他回答完就會忘記之前的對話，所以功能沒有網頁版那麼強。

3. 那為什麼要用這個？我覺得有個很大的好處是，你在任何地方都可以開啟這個視窗，不用再特別登入 ChatGPT 的頁面。而且目前看起來 API 用戶不會遇到系統阻塞無法上線的問題。

以下是簡單的圖文說明：
<!-- more -->

---

## 如何安裝與設定？

### 步驟一：取得 API Key

如果你已經有 OpenAI 帳號，那就到[後台](https://platform.openai.com/) ，若你沒有帳號，或者想新註冊一個，那就到 [API 頁面](https://openai.com/blog/openai-api)選 Sign up ，登入後，選右上角選單的「View API keys」，然後選擇畫面中央的「Create new secret key」。

<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/generate-api-key_MjXCsD.webp" loading="lazy" alt="generate-api-key" align=center />

產生後，先找個地方把這串亂碼記錄下來，未來沒辦法再重看一次這串 key 。（真的不見了也沒關係，你隨時可以刪掉舊的 keys，產生新的。）

---

### 步驟二：下載 Shortcut

[我的 Shortcut 連結在這邊](http://bit.ly/3KPcqJ2)，點開後，點選下方的 Get Shortcut ，接著一路點選 Add ，然後會看到一個視窗跳出來，請你輸入 API Key ，這邊就請你把步驟一申請到的 API Key 輸入進去。這邊可以放心，我不會知道你的 API Key。

<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/import-apikey_CowYG5.webp" loading="lazy" alt="import-apikey" align=center />

---

### 步驟三：設定你的啟動熱鍵

接著，請你點選左上角的選單，然後設定你的「Shortcut 啟動熱鍵」，意思是你只要透過熱鍵，就可以隨時叫出這個 ChatGPT shortcut。我覺得透過熱鍵啟動最方便，但如果你想透過其他方式啟動也可以。

如果你沒有別的想法，建議你可以用跟我一樣的 Control \+ Option \+ C 。

<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/set-a-shortcut_aS30cY.webp" loading="lazy" alt="set-a-shortcut" align=center />


大功告成！你已經完成設定了，就這麼簡單！

---

## 如何使用這個 Shortcut ？

若一切順利，你按下熱鍵後，就會跳出一個輸入視窗，在這個視窗你可以輸入「你想要請 ChatGPT 做的事」，就像你平常使用 ChatGPT 的方式一樣。

<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/input-window_DlrWQZ.webp" loading="lazy" alt="input-window" align=center />

不過因為輸入框框比較矮，如果你不太習慣這樣輸入，你也可以先在別的地方打好字，再複製貼上。

貼上後點選 Done ，然後等一下下， ChatGPT 就會產出結果給你了！

（在過程中他可能會請求你的系統權限，可以按下同意。）


<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/chatgpt-say-hi_37nm4M.webp" loading="lazy" alt="chatgpt-say-hi" align=center />

由於目前網頁版的 ChatGPT 在維持脈絡上還是比較強，所以我猜想，會想使用這個 shortcut 的人應該都是想要在自己熟悉的軟體或服務，例如 Word, Google Docs, Gmail 等等裡面使用。

因此我有預設直接把 ChatGPT 產的結果**複製到剪貼板**。所以你在產出結果後，可以直接關閉視窗，然後到你想要的地方貼上結果。

整個 Shortcut 的功能就只有這樣，如果你還想要更多，可以自己研究 ChatGPT 的 API 與這個 Shortcut ，並且改成你想要的樣子！

---

### 寫在最後

1. 由於這個 shortcut 很簡單，所以完全歡迎大家自己改造使用或分享。

2. 如果你有更好的 shortcut 作法，都歡迎寄信到 pj@pinchlime.com ，或著在 [Twitter](https://twitter.com/WuPingJu) 上跟我分享。

3. 目前這個版本受限於 ChatGPT 的 API 剛推出，以及我的技術能力較不足，比較像是一個 demo 版本，如果我未來有更好的作法，應該會透過我的電子報分享，所以歡迎你[訂閱我的電子報或部落格文章](https://pinchlime.com/subscribe/)。

祝大家使用愉快，希望能夠為你帶來幫助。