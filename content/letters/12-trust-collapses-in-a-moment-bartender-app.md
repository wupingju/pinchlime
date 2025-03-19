---
title: 信任的瓦解只在一瞬 - Bartender app
date: 2024-06-05
description: 我爬了一下 Reddit 的兩個討論串，中間也看了目前自稱是Bartender 新的開發者的回覆，還有來自 MacUpdater 這個工具的開發者的補充說明，最後我決定移除 Bartender ，改使用另一個功能類似，但看起來比較陽春的工具 Ice。
path: letters/trust-collapses-in-a-moment-bartender-app
extra:
  page_type: letter
---

有個 MacOS 上面的老牌軟體叫做 Bartender，它做的事情很單純，就是讓你可以管理你在 Mac 頂端的 menu bar。例如，可以隱藏不需要的圖示、設定它們出現的規則與間距等等（可能是因為要管理這個 bar 才取名叫做 bartender？）

我從 2018 年開始接觸生產力工具後就購買了 Bartender 3 ，後來升級到 4 時也繼續付費支持，升級到 5 時則是改用 Setapp 的版本，中間曾經換過幾台 Mac ，Bartender 始終都是我一定會在一開始就安裝、永遠保持開啟狀態的好用小工具，因為它可以幫我把不常用到的 icons 全部藏起來，讓我更容易在 menu bar 上面找到我想找的工具。

今天突然看到 Twitter 上面在傳一則來自 Reddit 的消息，主要的內容是建議大家移除 Bartender ，因為這個軟體似乎在幾個月前已經移轉了開發者，然後新的版本好像有些問題。

我爬了一下 Reddit 的兩個討論串，中間也看了目前自稱是Bartender 新的開發者的回覆，還有來自 MacUpdater 這個工具的開發者的補充說明，最後我決定移除 Bartender ，改使用另一個功能類似，但看起來比較陽春的工具 [Ice](https://github.com/jordanbaird/Ice) 。

下面條列簡述一下我觀察到的事情以及我決策的依據，若對原始資訊還有其他用戶的想法有興趣，歡迎去看這兩串 Reddit 討論：

- [Bartender 5 not safe anymore ? Warning from MacUpdater : r/macapps](https://www.reddit.com/r/macapps/comments/1d7zjv8/bartender_5_not_safe_anymore_warning_from/)
- [Highly suggest to remove Bartender 5 from your computers : r/macapps](https://www.reddit.com/r/macapps/comments/1d87ykz/highly_suggest_to_remove_bartender_5_from_your/?sort=new)

---

發生的事：

- MacUpdater 這個軟體版本管理工具的開發團隊發現 Bartender app 在更新到 5.0.52 版本時的簽名更換了，不是原本的開發者 Ben Surtees，他們聯絡後者得不到任何回應。他們也發現原本 Bartender 這個 app 的網站風格改變，blog 出現很多看起來是 ChatGPT 寫的 SEO 行銷文章。他們調查 5.0.52 版本的程式碼後沒有發現明顯的問題，但由於背後開發者的變化以及聯絡不上原本的開發者，他們決定通知使用者們謹慎更新這個版本。

- 有用戶收到通知後，跑到 Reddit 上面公布這件事，結果有人自稱是新的 Bartender owner ，回覆說他們已經在兩個月前從 Ben 那邊收購了 Bartender，會在 5.0.52 版本更改軟體簽名是正常的程序，也是一次性的，請大家不用擔心。

- 結果這則留言以及後續幾則短短的留言，成為信任崩塌的導火線，因為：
    1. 大家根本不知道這個新註冊的匿名帳號是誰，但 Bartender 安裝時會取得一些系統權限，這讓很多人覺得不放心。
    2. 後續有人跟進爆料，說他發現 5.0.52 版本根本不只是有新的簽名而已，裡面還有放了 Amplitude 這個追蹤系統的追蹤程式碼，這代表著只要安裝到新的版本，可能就會開始被追蹤 Bartender 的使用資訊，但是新的團隊完全沒有主動說明這件事。
    3. 有人發現這個新註冊的公司 Bartender App LLC 背後也找不到實際的經營人是誰。

- 各種資訊爆出來，加上缺乏透明度的回應，讓很多人都直接決定刪除這個 app ，不再使用，裡面有好幾個都說自己是從 Bartender 第一代就開始用，但信任崩壞就是崩壞了。


我的想法：

- 我會決定移除的原因是：
    - 程式面，目前看起來並沒有明顯的資安疑慮。
    - 但是新的開發團隊的溝通方式非常糟糕，把原本不是問題的事情都變成了問題。事前沒有通知用戶們開發團隊已經改變、加入追蹤機制也沒有通知用戶，並且又搞砸了 Reddit 公開說明的機會，這讓我對團隊的能力以及後續交付的品質打了大問號。
    B- log 上面低品質的 SEO 行銷文章是最後一根稻草，讓我感覺到這個新團隊應該只是想撈錢，並沒有真的想維繫與打造一個高品質的軟體。
    - 加上研究一下下，發現有其他替代方案也能解決我的需求，而且我沒有沉沒成本，就很直接了當的移除 app ，跟它說再見了。

- 信任的累積很困難，要崩毀卻非常快：
    - 之前寫的 [Skiff 的案例](https://world.hey.com/mimir/a-letter-from-pj-skiff-notion-skiff-4f075074)也類似，同樣是被收購，同樣是糟糕的溝通，導致大量既有用戶不滿意、信任崩潰，不只是新的開發者與 Bartender 這個品牌喪失信任，也有許多人說再也不會相信原本開發者 Ben Surtees 未來可能會推出的任何產品（目前還沒有 Ben 的說法，失聯中）。


暫時沒有別的想法了，但有感覺這個標題會成為一個系列文😆