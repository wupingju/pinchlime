---
title: 在 Raycast 裡直接使用 DeepL 翻譯 
date: 2022-12-21
updated: 2022-12-21
path: blog/tried-to-use-raycast-extension-deepcast
description: 我覺得翻譯得很精準也堪用，頂多微調幾個字就可以使用了。
taxonomies:
  categories: 
    - Tools
  tags: 
    - Raycast
    - DeepL
---


自從 [4 月安裝 Raycast](@/blog/raycast-introduction.md) 以來，一直沒有好好地發揮他完整的能力，只有用到一些基本款的功能，例如字典查詢、應用程式快速啟動、檔案查找、計算機、視窗管理等等。

不過上週 Raycast 推出 [Raycast Wrapped 2022](https://twitter.com/raycastapp/status/1603404709573828609) 這個活動後，看到好多人在分享自己使用 Raycast 的數據，覺得好像該來重新花點力氣玩玩看。

<!-- more -->

---

## Deepcast

於是逛起了內建的 Extension Store，發現比起幾個月前，又多了好多我感興趣的外掛插件。其中一個是 “[Deepcast](https://github.com/raycast/extensions/tree/447cf3a29ef4a3c5d2b3f34d593c00191dc3fe02/extensions/deepcast)”，它可以讓你串接 [DeepL](https://www.deepl.com/) 這個翻譯神器的 API ，然後就可以直接透過 Raycast 直接翻譯剪貼簿的文字，內建有 26 種語言可以翻譯。

我去年寫論文時就是 DeepL 的愛用者，但台灣一直沒辦法註冊（它註冊要認證地址以及該地區發行的信用卡，亞洲目前只有開放日本以及新加坡，[詳細開放地區可看這邊](https://www.deepl.com/pro/select-country)），所以都是透過 DeepL 的官方 mac app 使用免費版，並且有每次翻譯 5000 字元的限制。

但現在剛好有家人在美國，這次就委託他幫我註冊一個帳號，並且申請了 DeepL 的 API，每個月有 500,000 個字元的免費翻譯額度。

<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/deepl-account_Hxi7rK.webp" loading="lazy" alt="deepl-account" align=center />

申請好後在 Raycast 裡面輸入 API Key，馬上就能開始使用了！

<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/raycast-deepcast_JGSyJY.webp" loading="lazy" alt="raycast-deepcast" align=center />


如截圖，我只開啟了 Translate into English 以及 Translate into Chinese 這兩個選項，並且分別設定了 te 跟 tc 這兩個快速啟動詞（alias），而具體使用起來非常單純，流程如下：

* 框選你想要翻譯的文字
* 在 Raycast 中輸入設定好的快速啟動詞（alias）：”te”
* 再按下 return 鍵
* 翻譯結果就會直接到你的剪貼板，再到想要的地方貼上就好。

例如，我直接將上方的流程文字照著操作一次，會得到下列文字：

> Select the text you want to translate, enter the set alias "te" in Raycast, and then press the return button, and the translation result will go directly to your clipboard.

我覺得翻譯得很精準也堪用，頂多微調幾個字就可以使用了，這樣總共是用掉了 84 個字元的額度。

而如果再翻譯一次回中文，會得到下列文字（目前只能翻譯成簡體中文）：

> 选择你要翻译的文本，在Raycast中输入设定的别名 "te"，然后按返回键，翻译结果将直接进入你的剪贴板。

不過這個功能感覺比較適合在筆記軟體或文書處理工具裡面使用，若要在瀏覽器中使用，應該可以直接下載 [DeepL 的 chrome extension](https://chrome.google.com/webstore/detail/deepl-translate-reading-w/cofdbpoegempjloogbagkncekinflcnj) 就好，用起來也非常直覺簡單！