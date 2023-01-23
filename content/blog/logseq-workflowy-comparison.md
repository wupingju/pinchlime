---
title: 嘗試把 Logseq 當成 Workflowy 使用的心得
date: 2022-02-01
path: 2022/02/01/logseq-workflowy-comparison/
description: Workflowy是隊伍中的明星球員，而Logseq 則是令人期待的潛力新秀。許多 Logseq 的「缺點」似乎都只是暫時的，甚至不算是什麼明顯的缺點，而 Logseq 的一些優點則是非常吸引人認真投入與累積筆記。
taxonomies:
    categories: 
    - Tools
    tags: 
    - Logseq
    - Workflowy
    - Outliner
---

今天想來分享一下最近把 Logseq 當成 Workflowy 用的心得

![](https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/workflowy-logseq_E1hVKi.webp)

<!-- more -->

## 前情提要

大概去年 11 月底開始使用 Logseq ，一用就覺得[一見鐘情](@/blog/first-impression-of-logseq.md)，漸漸地不再用[原本也很喜歡的Obsidian](@/blog/my-favorite-obsidian.md)。不過因為有在兩台電腦上同步使用的需求，但 [Logseq 透過 iCloud Drive 同步會有掉檔案的問題](@/blog/logseq-icloud-drive-sync-data-loss.md)，所以在12月決定先不在工作上使用，只在 iMac 上單機使用。

為了替代 Logseq ，我 12 月到 1 月之間都透過 [Craft](https://craft.do) 來記錄工作上的會議紀錄和專案資訊，但卻逐漸發現一些問題，最後還是決定回到 [Workflowy](http://workflowy.com/) 這個已經用了好幾年的最愛軟體之一。用了以後發現非常順手（可參考拙作：[Workflowy 的雙向連結、鏡像以及看板功能](@/blog/workflowy-backlinks-mirror-board.md)），幾乎可以解決我90%的工作記錄及追蹤需求（不包含任務＆專案管理）。而在過年前忙於工作，稀少的空閒時間大多都花在新玩具 [Heptabase](https://heptabase.com) 上面，Logseq 一度疏於整理。

但趁著今年過年相對比較有空的假期，好好地思考了 Logseq 目前在我工作流中的定位，也整理了一下在 Logseq 上面累積了兩個多月的筆記，好像有一些階段性的心得可以分享一下。

先講結論：**目前 Workflowy 對我來說是隊伍中的明星球員，而Logseq 則是充滿潛力令人期待的新秀。**

---

## Logseq 用起來有哪些不順手的地方？

除了前面講的同步問題外，最近時常會在使用 Logseq 發現一個令我中斷心流的狀況是：我常常為了想要補充某段幾天前記下的想法，而必須大費周章去尋找它。

這是因為，我之前的做法都是直接在 Logseq 的 Journals 頁面記下當天的各種零碎雜感，但 Logseq 的 UI 可能是為了讓使用者專注於今日，必須要往下點開，才能回到今天以前的日子。這就讓體驗有所中斷。相較之下，Workflowy 的結構固定，因為它是一個無限階層的大綱架構，只要對自己的筆記稍微熟悉，很快就能根據位置找到那些還不成熟的想法進行補充。

這時我冒出來的想法是：好像可以試試看，**把 Logseq 當成 Workflowy 用。**

---

## 只需要兩個入口就好

在 Workflowy 上，我主要透過兩個節點來管理所有工作上的事情，分別是 **Daily Notes & Things**，主要的架構大概是這樣的：

- Workflowy Home
    - Daily Notes
        - 今天
            - 專案事務
                - 專案A
                - 專案B
            - 非專案事務
                - 會議A
                - 會議B
        - 昨天
            - 以此類推
        - 前天
    - Things
        - 會議入口
            - 定期會議
            - 其他會議
        - 專案入口
            - 專案 - 準備中
            - 專案 - 執行中
                - 專案 A
                - 專案 B
            - 專案 - 已完成
                - 專案C
        - 基於職責或任務的事務
            - 職責A
            - 任務A

從這個架構圖可以看到，所有東西都會被放在 **Daily Notes & Things** 底下，再分門別類，互相引用。通常是 Daily Notes 會引用到專案和會議的內容，再透過該內容的反向連結得到一覽的效果。

但在 Logseq 上面，原先的架構是每一天都是一個最高層級的 markdown 檔案，彼此之間沒有從屬性，所以我打算試試看用 Workflowy 的方法來運作 Logseq 一陣子。而在真的這麼做之前，也稍微思考了一下 Logseq 跟 Workflowy 彼此擅長跟不擅長的地方。

---

## Logseq 和 Workflowy 一樣好的地方

- 兩者都可說是無限層級的大綱軟體，有助於快速進行階層化、具有邏輯性的思考。
- 鍵盤操作都相當順暢，體驗很好。（像是游標即使在句子中間任何一點，按 Tab 都可以整段直接縮排。）
- 反向連結的顯示都很完整，這點的意思是，從任何一個連結點進去後，視窗下方的反向連結區域可以顯示完整的內文，而不僅僅是「哪個文件連到這個文件」而已。這在思考和編輯上的優點非常多，可以方便引用、甚至直接搬移內容。如下圖，左邊是 Logseq 官網的 FAQ 內容，反向連結的內容就在下方的 "Linked References" 處，可以直接閱覽及編輯，而右邊是我之前製作的 [Workflowy Demo](@/blog/workflowy-backlinks-mirror-board.md)，反向連結的內容會顯示在下方的 "Backlinks"處，也是可以直接閱覽跟編輯。

![](https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/workflowy-logseq-backlinks_pdScRU.webp)

---

## Logseq 不如 Workflowy 的地方

- Workflowy 可以把任何一個節點放到左欄的最愛，Logseq 只能以 .md 文件為主，不能細到把任何一個 node pin起來。
- Workflowy 有基本的 URL scheme，可以直接透過固定的連結（再製成快捷鍵）連到固定的節點，Logseq 目前還不行。
- Workflowy 每一行下面可以有一個單獨的 notes 欄位，是非常棒的一件事，拿來放tags、拿來放連結、放註解，都很剛好。這點 Logseq 就輸了。  
    如下圖，Logseq 的 shift + enter 只是軟換行，層級上跟本文是同一級的，引用時會被視為本文，全部內容都看得到。 Workflowy 的 notes 是另外一種屬性，顏色是不同的灰色，可以跟本文的黑色區別，且太長會略縮，在引用介面也不會顯示出來。 我覺得Workflowy的設計比較乾淨！  
    
![](https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/workflowy-logseq-notes_RLE6d4.webp)

- Workflowy 的同步非常順暢穩定，有陣子我直接拿它來當 MacOS 跟 iOS 之間的剪貼板，基本上隨時打開都會是一樣的東西，要多裝置同步編輯也幾乎沒問題。

---

## Logseq 比 Workflowy 好的地方

- Logseq 的核心是一個一個獨立的 markdown 文件，不僅方便攜帶，也有一堆軟體可以支援，加上檔案都存在自己的裝置上，幾乎不用擔心不見或者是隱私的問題。
- 雙向連結時的偵測對中文更友善，有許多國外開發的軟體沒有考量到「選字」這件事必須要多按一次 enter，所以常常在選字時就會自動觸發下一步動作。例如 Workflowy 在選雙向連結的標的時常常都會出錯。但在 Logseq 上面，即使用注音輸入法時按下選字的 enter 也不會強制斷行。
- 在 Logseq 裡面若更新一份文件的標題，有引用到該文件的所有文件都會自動更新，這樣就降低很多命名上的不確定性。
- Logseq 還有非常優秀的 PDF 註記及引用功能，這點 Workflowy 完全比不上。

---

## 小結：Workflowy是隊伍中的明星球員，而Logseq 則是令人期待的潛力新秀。

兩者相較起來，如果單純以我的需求來說，目前 Workflowy 在使用體驗上更滑順流暢及穩定，該有的功能都有，只要輸入法稍微習慣，就沒有太大的問題。（若自己紀錄的是機敏的資訊則要多考慮）

如果兩者只能選一個來用，我可能會選 Workflowy。雖然這樣比較不太公平，畢竟 Workflowy 已經問世很久，整個系統相對成熟許多。但因為我自己一直不想把工作上的內容與個人知識庫的內容混在一起，而 Workflowy 也不能開第二個工作區，所以目前還免費的 Logseq 就成為了當下最佳的替代方案。

但在進行這些功能比較時，卻也發現許多 Logseq 的「缺點」似乎都只是暫時的，甚至不算是什麼明顯的缺點。而且開放的架構也有許多 plugins 可以補足功能上的需求（例如 看板模式、任務管理還有其他更多服務的串接），而 Logseq 的一些優點則是非常吸引人認真投入與累積筆記。

所以以我目前單純想存放「零散想法與個人專案」相關資訊的需求來說， Logseq 應該是相當夠用的！至於把 Logseq 依照 Workflowy 的用法分成兩大入口來用的作法到底好不好？是否是多此一舉？就運作一陣子再來分享了！
