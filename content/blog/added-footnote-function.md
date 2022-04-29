---
title: 部落格新增了 Footnote 註腳的功能
date: 2022-04-29
updated: 2022-04-29
draft: true
description: 
path: blog/added-footnote-function
taxonomies:
  categories: 
    - Pinchlime
  tags: 
    - Zola
---

昨天在 Zola 的官方討論區看到[有人在提問某個程式碼的問題](https://zola.discourse.group/t/getting-markdown-without-paragraph/1282)，但發現他那段程式碼的目的是想要自訂 footnote ，也就是註腳的功能，這就讓我很感興趣。

雖然我一開始完全看不懂他的 code ，但還是留言詢問了一下可否分享他寫的完整代碼給我，結果他真的很好心地分享，還寫了一段說明。我簡單照著做之後，就真的實現了這個功能，覺得這對我來說是個很有意義的功能，因此想簡單分享（搬運）一下他的做法。

<!-- more -->
---

## Footnote 功能是什麼？

簡單來說，就像這樣{{ ftnt_refs( idxs=[1]) }}。

在學術文件或研究報告裡面應該很常見到註腳，通常用於補充解釋本文{{ ftnt_refs( idxs=[2]) }}，或者是標註參考資料的來源。而許多 pdf 或者網頁也都可以點選註腳後跳到特定段落，但對於 Zola 這種靜態網站產生器來說，官方文件裡面沒有的功能，我都先當成沒有。

之前也曾嘗試過像是 \[^1] 這樣的方式，



---

{% ftnt( idx = 1 ) %}
註解可以放在文章最下面，並且可以透過超連結和返回的按鈕跳轉。
{% end %}

{% ftnt( idx = 2 ) %}
我的理解是，這個解釋如果放在本文裡面會讓本文顯得太繁瑣，但又是一個最好可以提供，或者說，作者很想講的補充，所以就會放一個註腳，把比較完整的話放在註腳裡面，而讓本文維持語意的簡潔與完整。
{% end %}