---
title: Workflowy 的雙向連結、鏡像以及看板功能
date: 2022-01-25
path: 2022/01/25/workflowy-backlinks-mirror-board/
description: 在這過程中，雙向連結的功能，是讓每日紀錄能夠準確連結到特定專案紀錄資訊，也讓特定專案跟日期產生連結（之後查找就會很方便）。 鏡像的功能，則是讓某資訊能夠同時出現在不同地方，也能同步更新。 而看板的功能，則是可以把不同專案，但同屬性（例如專案進度或待辦）的資訊彙整在一起，時刻留意及更新。
taxonomies:
  categories: 
    - Tools
  tags: 
    - Workflowy
    - Outliner
---

本文一開始發布於自己的[個人推特推文串](https://twitter.com/WuPingJu/status/1482551447359086592)，簡單改寫後轉錄於此部落格。

從一月初以來，將工作上的逐日紀錄交給 [Workflowy](https://workflowy.com) 這個**無限層級的大綱軟體**來做，從我初接觸 Workflowy 以來也好幾年了，之間斷斷續續地使用，偶爾被不同的生產力工具吸引走，但都還是會找到想用 Workflowy 的理由，這個軟體真的有魔力，會讓人一直用下去。

<!-- more -->

## demo 頁面

本文還沒有要介紹 Workflowy 的基本功能，而是直接來介紹 Workflowy 隨著這一兩年的流行潮，也開發出的雙向連結功能，以及其他幾個優秀功能的搭配使用場景。

首先可以看我透過 Workflowy 的分享功能，創造的 [demo 頁面](https://workflowy.com/s/demo/vQWTHz5gMjHqCwUE)（見下圖） ，這個頁面是個簡單的純瀏覽示範，由三個區塊組成，第一個區塊是追蹤看板，第二個區塊是每日紀錄，第三個區塊是專案紀錄。demo 頁面中每個節點或者有底線的連結都可點。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/workflowy-demo-1_V5RjQF.webp" data-fancybox data-caption="workflowy-demo-1">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/workflowy-demo-1_V5RjQF.webp" loading="lazy" alt="workflowy-demo-1" align="center" />
</a>

不過在介紹上，我的順序會先講第三個區塊的專案紀錄。

每當有一個專案要開啟時，我就會開一個專案單獨的欄位，例如目前demo的專案A、專案B、專案C，這些欄位可以想成是這個專案的專屬資料夾，可以供**其他專案**以及**每日紀錄**來連結使用。

---

## 產生連結

在每日紀錄的區塊，用法就是每天開一個節點，當天若某專案有進度，就直接用 [[ ]] 連到該專案，並且記下相關資訊。例如我在 1月7日的節點底下，連結到了專案A，並且開了一個項目叫做「例行會議追蹤」（如下圖）。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/workflowy-demo-2_7BJYV0.webp" data-fancybox data-caption="workflowy-demo-2">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/workflowy-demo-2_7BJYV0.webp" loading="lazy" alt="workflowy-demo-2" align="center" />
</a>

此時若這個紀錄是重要的，那就直接把它用**鏡像(mirror)** 的功能連回「專案紀錄」區塊中，該專案的指定欄位，例如我在「專案紀錄->專案A->專案A例行會議追蹤」紀錄每次的追蹤會議，所以就在這項下面連結回1月7日的追蹤紀錄。

---

## 每日紀錄與專案紀錄的串連

這樣一來的效果，就是讓「每日紀錄」的區塊跟「專案紀錄」的區塊串連在一起。

在「每日紀錄」的欄位，有每個專案的完整記錄和討論，而在「專案紀錄」的欄位，則是可以一覽所有專案的重要進展跟資訊（當然可以再自己設置不同層級、或者是上 tag。 如圖，我把這兩大頁面的 demo 排在一起，可以稍微感受一下他們之間的連結性。）

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/workflowy-demo-3_ncdggB.webp" data-fancybox data-caption="workflowy-demo-3">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/workflowy-demo-3_ncdggB.webp" loading="lazy" alt="workflowy-demo-3" align="center" />
</a>

兩大區塊彼此有關，但各自有各自的重點。

---

## 追蹤看板

這時再回過頭來講第一個「追蹤看板」，「看板」是 workflowy 的功能之一，可以把任何一個列表轉換成看板模式，而我在這個 demo 的用法，就是把專案A、專案B、專案C的「專案Ｏ例行會議追蹤」這個點，都用鏡像的功能連到「追蹤看板」，這樣一來，每當我把每日紀錄的專案會議追蹤，鏡像到該專案的欄位後，又會自動再鏡像到追蹤看板，即時更新。（如下圖）

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/workflowy-demo-4_fz3Qbc.webp" data-fancybox data-caption="workflowy-demo-4">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/workflowy-demo-4_fz3Qbc.webp" loading="lazy" alt="workflowy-demo-4" align="center" />
</a>

簡單來說，看板的好處是能夠將同一屬性但不同日期或專案的資訊有效地整合在一起。

---

## 小結

在這過程中，**雙向連結的功能**，是讓每日紀錄能夠準確連結到特定專案紀錄資訊，也讓特定專案跟日期產生連結（之後查找就會很方便）。 **鏡像的功能**，則是讓某資訊能夠同時出現在不同地方，也能同步更新。 而**看板的功能**，則是可以把不同專案，但同屬性（例如專案進度或待辦）的資訊彙整在一起，時刻留意及更新。

透過這樣子的設計，我已經紀錄了近一個月的工作日誌以及專案資訊，即使一天同時有好幾個專案有新的更新，或是需要翻找某一天我們對於這個專案有什麼討論或動作，也都能很快找到想要的資訊， Workflowy 真的是很棒的工具，推薦使用！
