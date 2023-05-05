---
title: 開始使用 Cloudflare Web Analytics
date: 2023-05-05
description: 看了一下以後發現 Cloudflare Web Analytics 好像還不錯！因為他有下列最在意的優點：免費使用、重視隱私。
path: snapshots/what-i-tried-today/tried-to-use-cloudflare-web-analytics
taxonomies:
  kinds: 
    - What I Tried Today
  tags: 
    - Cloudflare
    - Umami
    - Netlify
extra:
  image: https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/cloudflare-web-analytics_Ju2RGs.webp
---
<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/cloudflare-web-analytics_Ju2RGs.webp" loading="lazy" alt="cloudflare-web-analytics" align=center />

今天早上收到我在使用的追蹤工具 Umami 的通知，說 Umami Cloud 即將結束 Public Beta ，要開始正式上線，這也意味著要開始收費。

看了一下公布的[定價內容](https://umami.is/pricing)，發現有點尷尬。 Free tier 每個月有限制 10,000 次的 page views ，以我過去幾個月的數據來看，蠻有機會超過。但下一個 tier 就要每個月 9 美元，並且有每個月 10 萬次的 page views ，這對我來講又太多。

因此我開始研究替代方案。先前有研究過 [Fathom](https://usefathom.com/pricing) 或者是 [Plausible](https://plausible.io/#pricing) ，最便宜的也都要每個月 9 美元，而今天有個推友推薦我的 [Simple Analytics](https://www.simpleanalytics.com/pricing) ，也是要 9 美元。看來看去我想說，如果都要付錢的話，那好像要研究一下其他幾個有沒有比 Umami 更好。

但在這時我看到 Simple Analytics 的頁面上有與其他產品的比較，[其中一個是 Cloudflare](https://www.simpleanalytics.com/blog/why-simple-analytics-is-a-great-alternative-to-cloudflare-web-analytics) ，看了一下以後發現 [Cloudflare Web Analytics](https://www.cloudflare.com/web-analytics/) 好像還不錯！

因為他有下列幾個我最在意的優點：

* 目前可以免費使用，並且只要貼上一段 js code 就可以直接開始記錄。
* 重視隱私， Cloudflare 有說明他們不會追蹤用戶的 IP 以及 “fingerprint”，也不紀錄 Cookies 。

至於其他追蹤工具各式各樣的分析或即時追蹤功能，我好像都不太需要，我只想要重視隱私，並且能夠有八九成準確紀錄流量的工具就好，看起來 Cloudflare 正好符合這個需求。

於是我就安裝了，一樣是透過先前提過的 [Netlify 的 snippet injection 功能](https://pinchlime.com/blog/embed-tracking-code-for-static-websites-with-netlify-snippet-injection-feature/)來埋設追蹤碼，非常簡單，一分鐘內就完成安裝並開始追蹤。

追蹤幾個小時下來，看起來數據儀表板也是該有的都有，包含流量資訊、各頁面的分別數據、 Referers 等等。

<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/cloudflare-web-analytics-dashboard_0hLUzO.webp" loading="lazy" alt="cloudflare-web-analytics-dashboard" align=center />


接下來打算讓他跑個一兩週看看數據跟 Umami 追蹤的有沒有什麼不一樣，若沒有太大落差，應該就會正式轉向 Cloudflare 了！