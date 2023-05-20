---
title: 為何我想停用 Cusdis 但卻又反悔？
date: 2023-02-08
description: 在缺乏通知的問題解決後，我決定還是繼續使用 Cusdis ，直到我找到更好的方案為止。
path: snapshots/why/why-did-i-want-to-stop-using-cusdis
taxonomies:
  kinds: 
    - Daily Why
  tags: 
    - Cusdis
    - Remark42
    - Comment System
---



昨晚發布了一篇 [測試了 Chirpy 這個留言系統](@/snapshots/tried-tried-chirpy-comment-system.md) ，在裡面我提到：

> 而我也因為這次 Chirpy 的嘗試，決定把原本網站安裝的留言系統 Cusdis 給關閉了

不過，就在我把 Cusdis 從網站移除後過沒多久，事情發生一些變化，我決定再繼續使用它。

這篇就來簡單記錄一下，為何我原本想要停用 Cusdis ，後來又決定繼續使用。

### 為何我原先打算停用 Cusdis ？

我從去年 6 月安裝 Cusdis 這個留言系統以來，就一直對它有一點點不滿意。主要的原因是，它在接收到使用者留言後的通知系統不太靈光，雖然 Cusdis 官方[有提供 email 通知的設定教學](https://cusdis.com/doc#/features/notification)，但我好像只有剛安裝好的時候有成功過一兩次，之後都沒有辦法觸發 email 通知。

而另一個進階的 [Webhook 通知](https://cusdis.com/doc#/advanced/webhook)功能也無法設定成功，照著教學跟官方的 telegram chatbot 對話後也沒有任何反應。

在沒有通知的狀況下，我必須要一直手動到後台查看網站有沒有新留言，這對我來說是蠻煩瑣的一件事。

另外，據我理解，使用者留言後，即使有留下 email 資訊，也無法收到「自己的留言有新回覆」的通知。所以讀者也沒辦法很輕易知道自己的留言有沒有被我回覆了。

所以昨天在試用 Chirpy 後，一個衝動就打算把 Cusdis 先關掉，回復到只能透過 email 聯繫與討論的原始狀態。

但我把 Cusdis 移除後，問了在[網站](https://www.pseudoyu.com/zh/)上也有在用 Cusdis 的推友 [Pseudoyu](https://twitter.com/pseudo_yu) 他是否也有遇到通知故障的問題，結果熱心的 Yu 提供了我 Webhook 的解方！

---

### 為何我又決定繼續使用 Cusdis ？

假設有人也遇到類似的問題，我不確定這個解方對你有沒有幫助，但至少解決了我的問題，所以我還是來分享一下，主要的設定步驟為：

1. 先在 telegram 加入[這個 chatbot ](https://t.me/userinfobot)，跟他對話後，記下他提供的 ID

2. 把 ID 填入這串網址最後的 {ID} 欄位 `https://tg-bot.cusdis.com/api/hook/{ID}`

3. 把填完 ID 的網址，貼到 Cusdis 後台填入 Webhook 的輸入框

4. 再加入[官方的 chatbot](https://t.me/CusdisBot) 

全部都完成後，就成功了！只要有新的留言出現，官方的 chatbot 就會通知我有人留言，並且提供我一個 approve link ，如下圖：

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/cusdis-approve-link_C1sZmK.webp" data-fancybox data-caption="cusdis-approve-link">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/cusdis-approve-link_C1sZmK.webp" loading="lazy" alt="cusdis-approve-link" align="center" />
</a>

這個 Link 點下去就，就會跳出一個無須登入的視窗，可以審核留言，也可以直接以網站主的身分回應留言。（當時會選用 Cusdis 的其中一個原因就是覺得這個 link 很聰明也很方便，但一直用不了）

不過，我測試的結果是，按下連結後，會跑出 invalid_token 的錯誤。

但此時熱心的 Yu 又提供我解決方案，他說可能要在部署 Cusdis 的 Vercel 那邊設定環境變數，要把 Host 跟 NEXTAUTH_URL 這兩項都設定為自己的 cusdis url 。

我原先好像只有設定到後者，沒有設定到 Host ，在補上設定，並且重新在 Vercel 上部署 Cusdis 後，也可以正常使用 approve link 了！

因此在缺乏通知的問題解決後，我決定還是繼續使用 Cusdis ，直到我找到更好的方案為止。

---

### 我理想中的留言系統是怎樣？

在這個過程中我也思考了一下，對我來說留言系統的最佳解可能會需要有哪些功能？

想了一下，答案應該是之前 Reorx 在更换[博客评论系统](https://reorx.com/blog/blog-commenting-systems/)這篇文裡面有推薦過的 [Remark42](https://remark42.com/) 。

因為它完全滿足我對留言系統的基本功能期待，如下：

* 有匿名留言的功能

* 要用 Twitter, Github, Telegram, FB, Google 等不同登入方式也可以

* 也可以用 emal 登入

* 支援 markdown

* 可以串接 telegram 或 slack 通知網站主

* 可以 email 通知留言者他們的留言被回覆

* 輕量、注重隱私

雖然我之前研究了一下，發現我好像還沒有能力自己部署，但未來一定要找機會嘗試換換看！