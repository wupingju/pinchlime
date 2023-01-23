---
title: 嘗試安裝 Cusdis 但失敗
date: 2022-06-18
description: 嘗試研究了一下，發現這好像是我看不太懂，也不知道該怎麼解決的 CORS 問題。所以只好先放棄了！
path: snapshots/what-i-tried-today/tried-to-install-cusdis-but-failed
taxonomies:
  kinds: 
    - What I Tried Today
  tags: 
    - Cusdis
    - Failed Experiences
---

之前曾經有提過想試試看[輕量的評論系統 Cusdis](@/snapshots/found-lightweight-comment-system-cusdis.md)，今天突然有股動力實作，就照著 [轻量级开源免费博客评论系统解决方案 （Cusdis \+ Railway） · Pseudoyu](https://www.pseudoyu.com/zh/2022/05/24/free_and_lightweight_blog_comment_system_using_cusdis_and_railway/) 這篇的說明開始架設。

第一步註冊 Railway 帳號並部署 Cusdis ，沒問題。

第二步，把 Cusdis 的 embed code 貼到部落格的對應段落，花了一點點時間，還是完成了。

但完成以後，卻只看到那個區塊有個「空白」，卻跑不出 Cusdis 的留言框框。

原先以為是 CSS 的問題，花了好多時間在亂調整一通，都失敗。後來打開瀏覽器的 inspect ，看到有一段錯誤碼是：

```
Access to script at 'https://cusdis-production-54de.up.railway.app/js/iframe.umd.js' from origin 'https://notes.pinchlime.com' has been blocked by CORS policy: No 'Access-Control-Allow-Origin' header is present on the requested resource.
```

嘗試研究了一下，發現這好像是我看不太懂，也不知道該怎麼解決的 CORS 問題。所以只好先放棄了！

還是先維持目前的 email 評論方式吧！
