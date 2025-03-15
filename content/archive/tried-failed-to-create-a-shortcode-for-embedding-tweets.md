---
title: 嘗試製作一個嵌入 Tweets 的 shortcode 失敗
date: 2023-01-24
updated: 2023-01-24
description: 我發現 Twitter 官方好像沒有提供 iframe 的嵌入方案。不過，Twitter 官方提供的方式也不能說困難。
path: snapshots/what-i-tried-today/failed-to-create-a-shortcode-for-embedding-tweets
taxonomies:
  categories: 
    - Pinchlime
extra:
  page_type: archive
---

本週在編輯第 16 期電子報的時候，嘗試了 substack 貼上推文串的功能，覺得效果蠻好的、也很直覺。

因此就起心動念想在網站上面也做一個類似的功能。

我首先想到的是 Zola 的 Shortcode 功能，它有點類似模板，我想說可以設定成某種固定的 iframe 段落，只要設定推文的網址，就能自動渲染產生。

但我發現 Twitter 官方好像沒有提供 iframe 的嵌入方案。

不過，Twitter 官方提供的方式也不能說困難，詳見 “[How to embed a Tweet on your website or blog](https://help.twitter.com/en/using-twitter/how-to-embed-a-tweet)”，只要在想嵌入的推文點幾下，就會產生完整的嵌入代碼了。

試著操作了一下，發現雖然步驟比我想像中還要多幾步，但也不困難，只要每次想嵌入時，到 <https://publish.twitter.com/#> 貼上對應的網址，就可以產生嵌入代碼了。


實際運作的效果可以參考下方這則我的推文：

<blockquote class="twitter-tweet"><p lang="zh" dir="ltr">2023 新年快樂！<br><br>也來分享一下那些在 2022 年開始進入我工作流的好工具們，完整的介紹可以看連結內的文章！<br><br>文內會依使用的情境與工作流，把工具分為三大類別，分別是：「個人知識管理」、「內容輸出與分享」與「工作記錄與溝通」。<br><br>而推文串則有各類內容的摘要！<a href="https://t.co/seUpT3MKJr">https://t.co/seUpT3MKJr</a></p>&mdash; PJ Wu 吳秉儒 (@WuPingJu) <a href="https://twitter.com/WuPingJu/status/1609834874676051968?ref_src=twsrc%5Etfw">January 2, 2023</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

整體來說覺得還算堪用了！

不過這樣做會拖累網頁的效能表現，所以想了想，我應該只會在必要的地方嵌入吧。