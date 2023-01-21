---
title: 開始使用 Beta 版的 Umami Cloud
date: 2023-01-01
updated: 2023-01-01
path: blog/started-using-umami-cloud
description: 設定超級無敵簡單，只要輸入要追蹤的網域，就會給你一段程式碼，只要把這段程式碼放到網頁的 <head> 區塊就可以開始追蹤了。Heptabase 裡面處理與輸出。
taxonomies:
  categories: 
    - Tools
  tags: 
    - Umami
extra:
  image: https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/umami-cloud-beta_xN33tf.webp
---

這個部落格的流量追蹤與統計，是透過 [Umami](https://umami.is/) 這個開源的工具進行的。

我在 2022 年 6 月時[從 Google Analytics 轉向使用 Umami](@/snapshots/tried-tried-to-install-umami-on-my-websites.md)，當時照著教學文章一步一步照著做，就透過 [Railway](https://railway.app/) 這個 PaaS 平台完成了設定，在 Railway 上面建立了一個資料庫，並部署 Umami 服務。

從那之後，我很順利地累積了半年多的數據，Umami 的介面乾淨、對於一個個人網站來說該有的數據都有，我很滿意。

不過在 12 月底時，我收到 Railway 這邊的用量通知，說預計費用已達到 8 塊多美元，而 Railway 一個月的免費額度只有 5 美元而已。

看起來不太妙，於是我開始想有沒有什麼替代方案，畢竟我目前還沒有想要在流量紀錄上面每個月持續花錢。

<!-- more -->

我第一步找的是 Umami 的官網，想看看他們有沒有其他推薦的解決方案，結果發現官網的 Pricing 頁面，寫著「Umami Cloud BETA」的字樣，看起來是可以直接使用 cloud 版本。

<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/umami-cloud-beta_xN33tf.webp" loading="lazy" alt="umami-cloud-beta" align=center />

於是我就趕緊註冊，然後發現設定超級無敵簡單，只要輸入要追蹤的網域，就會給你一段程式碼，只要把這段程式碼放到網頁的 <head> 區塊就可以開始追蹤了。

而我也一樣透過 Netlify 的 [Snippet Injection 功能](https://docs.netlify.com/site-deploys/post-processing/snippet-injection/)來放置這段代碼，整個過程從註冊完 Umami，產生追蹤碼，再到 Netlify 設定完，不超過 5 分鐘。


若這個月沒什麼意外，我可能會先停掉自架版本的 Umami ，先用一陣子免費 BETA 版的 Umami Cloud，未來再依據定價狀況且戰且走了！
