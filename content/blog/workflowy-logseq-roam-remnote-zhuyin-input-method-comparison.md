---
title: Workflowy, Logseq, Roam Research, RemNote 的注音輸入比較
date: 2022-02-26
updated: 2022-02-26
path: 2022/02/26/workflowy-logseq-roam-remnote-zhuyin-input-method-comparison/
taxonomies:
  categories: 
    - Tools
  tags: 
    - Logseq
    - Remnote
    - Roam Research
    - Workflowy
---

> 本文原先是我自己[在推特上的想法](https://twitter.com/WuPingJu/status/1496869085186908163)，擴寫為比較完整的文。

最近對 Workflowy 在中文輸入（注音輸入）上面的小缺點越來越不能忍受。

<!-- more -->

## 我在 Workflowy 的使用習慣

我的使用習慣很常直接用 [[ 來當成連結到某個既有頁面（節點）的快捷鍵，但是此時如果需要選字，一按 enter 選字馬上就會被 Workflowy 判定為斷行，不僅找不到我想連結的頁面，還會直接產生錯誤的新頁面，體驗不太好。

如下圖，在 Workflowy 測試注音輸入。假設我原本已經有個頁面叫做「注意力」，但我現在想要創立 / 連結到「注音」的頁面。

![](https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/testing-zhuyin-in-workflowy_EZHFLI.gif)

此時我在 Workflowy 裡面輸入「注」，然後按下 enter 要先確定選字時， Workflowy 就會自動多跳一步，直接幫我選到「注意力」這個項目，而且還會跑出多餘的贅字在旁邊。

而即使我直接輸入正確的「注音」兩個字，然後再按下 enter 選字， Workflowy 創立注音這個頁面後，還是會跑出額外的兩個贅字。

這原因應該是因為從程式設計上，就沒有重視過注音這種必須選字的輸入法吧！

隨著我工作上紀錄的資訊越來越多，也愈常需要直接透過 [[ 來連結到想連結的頁面，而 Workflowy 這個不足就很影響體驗，所以我開始測試其他幾個工具哪個有辦法取代 Workflowy 。

一開始我想到的是同樣可以免費基本使用，也一直沒使用過的 [RemNote](https://www.remnote.com/) 。

---

## 在 RemNote 測試注音輸入

結果我一測試就發現， RemNote 的注音輸入根本是災難，比 Workflowy 還要糟很多。

如下圖，從在 RemNote 測試注音輸入的結果可以看到， RemNote 基本上根本沒考慮中文的使用，不僅「暫選狀態」的字不會啟動搜尋，在處理 enter 時的方式也最糟糕，簡直無法繼續使用下去，直接放棄。

![](https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/testing-zhuyin-in-remnote_ZkPTE0.gif)

接著來測試 Logseq。

---

## 在 Logseq 測試注音輸入

[Logseq](https://logseq.com/) 的表現就好很多，輸入 [[ 後並不會馬上強制選取某個頁面，而是可以讓我舒服地選字後再去連結。

從下圖在 Logseq 測試注音輸入的結果可以看到，當我輸入「注」這個字，並且按下 enter 時，Logseq 就會搜尋「注」相關的頁面，但不會馬上幫我確認要連，我可以自己選擇要不要連。而連下去以後也不會出現多餘的贅字。

![](https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/testing-zhuyin-in-logseq_CHZMsD.gif)

而我直接輸入「注音」然後按 enter 選字後，也很順暢，總之，透過 Logseq 的 [[ 快捷鍵，我可以順順地打上我想要連結的頁面，或者也可以新創一個頁面。

最後來測試另一個鼎鼎大名的雙向連結大綱軟體： Roam Research。

---

## 在 Roam Research 測試注音輸入

有點出乎我意料的是，[Roam Research](https://roamresearch.com/) 在注音輸入的體驗上相當好，基本上跟 Logseq 是完全一樣的。（或者以時間先後來說，可能該說 Logseq 跟 Roam Research 的體驗是一樣的）

如下圖，我一樣可以先按下 [[ 啟動雙向連結的搜尋偵測，但此時即使怎麼打字、按下 enter 選字，都可以好好編輯，選完也不會跑出多餘的贅字。

![](https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/testing-zhuyin-in-roam-research_LXSYEp.gif)

---

## 結論：如果仰賴注音輸入啟動雙向連結，建議用 Logseq 或 Roam Research

我主要習慣的輸入方式是 Mac 內建的注音輸入法，所以不確定其他版本的注音，或者是其他類型的輸入法測試起來會怎樣。

但至少以上面幾個測試來說， Logseq 跟 Roam 的體驗比 Workflowy 好很多，而 RemNote 則是完全不考慮。

但如果自己在使用上並不會特別常使用 [[ 當成連結的快捷鍵，那也是還ok， Workflowy 其他層面使用起來都相當流暢滑順，還是非常推薦。

而如果是以英文為主力的話，那麼這次的比較就不會是影響選擇的關鍵了，可以再比較看看自己最有感的地方。

以我來說，這樣比較下來，最後就是決定在 Logseq 和 Roam 之間選一個來當作工作上使用的主力。
