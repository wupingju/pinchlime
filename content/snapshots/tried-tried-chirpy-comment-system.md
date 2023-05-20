---
title: 測試了 Chirpy 這個留言系統
date: 2023-02-07
updated: 2023-02-08
description: 可能是因為目前 Chirpy 還在前期開發階段，雖然核心的留言功能做的蠻簡單使用，也有外加的追蹤（倘若有這方面的需求的話，或許兩個融合起來一次搞定還蠻不錯的），但正好不太符合我的需求
path: snapshots/what-i-tried-today/tried-chirpy-comment-system
taxonomies:
  kinds: 
    - What I Tried Today
  tags: 
    - Chirpy
    - Cusdis
    - Plausible
---


今天發現 [Chirpy](https://chirpy.dev/) 這個開源、也是主打隱私的留言系統，看了一下文件發現好像非常簡單安裝設定，不用自己架設資料庫。而且現在還在 Open beta 階段，使用是免費的。

於是晚上就花了一些時間測試使用，真的非常簡單安裝，只要註冊帳號後，開設專案，設定網域，接著把兩段程式碼加入自己的網站，就可以開始留言了。

留言的介面如下，我覺得還算乾淨好看。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/chirpy-demo_BaPVgb.webp" data-fancybox data-caption="chirpy-demo">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/chirpy-demo_BaPVgb.webp" loading="lazy" alt="chirpy-demo" align="center" />
</a>

我在測試時，主要是想測試匿名留言的功能，以及管理者的後台會怎麼通知。

前者是我希望盡可能降低留言的阻力，因此會想要有的功能。

而後者是我希望有盡量清楚、不會漏接的通知系統，這樣我收到留言後就可以儘快回覆。

測試後的結果是，這兩點都可以做到，可是效果都不像我想像中那麼好。

在匿名留言方面，留言完畢後，匿名留言者會被導到 Chirpy 的主頁，此時身分是一個匿名的亂碼帳號，他可以接著填寫個人資訊或者是開啟 Chirpy 專案。

咦？為何留言者要開啟專案？

我可以理解這可能是 Chirpy 想要增加使用者的 base ，但這體驗的路徑太奇怪了，完全可以想像留言者留言後的錯愕以及不知所措。

而在後台通知方面，目前好像沒有一個列表或資料庫的介面，只有 notifications 而已，感覺稍微有點不足。

另一個蠻微妙的點是， Chirpy 內建整合了 [Plausible](https://plausible.io/) 這個也是注重隱私的追蹤工具，所以在 Chirpy 的後台介面，最核心可以查看的資訊是頁面的統計數據。

但，這好像不是我想要的功能，因為我已經有設定 Umami 的追蹤了。

總之，可能是因為目前 Chirpy 還在前期開發階段，雖然核心的留言功能做的蠻簡單使用，也有外加的追蹤（倘若有這方面的需求的話，或許兩個融合起來一次搞定還蠻不錯的），但正好不太符合我的需求。

而我也因為這次 Chirpy 的嘗試，決定把原本網站安裝的留言系統 Cusdis 給關閉了，這就下一篇再來分享。

（結果一天後就決定不關閉，要繼續使用 Cusdis，詳見： [為何我想停用 Cusdis 但卻又反悔？](@/snapshots/why-why-did-i-want-to-stop-using-cusdis.md)）