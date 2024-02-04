---
title: 嘗試透過 Apple Shortcuts 製作能夠記憶對話脈絡的 ChatGPT 助手
date: 2023-03-04
updated: 2023-03-04
description: 這個過程蠻有趣的，雖然中間遇到一些挫折，但最後還是順利達成想要的結果。
path: snapshots/what-i-tried-today/tried-to-build-a-chatgpt-assistant-who-can-remember-contexts-via-shortcuts
taxonomies:
  categories: 
    - Tools
  tags: 
    - ChatGPT
    - Shortcuts
---

在昨天成功[透過 Shortcuts 串接 ChatGPT API](@/blog/chatgpt-api-shortcut.md) 後，今天繼續花了不少時間製作 shortcut 腳本，我嘗試想要直接在 shortcut 裡面達成「聊天」的效果。

我知道最簡單的做法，是把過去的對話紀錄全部疊加上去，作為下一次的 input 前綴，但這樣很快就會遇到 token 上限的問題，也很容易花費過多的 tokens，所以我就思考有沒有什麼其他的作法。

我第一個想到的，是在一段對話後，可以選擇「是否要記錄此段對話」，因為有些對話可能只是確認性質、或者是鋪陳資訊而已，未必是需要被記憶與維護的脈絡，因此若可以不保留不重要的內容，可能就可以省一些 tokens。

第二個想到的是，即使是要保留的對話，也未必要保留整段完整的文字，因此假設在這個階段能夠先請 ChatGPT 摘要一輪，那就有機會更省 tokens 。

我就根據這兩個想法，嘗試透過 Shortcuts 製作看看，結果花了不少時間。

中間最大的卡點是：我實在是不太熟悉 Shortcuts 的使用方式以及概念，所以有許多步驟都在反覆試錯，甚至到失敗了很多次之後，我才發現每個 Shortcut 執行完畢後，他的變數好像是沒辦法保留的。比方說，我即使在單次的流程裡面設定了「把對話摘要加到 “full_conversation” 這個變數」的規則，但當它重新執行一次第二輪對話時，這個變數就不見了。

發現這個限制後，我知道我得要找到一個方式來「維持記憶」，不能夠只靠 Shortcut 本身的設定而已。

後來找了一下，好像可以直接串接 apple notes 來處理，等於我可以把對話脈絡持續疊加到 apple notes 裡面，然後在第二輪、第三輪、第 N 輪對話時，都去讀取 notes 裡面的對話脈絡，這樣就可以達到我所有想要的效果了。

這個過程蠻有趣的，雖然中間遇到一些挫折，但最後還是順利達成想要的結果。不過目前整個運作起來還不太穩定（可能是我對 ChatGPT 回覆方式的設定有問題），所以先不分享這個 Shortcut 出來，但若有興趣測試或瞭解細節的還是很歡迎你跟我說！

最後附上一張經過三輪對話，ChatGPT 成功回答我喜歡的寶可夢有哪些的測試截圖。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/my-favorite-pokemons_bJCVQU.webp" data-fancybox data-caption="my-favorite-pokemons">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/my-favorite-pokemons_bJCVQU.webp" loading="lazy" alt="my-favorite-pokemons" align="center" />
</a>