---
title: Heptabase - 透過白板促進思考與學習效率的視覺系筆記工具 - 《新 Pin 上線 ＃2》
date: 2022-02-27
updated: 2022-06-21
path: 2022/02/27/heptabase-introduction/
description: 對我來說， Heptabase 的設計是最直覺的。透過 Hepta 的設計，用戶可以專注於產生「原子層級」的卡片，之後再慢慢組織他們之間的邏輯關係或者是從屬性。
taxonomies:
  categories: 
    - New Pins
  tags: 
    - Heptabase
---

> 新 Pin 上線是 Pin 起來！網站在 2022 年嘗試的新系列文，嘗試用比較簡單的架構來介紹最近新嘗試、或有更新的工具，這些工具不一定是全新的產品服務，可能已經存在很久，只是我最近才開始使用。

**2022.06.21 更新**：本文的部分資訊有根據目前 v0.160.0 版本的內容重新微調編輯一次，歡迎先看完本篇後，再來看 6 月的更新文章：[迅速迭代功能的 Heptabase 已成為我最愛用的知識管理工具](/blog/heptabase-has-already-become-my-favorite-pkm-tool)。

---

今天要來介紹一下我從過年期間開始使用，一個多月來很喜歡，也很期待後續發展的筆記／思考／學習工具： [Heptabase](https://heptabase.com/) ！

![](https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/heptabase-banner_DfkVdH.webp)

<!-- more -->

## 為什麼想嘗試 Heptabase？

從去年 10 月左右就從[星箭廣播](https://podcast.starrocket.io/)得知 Heptabase 這個由台灣人新創團隊開發的全新生產力工具，當時還叫做 Project-Meta ，但後來…這名字變成了大家知道的那個 Meta ，於是他們改名為 Heptabase ，或者也可簡稱 Hepta 。

當時對 Hepta 的第一印象是很酷的「白板軟體」，可以在上面畫流程圖之類的，但沒有細看介紹，就送出了試用的申請，但好像沒特別收到通知，就想說算了。結果 1 月的時候傳出 Heptabase 獲得[矽谷創投 Y Combinator 投資](https://twitter.com/Heptabase/status/1482526830972518403)的消息，又讓我對 Hepta 產生興趣，再認真一看，發現非常像我曾經一度購買，興致高昂地使用，卻發現介面與操作方式過於老舊，而敗興而歸的老牌 Mac 軟體 [Tinderbox](https://www.eastgate.com/Tinderbox/)。

但看了一下創辦人詹雨安在 [YouTube 上面的介紹](https://www.youtube.com/watch?v=fxuzPgFixZ4)後，發現 Heptabase 好像比我想的更成熟、更讚，所以又送出了一次申請，而這次終於拿到了 Close Beta 的測試機會。

（備註：1月底 Heptabase 仍有限制測試名額，須留下 email 等通知，且須一次繳年費才能測試，而目前已開放 Open Beta ，但仍是須要一次繳完年費才能測試。）

---

## Heptabase 有哪些功能？

在此需要先說明的是，本文撰寫於 2022.02.27 ，目前的 Hepta 版本是 0.92.0 ，由於 Hepta 的開發速度、版本更新速度極快，所以這部分的功能可能會有些變化，但這篇文先介紹一些最基礎的、應該不會有太大變動的功能就好。

### 基本三元素 - Map, Whiteboards, Cards

這三個是 Hepta 裡面的三個層級，每個層級有不同的功能以及呈現方式，接下來一個一個介紹：

**Map** 

Map 只有一個，放置所有的 Whiteboards，在 Map 上面可以自由移動 Whiteboards ，也可以調整大小，Hepta 團隊就曾分享過[把 Whiteboards 依照某些特定的圖像如地圖來排列](https://twitter.com/Heptabase/status/1463120531176132620/photo/1)（如下圖），透過固定的位置來增強圖像方面的記憶與聯想。

![](https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/heptabase-canada-map_AG4gDW.webp)

**Whiteboards** 

Whiteboards 可以有無限個，每個 Whiteboard 可以想成是一個特定且獨立於其他 Whiteboards 的主題，裡面可以放置不同的 Cards ，而且會有專屬於這個 Whiteboard 的「屬性」紀錄。例如， Cards 之間的關係、顏色、擺放位置等等。

而在 v0.143.0 版本後， Whiteboards 裡面還可以再建立不同的 Whiteboards ，藉此更有效率地整理不同內容的「層級與結構關係」。

**Cards** 

Cards 是 Heptabase 裡面最基礎的元素，每張 Card 目前可以放文字、圖片、程式碼、數學公式、To-do List 等等，文字方面支援 Markdown 語法以及雙欄的編輯界面，也支援現在流行的 slash commands ，就是只要輸入一個 / 就可以叫出一些文字編輯的選項。

**Connections & Colors** 

當不同的 Cards 被放到 Whiteboard 時，可以用內建的連接工具來為 Cards 之間建立箭頭或連接線，也可以在連線中間附註，效果類似於那些心智圖軟體。而 Cards 在 Whiteboard 中可以縮起來只顯示標題或完全展開，也可以切換顏色（目前 Light & Dark mode 各有預設的 8 種）

如下圖，這是我自己某個 Whiteboard 裡面的一個小角落。

![](https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/heptabase-connections-colors_a9FzGG.webp)

---

### 側邊欄的 Timeline, Tags, Card Library

![](https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/heptabase-sidebar_pvg3bl.webp)

_上圖為 Heptabase 的側邊欄。_

**Timeline** 

Heptabase 還有一個單獨的介面叫做 Timeline ，點開後就會出現一個以日期為核心的紀錄頁面，在這邊能夠快速擷取想法製成 Cards ，也可以快速幫 Cards 標註不同的 tags ，或者是直接從 Timeline 把卡片加入特定的 Whiteboard。

**Tags**

在 Tags 介面可以看到所有目前有的標籤，以及擁有該標籤的卡片們。透過這樣的選取可以直接把同一標籤的卡片們同時打開在右側邊欄編輯，也可以加入特定的白板。

**Card Library** 

Card Library 就是卡片們待的地方，在這邊同樣可以透過 Tags 來篩選卡片，更可以透過 Whiteboards 來篩選卡片。這邊就得要提到 Hepta 最核心的概念之一： **一張卡片可以出現在不同的 Whiteboards**。

---

### 同樣的卡片可以出現在無數個白板

過往的筆記工具裡面，大多都是線性的結構，一則筆記必須放置在一個固定的資料夾，或許可以用 tags 來建立不同屬性的分類，但一個蘿蔔大多就是配一個坑。

但有時候，同樣的內容，可能會需要被放置在不同的資料夾或筆記本裡面，例如我今天若寫了一則筆記介紹「複利效應」，我可能會想把這則筆記的內容用在、放在「財產管理」、「持續寫作」及「持續運動」這些筆記本或專案裡。

有些軟體做得好一點，像是[我曾介紹過的 DEVONthink](/2021/01/24/devonthink3-introduction/) 可以用 “Replicate” 的功能把某個檔案建立分身，放到其他資料夾。而另一個[曾經介紹過的 Workflowy](/2022/01/25/workflowy-backlinks-mirror-board/) 則是可以用 “Mirror” 的功能，把特定的節點（筆記）鏡像到別的節點，達到同步更新的效果。

另外，Roam Research 或是 Logseq 這些軟體也可以做到 “Block embed” 的功能，把某則內容鑲嵌到另一則內容底下，來完成「一個筆記出現在不同地方」的效果。

但是對我來說， **Heptabase 的設計是最直覺的**。

因為在 Hepta 裡面，用戶不需要去理解各種新的名詞或功能，不用懂 Replicate, Mirror, embed 這些更像是「附加」的功能，在 Hepta 裡面，只要記得一件事：

**每張卡片的內容專屬固定，但可以同時出現在不同白板裡**。

而在白板中添加或移除卡片的方式也相當友善直覺，也把從白板中「移除」（close）跟完全「刪除」（delete）卡片兩件事做出了明顯的區隔。

透過 Hepta 的設計，用戶可以專注於產生「原子層級」的卡片，之後再慢慢組織他們之間的邏輯關係或者是從屬性。

---

### Heptabase 的卡片也可以雙向連結

這一兩年來，筆記軟體幾乎都要加上雙向連結的功能了， Heptabase 也不例外，在卡片編輯介面可以方便地透過 @ 或是 [[ 連結到既有的卡片，或者是建立新的卡片。

而建立連結後，被連結的那張卡片的「 Card Info 」介面可以看到有哪些卡片連結到這張卡片，相對應的文字情境也會一併呈現，藉此可以迅速回憶起自己連結到這張卡片的「上下文情境」是什麼。

---

### Heptabase 的公開分享功能

在近期某次版本的更新後，Hepta上線了公開分享的功能，只要按一下 share ，就可以把特定白板公開分享，例如創辦人就分享了他的 [How to start a startup白板](https://app.heptabase.com/w/b6d57c892e2c099a4835431b45aa2d11264ddcdb3186b7acb3efc400632b8df5)，相當值得瀏覽參考看看！

---

## 可以怎麼使用 Heptabase？

有些人拿來學習新知識，有些人拿來規劃專案，有些人拿來整理與組織筆記和想法， Heptabase 有很廣泛的應用可能性。

目前官方已經有整理豐富的 [Use Cases](https://heptaplatforms.notion.site/Use-Case-How-people-are-using-Heptabase-70c85a0c686945218427618549087629)可以參考，以我自己來說，我目前的用法主要放在 6 月更新的[迅速迭代功能的 Heptabase 已成為我最愛用的知識管理工具](/blog/heptabase-has-already-become-my-favorite-pkm-tool) 這篇文裡面，節錄如下：

> 每日紀錄與連結我的各種想法，再將它們放到 [Pin 起來的筆記與想法快照](https://notes.pinchlime.com/)

> 在閱讀文章和書籍後製作閱讀筆記卡片，並直接在卡片上面透過將文字加粗、 highlight 以及寫筆記來進行「漸進式總結」。

> 專門用一個白板來收集部落格與[電子報](https://pinchlime.substack.com/)的主題靈感，也用一個白板來擔任我的「工作台」，放置那些待處理、待加工的草稿卡片，並且直接在 Heptabase 裡面撰寫長文，撰寫的過程會將需要參考的卡片放到側邊欄對照。

---

## Heptabase 要付費嗎？

如前面一開始講到的，Heptabase 目前仍處於 Open Beta 的階段，但團隊選的策略是「慢慢地服務核心用戶並快速迭代版本」，因此目前只有開放繳年費使用的方案。年費是 83.88 美金，以目前匯率來說約為 2500 台幣。而根據官網的資訊，月費方案應該今年的某個時間點會開放，就再拭目以待囉！

如果是對於價格較為在意的人，或許可以等到月費方案上線後再來用用看。

但若是喜歡嘗試不同生產力工具、對上述介紹（或其他地方的介紹）很心動、或者單純想支持台灣團隊的產品的人，我就蠻推薦可以刷下去試試看，對我來說，目前尚未宣布進入「正式版」的 Heptabase 就已經是個超級棒的知識管理工具，在嘗試與學習的過程中也有了許多新的想法，這錢花得非常值得。

另外，也很推薦 Heptabase 的 [Discord 社群](https://discord.gg/KAkXjPX8Yn)，目前對我來說是個能夠舒服吸收資訊的狀態，有蠻好的互動風氣。

---

## 小結 - 光是設計理念就令我買單的 Heptabase

用了 Heptabase 一個多月的感想是：每天幾乎都在期待今天又要更新什麼新功能，我記得我開始用的時候應該是 0.58.0 之類的版本，現在已經到 0.92.0 了，中間新增了許多實用的功能。

而且從 Discord 裡面有個頻道叫 “our-vision” ，可以看到 Hepta 背後有一整套我很欣賞的設計理念，即使暫時不用 Hepta ，都很推薦進去看看創辦人 Alan 的論述，我自己是相當有收穫！

期待未來能夠繼續寫更多 Heptabase 的介紹及分享文章！

---

看更多關於 Heptabase 的文：
- [用 Heptabase 進行卡片寫作的心得](/2022/03/07/implementing-zettelkasten-in-heptabase/)
- [迅速迭代功能的 Heptabase 已成為我最愛用的知識管理工具](/blog/heptabase-has-already-become-my-favorite-pkm-tool)