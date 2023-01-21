---
title: 迅速迭代功能的 Heptabase 已成為我最愛用的知識管理工具
date: 2022-06-21
updated: 2022-06-21
path: blog/heptabase-has-already-become-my-favorite-pkm-tool
description: 目前的 Heptabase 已經不單純是個「有潛力的工具」，而是已經可以承載複雜知識管理任務的產品了。甚至可以說，它目前就是所有選擇裡面最符合我需求的、最棒的工具。
taxonomies:
  categories: 
    - Tools
  tags: 
    - Heptabase
---

<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/heptabase-changelog-screenshot_qRE6ix.webp" loading="lazy" width = "768" height = "478" alt="heptabase-changelog-screenshot" align=center />

*這張圖來自 Heptabase 的 [官方 changelog 頁面](https://heptaplatforms.notion.site/Heptabase-Version-Changelog-29ea6db0b4ff4127b83d454742de86ad)，點進去可以看到每個版本大致上改了什麼東西。*

---

Hi！

好久沒有寫 Heptabase 的文了，從上一篇 [用 Heptabase 進行卡片寫作的心得](@/blog/implementing-zettelkasten-in-heptabase.md) 至今三個多月，已經過了超過 60 個版本號的更新（現在是 v0.160.0），這期間我曾一度停用 Heptabase 兩個月，一方面是覺得有些想要的功能還沒有，用起來不太順手，另一方面是當時忙於架設自己的部落格和 wiki 頁面。

但在 5 月底，我重新開始大量使用 Heptabase ，這次不僅只是單純回來逛逛玩玩，而是開始將自己的「第二大腦」從 Logseq 移出，**全部都放到 Heptabase 上面**。

這麼做的原因是，這幾個月來， Heptabase 推出了幾個對於知識管理來說相當重要的功能更新，同時也不斷地在提升整體的使用體驗。

我覺得目前的 Heptabase 已經不單純是個「有潛力的工具」，而是已經可以承載複雜知識管理任務的產品了。甚至可以說，它目前就是所有選擇裡面**最符合我需求的**、最棒的工具。

以下先從此時此刻的角度回頭看，過去幾個月更新了哪些重要的功能，以及我怎麼看待跟使用這些功能。因為版本實在是不少，我有簡單根據幾個不同的體驗領域來分類。（版本號後面的連結都會直接連到 Heptabase 的[官方 changelog 頁面](https://heptaplatforms.notion.site/Heptabase-Version-Changelog-29ea6db0b4ff4127b83d454742de86ad)，上面會有簡單的附圖或影片，這邊就不重複貼了！）

而在回顧完不同版本的功能後，會再簡單講一下目前我怎麼用 Heptabase ，以及他在我自己知識管理系統上的定位。

<!-- more -->
---

## 分類與組織卡片的體驗提升

* v0.143.0 [Whiteboard: Nesting & Linking](https://heptaplatforms.notion.site/Whiteboard-Nesting-83cfa6d205f84d7ea043db15c194d1b7)

5 月底更新的 Nested Whiteboards （巢狀白板、層級化白板、嵌套白板）是我認為這幾個月來 Heptabase 最重要的一次更新，也是在看到這次更新後，我之前覺得 Heptabase 最缺乏的地方補足了，最需要的功能有了，才決定開始認真在 Heptabase 裡面累積我的知識與想法。

這邊簡單說明一下為何我這麼看重這個功能。

原先的 Heptabase 如同最早部落格[那篇介紹](@/blog/heptabase-introduction.md)所說的，主要可以分成 Map, Whiteboards, Cards 這三個元素，這三個元素彼此有明確的層級關係，後者只能屬於前者，而 Map 只有一個，這樣扁平的層級架構讓整個 Heptabase 的運作相當受限。

舉例來說，如果我想在 Heptabase 裡面記下每日的 daily notes ，那麼我可能會每天開一張卡片，上面寫著當天的日期。一個月過去，我可能累積了 30 張卡片，我想將它們收納在一起，於是我開了一個「月份」的白板。如果只有一兩個月還好，但如果要每天更新，持續累積呢？我的各月份白板會逐漸吃掉那個唯一的 Map 的空間。

同樣的情境可能會出現在任何稍微複雜一點的領域裡面，這些領域大多有一個核心的名詞可以來描述他們，例如「crypto assets」，而裡面可能會再有一些中規模的集群，例如「cryptocurrencies」、「stablecoins」、「privacy coins」、「NFT tokens」等等，這些中規模的集群裡面還會有各自的子項目。例如穩定幣還會有「演算法穩定幣」或者是「資產支撐穩定幣」，但倘若整個系統的檔案架構只能有 Map （我關注的所有領域）、Whiteboards （我有興趣的各種主題）、卡片（各種主題下的相關概念），那麼就有點難好好地承載與分類這些複雜的資訊。

所以在新手上路 onboarding 時，就有特別向團隊回饋說，希望有 nested whiteboards 的功能。我覺得這樣做不僅可以更有效率地應用整個地圖，也可以更好地整理複雜的資訊與知識。

在等了幾個月後， Heptabase v0.143.0 版的這次更新沒有讓我失望，上線的 Nested Whiteboards 非常直覺好用：

* 在白板裡面可以創立新的子白板，這些子白板可以跟卡片們並排在一起

* 白板可以連結到白板（但卡片還無法連到白板）

* 可以一次拖曳許多卡片到子白板裡面

透過這次的更新，較複雜概念的拆解與組織變得容易很多，也可以更輕易地執行「歸檔」或「分類」這樣的工作。例如我最近若對於穩定幣的發展特別有興趣，我可能會在意起穩定幣的機制、穩定幣的監管、穩定幣的用途等等。

我可以先逐步收集我有興趣的概念放到「穩定幣」這個白板裡，但當我針對這些子議題、子領域整理出較完整的系統後，就可以一次把這些對應的卡片都搬到子白板裡，這時從 Map 連進「穩定幣」這個白板後，也可以直觀地看到各個跟穩定幣相關的子白板。

---

## 創造卡片的體驗提升

* v0.117.0 [Whiteboard: Drag blocks to create a card](https://heptaplatforms.notion.site/Whiteboard-Drag-blocks-to-create-a-card-503e7260570a4383930c731c171d296a) 

* v0.118.0 [Whiteboard: Drag blocks across cards](https://heptaplatforms.notion.site/Whiteboard-Drag-blocks-across-cards-c23f1015046a451591d3240ab949c381)

這兩次的更新讓「卡片」跟「白板」之間的互動以及「卡片」跟「卡片」之間的互動變得更輕易了。可以透過簡單的拖曳來搬移卡片內容，也可以單純拖到白板上來創造新的卡片。而後續還有一次版本更新是，將某段文字拖曳到白板上形成卡片後，該段文字的首行會直接形成一個超連結，就連到該張卡片上。

這樣直覺的互動方式也產生了一種潛在的 workflow 是，先大量輸入或貼上文字到某張卡片，再到對應的白板上面去拆解組織他們，拆解後又可以快速透過 drag and drop 的方式搬移組織卡片的內容。

同樣以前面的穩定幣為例，當我看到一篇較長的深度文章時，我可以先專注於剪貼 quotes 以及寫下我自己的想法到一張卡片上，待收錄完後，我可以迅速地把這張文章摘要卡片的內容用拖曳的方式分散開來，此時這張原始的文章卡片將會成為一張索引或目錄卡片，點擊上方的超連結就可以快速跳轉到對應的子項目卡片，這個過程很滑順直覺。

---

## 搜尋查找卡片的體驗提升

* v0.130.0 [Whiteboard: Full text search for cards](https://heptaplatforms.notion.site/Whiteboard-Full-text-search-for-cards-2b34d3fa252c405a94703af2f98fd009) 

* v0.131.0 [Command Palette: Global Full-text Search](https://heptaplatforms.notion.site/Command-Palette-Global-Full-text-Search-2ae2e70774644d47a25fc9c97c64dea7) 

* v0.144.0 [App: Universal Search](https://heptaplatforms.notion.site/App-Universal-Search-with-Cmd-O-d3fa729786f24dc9a2dcf024fdcc1302)

這三次更新讓「查找卡片」這件對於卡片筆記來說，非常自然、必要且頻繁發生的動作，變得更容易完成。尤其是 0.144.0 版本導入的 Command \+ O 查找方式，可以讓我快速跳轉到我想要的卡片或白板。這種查找效率的提高帶來幾個好處：

* 卡片更容易可以重複使用，避免產生多張內容類似的卡片。

* 當我更容易找到自己想找的卡片，自己的思緒就更不容易中斷，能很流暢地完成原本想進行的工作。

* 透過關鍵字查找，也有機會在查找的過程中發現自己沒預料到的、可能可以連結的卡片內容。

---

## 雙向連結的體驗提升

* v0.138.1 [Editor: Show link reference & whiteboard info on the bottom](https://heptaplatforms.notion.site/Editor-Link-reference-Info-1e47af55a8a140b199f6002a12474f4a)

這次的更新帶來我期待已久的 Link References 功能。在更新前， Hepta 的 Card Info 介面只看到的哪張卡片與這張卡片相連，但更新後，這個介面提供了更多資訊，這樣的資訊有助於在編輯卡片的當下，就觀察到更多「連結到這張卡片的卡片」，進而觸發更多聯想。對我來說這是讓 Hepta 在「雙鏈軟體」這個領域邁出重要一步的一次更新。 

* v0.151.0 [Editor: Mention menu preview and better \]\] behavior](https://heptaplatforms.notion.site/Editor-Mention-menu-preview-and-better-behavior-b8acbd2615004cb49a7de0909d3507b2) 

這次的更新讓透過兩個中括號 \[\[ 啟動雙向連結的預覽體驗更好，透過雙擊 \[\[ 來快速搜尋要連結的卡片時，更容易正確連結到心中想要連結的那張卡片。

* v0.158.0 [Editor: Show full linked reference](https://heptaplatforms.notion.site/Editor-Show-full-linked-reference-e48ec0927825488b866f59ef432bbc80) 

這次的更新可以視為 v0.138.1 的進一步強化，讓 Card Info 介面承載的資訊更多，若打開在側邊欄也會同步更新內容，目前看起來只差同步編輯以及交互 drag & drop 了。

---

## 其他的體驗提升

### 白板的整理與視覺體驗

* v0.103.0 [Whiteboard: Fit to content](https://heptaplatforms.notion.site/Whiteboard-Fit-to-content-98d65092ce0e46bdbfdf4437c14bf64e) 
  * 可以一次圈選多張卡片並根據內容量調整卡片大小。
* v0.112.0 [Whiteboard: Auto-content fit](https://heptaplatforms.notion.site/Whiteboard-Auto-content-fit-76bd1ebc494948d18240ad5e4a27f503) 
  * 可以自動調整卡片大小
* v0.116.0 [Whiteboard: Tidy up](https://heptaplatforms.notion.site/Whiteboard-Tidy-up-72a5ccfd78d3419f84862aa03d7ec102) 
  * 拿來整理雜亂卡片超好用。
* v0.119.0 [Whiteboard: Bulk fold cards](https://heptaplatforms.notion.site/Whiteboard-Bulk-fold-cards-d619b0912b5e4d9e8b7c045bcfc11e8f) 
  * 可以快速 fold 跟 expand 卡片，可以有效的利用空間，或者把一些較次要的資訊快速隱藏起來，有需要再打開來看。
* v0.140.0 [Map: Change Whiteboard Color](https://heptaplatforms.notion.site/Map-Change-Whiteboard-Color-d2c54762544a4deb9692473cc9e89081) 
  * 可以在 Map 上面更改白板的顏色，讓同類型的白板更容易識別。

### 編輯器的處理體驗

* v0.131.0 [Editor: List usability improvemen](https://heptaplatforms.notion.site/Editor-List-usability-improvement-62e3f40f90194ed49d172c38ebd2a328) 

  * 這次改版提升了許多編輯器的細節，讓很多體驗都更「合理」

* v0.136.0 [Editor: Update card link with card’s title (like Notion, Roam, etc)](https://heptaplatforms.notion.site/Editor-Update-card-link-with-card-s-title-like-Notion-Roam-etc-e486ae20142742c18d55fa6110ee2a1d) 

  * 自動更新連結卡片的標題可以讓之後查找時不會找不到東西，不過我覺得這有點仰賴命名的能力。

* v0.156.0 Open the slash menu between texts 

  * 可以在打字的過程中展開 slash menu 。

從上述整理可以大致發現， Heptabase 團隊蠻習慣在一段時間內專注更新某個領域的體驗，並且大概每 7-10 個版本就上線一個重要的功能，這速度真的是很驚人，作為一個使用者與愛好者，也很開心看到產品成長地這麼迅速。

---

## 我目前怎麼使用 Heptabase ？

在經過上述幾個月的版本迭代與功能更新後， Heptabase 已經基本滿足，甚至超越我對於知識管理工具的期待：

* 可以依照日期建立卡片，進行快速無壓的每日紀錄

* 比照大多數雙鏈筆記軟體，可以快速準確地透過 @ 以及 \[\[ 來建立新卡片或連結既有的卡片。

* 有快速精準的全局搜尋功能，能夠透過關鍵字找到我想去的白板或卡片

* 有層級化的管理方式，讓我可以妥善地分類與管理卡片

* 良好支持注音輸入法與中文搜尋 （這真的很重要啊！）

* 有堪稱優秀的編輯器體驗（很多細節寫長文會更有感，例如我先點列好多內容組織架構後，在編輯拆解點列架構時，子項目們會一起往前退一格。）

* 具有把許多內容一次展開來檢視的能力，這種視覺化的體驗能夠更好地建立不同內容之間的關係

因此，基於上述的功能，我現在主要會透過 Heptabase 來進行下列活動：

* 每日紀錄與連結我的各種想法，再將它們放到 [Pin 起來的筆記與想法快照](https://notes.pinchlime.com/)

* 在閱讀文章和書籍後製作閱讀筆記卡片，並直接在卡片上面透過將文字加粗、 highlight 以及寫筆記來進行「漸進式總結」。

* 專門用一個白板來收集部落格與[電子報](https://pinchlime.substack.com/)的主題靈感，也用一個白板來擔任我的「工作台」，放置那些待處理、待加工的草稿卡片，並且直接在 Heptabase 裡面撰寫長文，撰寫的過程會將需要參考的卡片放到側邊欄對照。

從上述三項可以看出，目前我的用法比較偏向拿來捕捉與整理自己的靈感、想法和觀點，再進而組織整理與輸出，所以我比較常用到的是卡片以及編輯器的功能，白板對我來說則相對少用一些。但我的待辦清單裡面已經有好多項想用 Heptabase 學習的複雜知識，屆時若對白板的用法有更多感想，再來分享！

---

## Heptabase 怎樣還可以更好？

雖然已經非常滿意了，這邊還是想來許願一下，未來希望 Heptabase 可以有的功能：

**更快速輸入內容的方式**

可能是類似 Drafts 或 The Archive 那種，按個快捷鍵就可以叫出來釘在桌面上的獨立紀錄視窗，上面可能只需要一個輸入框、可以快速上一些標籤資訊、或者可以選擇加到某個白板，就好。這樣我可以在不打開 Hepta 主程式的情況下，就很輕易地收錄想法或摘錄內容，等到有完整的時間時，再來一次整理這些快速收錄的內容。

**更好地產出長文的方式**

姑且稱這個需求叫做「Output App」，這是最近開始用 Heptabase 寫長文時感覺到需要的功能，簡單描述一下，他會跟 Tags, Timeline, Card Library 這類「 Meta-app 」一樣，都是「某種特定應用卡片的方式」。這個 Output App 最主要的目的就是更好地將卡片們編輯與整理成一篇一篇的長文。

比方說，我可以在側邊欄展開原先累積的許多原子卡片，並將想要放到長文章的段落拖曳到 Output App 裡面的某篇 Output draft，拖曳後，系統會自動在這些原子卡片與這篇 Output draft 之間建立連結，這樣做的好處是雙向的。

* 當我未來看這篇完稿的 Output 時，我會知道他是基於哪些原子卡片而生的

* 當我在白板或其他地方查看原子卡片時，我可以清楚知道我以這些原子卡片為基礎產生了哪些完整的長文 Output。

而這個 Output App 也可以串接各種輸出的平台或方式，例如 Twitter, Medium, Wordpress, 或其他更多可能性，在輸出的同時也可以為這篇 Output 標註必要的 metadata ，讓自己也更容易回顧哪些內容曾經在哪個地方輸出。

**更好的連結體驗**

* 提供每張卡片（或白板）的專屬 URI 連結，這讓我更容易透過 Keyboard Maestro 之類的軟體來快速跳轉到想要的卡片上面。

* 讓卡片也可以連結到白板。因為白板常常是作為某種「中規模的概念」來使用的，本質上他也可以理解為「一張裡面放著許多卡片的大卡片」，所以這樣的「大卡片」也應該要可以被其他的小卡片們連結。比方說當我在整理「支付工具的監管方式」時，我就可以很快速地連結到「穩定幣的監管」這個白板。

**更好的搜尋體驗**

* 搜尋時能顯示「關聯度」，這點是我最佩服也最喜歡 DEVONthink 的地方之一，他會根據字詞的權重來給予搜尋關聯度的排序，這樣更容易找到我當下想找的卡片。

* 可以進行模糊搜尋，或進階搜尋。

總結來說，這些需求主要想達到的，都是讓「輸入」資訊到卡片更容易，讓「查找與處理」卡片更容易，並且讓那些重要的卡片更容易被重複利用，最終還能清楚看到這些重複利用的軌跡或被利用的頻繁程度。

如果這些需求都能做到，那整個「輸入 → 處理 → 輸出」的流程將會更加順暢。但在這些願望實現之前，目前的 Heptabase 已經非常棒了，而且我總覺得我連一半的潛能都還沒激發出來，希望接下來更密集使用後能分享更多的使用案例給大家！