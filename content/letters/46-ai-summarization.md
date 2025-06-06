---
title: 我終於還是開始靠 AI 幫忙摘要
date: 2025-05-23
description: 我覺得這樣子體驗很好，雖然是簡化、摘要後的內容，但實際上卻增加了我的閱讀量。我甚至不太在意產出的摘要是否有幻覺或者誤讀，對我來說那是可以容忍的錯誤空間，因為現在的模型已經好到八九成以上的內容都沒什麼問題，而且我也是基於原文生成，而不是請他搜尋或依照訓練的資料生成，這也讓幻覺的比率降低了不少。
path: letters/ai-summarization
extra:
  page_type: letter
---

大家好，好久不見，距離上次寄信已快一個月，想說來更新一下最近在幹嘛。

如信件標題所述，我最近開始會透過 ChatGPT 協助我摘要內容，主要是摘要有一定長度的英文訪談內容和長篇論述，像是 [Lenny’s Podcast](https://www.lennysnewsletter.com/podcast/archive?sort=new) 或者是 [Stratechery](https://stratechery.com/)。我會直接透過設定好的 prompt 請 ChatGPT 產出中文摘要，產完後就把它們存在 Heptabase 裡面，排時間閱讀、寫簡單的筆記在 Heptabase 裡面。



**為什麼要這樣做？**

在回答這個問題前，不如先説説，為什麼以前不這樣做。

在 ChatGPT 剛推出的時候我就有嘗試過請他摘要內容，開放 API 後也有嘗試建立自己的摘要助手，也有用過一些摘要工具，但體驗都沒有很好，我猜可能是因為我不會下 prompt、當時的模型還不夠厲害、或者是 context window 還不夠長，還有一個原因是我有某種自傲或偏執，認為只有自己讀進去才是讀，靠 AI 摘要的東西根本就進不了腦袋，那還不如不要摘要。

在這一兩年內我一直都抱持著這樣的價值觀，認為不該把「閱讀」這件事交給 AI。我也確實這樣實踐，每當我認真閱讀一些很長的文章或 Podcast 逐字稿，花了一兩個小時讀完並做完筆記，我都會覺得自己很棒，認為我這樣的「人工堅持」是很有意義的。

但另一方面，這樣做真的很花時間，所以我真正讀完的我想讀的長內容少得可憐，真的很少。

**那是什麼改變了？**

有一個遠因跟一個近因，遠因是在我雖然讀得少，但我在幾次工作機會上有接觸到 Alan 的筆記方式，我覺得那樣整理逐字稿的效果很好，當時我花了幾個小時整理了一集 Lenny’s Podcast 的逐字稿，那集的內容我到現在都還印象深刻，看到那些筆記也還是覺得很有價值。這個經驗讓我好像更掌握「怎麼製作摘要」這件事。

近因是 Heptabase 最近的協作功能推出 “Can edit” 跟 “Can view” 的權限，讓我打算開啟一個我想了很久的計劃：一起共學 Lenny’s Podcast ，於是我寫了[一篇文](https://www.threads.com/@wu_pingju/post/DJy7y8khZqX)介紹這個計劃，也開始徵求協作者。

但在開徵的隔天，我突然想到一件事，如果我跟 AI 協作這個白板，會不會更有效率？於是我就再度開始嘗試 AI 摘要，結果，[測試的結果](https://www.threads.com/@wu_pingju/post/DJ3yhIVhIn_)令人驚訝的好。由於我的 prompt 技巧並沒有什麼進展，我想肯定是因為模型更好了，才有這樣的好表現。

**現在的我是怎麼做？**

這幾天，我每天都丟幾篇很長的 Podcast 去產摘要，有時可能連產幾次看看哪篇最好看，然後再馬上讀完。我發現這種「濃縮後的 Podcast 內容」恰好符合我現在的需求。因為一集訪談通常都要一小時左右，裡面參雜著一些沒那麼重要的資訊和閒聊，但是 AI 會幫我抓出那些核心的重點，我只要讀那些重點就好。

我覺得這樣子體驗很好，雖然是簡化、摘要後的內容，但實際上卻增加了我的閱讀量。

我甚至不太在意產出的摘要是否有幻覺或者誤讀，對我來說那是可以容忍的錯誤空間，因為現在的模型已經好到八九成以上的內容都沒什麼問題，而且我也是基於原文生成，而不是請他搜尋或依照訓練的資料生成，這也讓幻覺的比率降低了不少。總之，目前用這種方式閱讀，對我來說明顯利大於弊，因為若不這樣做，我實際上就是完全不會閱讀。

底下分享一篇範例，歡迎跟我分享你看了的心得，無論是覺得很不錯或覺得還好，都歡迎跟我分享！

---

範例原文：[The Agentic Web and Original Sin](https://stratechery.com/2025/the-agentic-web-and-original-sin/)

產出的摘要內容：

廣告驅動的網路模式雖然引發隱私與操控的爭議，但在缺乏直接付費機制的早期網際網路階段，它是唯一能大規模提供免費內容、讓用戶、網站和廣告商三方共贏的商業模式。

早期網際網路嘗試在瀏覽器中內建支付功能，但受到 Visa 和 Mastercard 等信用卡體系壟斷的阻礙未能成功實現。支付功能的缺位使得廣告成為線上內容唯一可行的大眾化營利模式，長期塑造了網路經濟的走向，並在無形中開啟了依賴用戶數據與隱私交換的商業生態。

微支付（micro-transaction）模式看似允許用戶按篇小額付費，但信用卡手續費成本高昂、內容生產前置投入大等因素使其經濟上不可行。同時，要求用戶為每篇內容反覆決定是否付費會帶來決策疲勞，導致微支付至今難以普及。反觀訂閱模式，透過定期付費換取穩定且明確的內容服務，用戶無需頻繁抉擇即可持續獲得價值，創作者也能獲得可預期的收入，但訂閱制可能將內容封閉在付費牆內，限制其廣泛傳播。

以廣告為本的內容經濟誘導網站追求點擊與流量，曾一度刺激大量內容創作和經濟價值，但也讓粗劣內容充斥、品質下滑。如今這套模式面臨衰退：Google 等搜尋引擎提供的流量支撐正迅速瓦解，用戶大量轉向封閉的應用生態或由 AI 直接給出答案，導致依賴廣告營收的網站訪問量驟減、收入每況愈下，整體廣告支撐的網路內容生態陷入困境。

新一代 AI 技術催生了代理式網路（agentic web）的概念，即軟體代理可以代表用戶自動瀏覽網站、蒐集資訊並執行任務，帶來服務自動化與個人化體驗的新可能。然而，當 AI 代理直接擷取網路內容並提供答案時，傳統靠人類瀏覽所支撐的廣告變現模式失效，內容提供者面臨無法透過流量獲利的困境；同時，如何確保代理取得資訊的可靠性並維持內容生態的良性循環，也成為這種新模式下亟待解決的挑戰。

微軟在 2025 年 Build 開發者大會上提出了「開放代理式網路」的構想，包括採用 Anthropic 發起的 MCP（Model Context Protocol，模型上下文協議）以及微軟自研的 NLWeb（Natural Language Web，自然語言網路介面）作為開放標準，讓網站透過自然語言接口直接被 AI 代理存取，猶如為代理世界打造一套類 HTML 的通用橋樑。這套方案可讓網站更容易融入 AI 生態，然而其設計缺乏內建的支付機制，無法為內容提供者帶來直接收益，難以從根本上解決內容生態的經濟誘因問題。

區塊鏈上的穩定幣（stablecoin）為數位微支付帶來了突破：這類數位貨幣價值穩定，可像資訊一樣快速低費地傳輸，交易幾乎零手續費且金額可無限細分，使極小額支付成為可能。在此基礎上，AI 軟體代理作為純粹的程式決策主體，不受人類逐筆付費猶豫的影響，能夠根據內容使用量自動執行小額付款給內容提供者，為代理式網路注入全新的經濟驅動機制，補足過去微支付不可行的缺口。

未來可以考慮以市場機制來鼓勵內容創作：在代理式網路的協議層引入數位貨幣支付功能（例如穩定幣），由 AI 平台根據其生成答案時引用內容的頻率，透過競價拍賣機制向原內容創作者支付報酬。如此將形成一個全新的內容生態市場：創作者為了獲得 AI 引用而競相提供高品質、有價值的內容，AI 平台、使用者與創作者之間達成新的三方共贏平衡。儘管這種市場化方案的實施細節充滿挑戰，但正如當年廣告模式意外地促成了網路的繁榮，一個開放競價的內容市場有望自發地探索出 AI 與網路內容共生共榮的新道路。