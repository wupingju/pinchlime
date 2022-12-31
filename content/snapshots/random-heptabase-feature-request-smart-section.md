---
title: 我想要的 Heptabase 功能 - Smart Section
date: 2022-12-30
updated: 2022-12-30
description: 我想透過 section 來實現的原因是，它是一個視覺上聚焦的方式，著重呈現卡片之間的群組關係，但它不會重複影響卡片庫或白板的內容。
path: snapshots/random/heptabase-feature-request-smart-section
taxonomies:
  kinds: 
    - Random Thoughts
  tags: 
    - Heptabase
---

昨晚想到這個需求，今天早上在 Heptabase 的 discord 裡面提出，期待之後有機會實現，也在這邊記錄下來。



以下是原文：

想要一個功能，我先以 smart section 命名跟想像

在白板中可以選擇加入一個 smart section，加入時可以自訂這個 section 的篩選條件，例如某個日期到某個日期、帶有某個tag、卡片中有某個字串等等。

設定後，這個 section 會帶著符合條件的卡片，直接出現在當前白板上，這個 section 會隨著符合條件的卡片變動而即時更新內容（例如多加入一張符合 tag 的卡片在其他地方時，這個 section 也會自動擴張。

而這個 smart section 由於篩選條件固定，因此不能隨意把卡片加入或移出，除非調整篩選條件。

但在介面裡可以編輯個別卡片的內容，也可以透過拖曳的功能直接把想要的卡片拉出 section 到目前的白板裡。

這個功能的特性是，可以快速篩選並呈現某個群組的卡片，但他不會是一次性把卡片加入白板，而著重的是持續性的監測、或者是快速的加入參照。

我有想到的使用情境，例如想寫 weekly 或 monthly reviews 時，就可以快速把過去某段時間的 journal 卡片抓出來一起參考對照，或者可以設定成「未來七天」的持續呈現，這樣可以聚焦在短期內應該做的事情，有點像是 smart views 的感覺，當然也可以是把特定的 tags 都聚集在一起展開研究。

我想透過 section 來實現的原因是，它是一個視覺上聚焦的方式，著重呈現卡片之間的群組關係，但它不會重複影響卡片庫或白板的內容。