---
title: 如何透過 Logseq publish 在 Netlify 上建立個人 wiki？
date: 2022-05-21
updated: 2022-05-21
path: blog/publish-logseq-personal-wiki-on-netlify
description: 本文介紹如何將自己的 Logseq graph 透過內建的 publish / export 功能，直接發布到網站上，藉此建立一個「個人 Wiki」頁面，或者也可以稱它為 Digital Garden。
taxonomies:
  categories: 
    - Tools
  tags: 
    - Logseq
    - Netlify
    - Github
    - Personal Wiki
---

今天想來分享一下，如何將自己的 Logseq graph 透過內建的 publish / export 功能，直接發布到網站上，藉此建立一個「個人 Wiki」頁面，或者也可以稱它為 Digital Garden。

如果一切順利，完成品就會是一個類似這樣的東西： 

[https://logseq.pinchlime.com](https://logseq.pinchlime.com) 

點開來以後會很像自己 Logseq graph 的樣子，可以有超連結、可以建立頁面、可以設定雙向連結，也可以看到 graph view 。

<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/logseq-publish-demo_li7WwB.webp" width = "768" height = "382" alt="logseq-publish-demo" align=center />

這個頁面是 4 月底到 5 月初我自己的小小嘗試，透過這個嘗試我發現建立「個人 Wiki」有非常多優點，但 Logseq 還有一些不足的地方，因此後來我又找到了 [Dendron](https://www.dendron.so/) 這個工具來建立我自己的個人 wiki ，目前放在 [Pin 起來的 Wiki](https://wiki.pinchlime.com/)。

但 Dendron 更小眾一些，使用起來門檻也比 Logseq 高一些，如果你對 Logseq 有興趣，或者本來就已經是 Logseq 的使用者，也對建立一個個人 wiki 頁面有興趣的話，相信這篇簡單的教學應該還是可以提供一些幫助！

<!-- more -->
---

## 概念簡述

因為後面比較多是步驟的整理，這邊還是試圖描述一下整件事情在做什麼。大致上可以拆解成這些項目：

- 透過 Logseq 內建 Export graph 功能將 local 的 graph 內容輸出成靜態網頁
- 將輸出的內容放到 Github 的 repository 裡面
- 透過 Netlify 自動偵測 Github repository 的變動，藉此達成自動部署

這三件事情裡面，每一件都有自訂的空間。比方說第一步可以決定要 publish 哪些頁面。第二步可以決定要放在哪個 Github ，還是 Gitlab 或 Bitbucket 等不同的平台。第三步則是可以決定要部署在 Netlify 或者是 Github pages 或 Vercel 等平台。個別平台的作法可能會不太一樣，因為我的部落格是放在 Netlify 上面，所以就以 Netlify 為主來介紹了！

另外也提前說明一下，整個過程都不需要輸入任何指令，無論是 Github 或是 Netlify 都有好懂易用的介面，所以即使像我一樣的程式外行都可以順利完成！

---

## 預先準備

如果你已經很熟悉 Github 或者是 Vercel 與 Netlify 等平台，那應該很容易就可以搞定整件事，所以這邊先假設讀者跟一兩個月前的我一樣，是還沒有相關帳號或經驗的人。

所以為了要完成這整件事，除了 Logseq 之外，還需要預先準備：

- Github 帳號 ，沒有的話就去申請一個吧！ [https://github.com/](https://github.com/)
- Netlify 帳號，沒有的話就去申請一個吧！ [https://www.netlify.com/](https://www.netlify.com/) 當時我是直接透過 Github 帳號申請登入，所以可以先完成上一步驟再來註冊 Netlify。
- 下載並安裝 [Github Desktop](https://desktop.github.com/) 應用程式，然後綁定自己的 Github 帳號。

---

## 第一階段：設定好自己的 Logseq

### 步驟一：設定 Logseq 的輸出資料夾

先在自己的電腦上，建立或把一個資料夾當成 Logseq 的「輸出資料夾」，這跟 Logseq graph 本身存放的資料夾不一定要一樣（我放在完全不同地方），可以把它理解成為，每次你打算把資料公佈到網路上，你就必須先放在一個本機的資料夾，這個資料夾裡面的 Logseq 輸出資料，就是你想要放在網路上的所有內容。

比方說，他可能命名為 "logseq-pub" ，然後放在 documents/Github 裡面，路徑可能就是 documents/Github/logseq-pub 。

### 步驟二：設定要公開發布的範圍

若是打算整個 Logseq graph 都公開：
- 那就在 Logseq 裡面選擇 Settings -> Editor -> 點選 "All pages public when publishing"

若是一個 graph 裡面，只有部分頁面想公開：
- 那就不要勾選 Settings -> Editor 裡面的 All pages public when publishing
- 而是將想要公開的頁面，點選右上角選單的 Make it public for publishing ，或者是在頁面的最上方第一列，輸入 public:: true 。
- 不想公開的頁面，則在頁面最上方第一列，輸入 public:: false 。
- 這樣在輸出 graph 時，就不會輸出那些填入 false 的頁面了。

### 步驟三：將頁面公開輸出

在 Logseq 的任意頁面，點選右上角的選單，選到最下方的 "Export graph" ，再點選 "Export public pages"，並選擇路徑在步驟一設定的那個資料夾（logseq-pub），就可以把整個 graph 輸出成可以發布到網路上的完整檔案了。

假設你在前一個步驟選定全部公開，那這時輸出的就會是整個 graph ，反之就是只有你設定的那些頁面。
第一階段完成後，你會有一個 Logseq 的輸出資料夾，裡面已經有你成功輸出的內容，接下來要做的就是把它們放到網路上。

---

## 第二階段：將 Logseq 的輸出資料夾設定為 Github 的 repository 

### 步驟一：創建新的 repository

透過 Github Desktop 選擇「Create a New Repository」，幫它取個名字，並且在 "Local Path 這邊，選擇剛剛設定的 logseq-pub 資料夾。

<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/github-create-a-new-repository_33JKGw.webp" width = "768" height = "881" alt="github-create-a-new-repository" align=center />


### 步驟二：Publish repository

選好之後按下 Create Repository 就好，接著在 Github Desktop 的右方可以看到「Publish repository」的按鈕，按下去就好。按下去以後，預設會把這個 repository 設定為「Private」，意思就是別人看不到你的資料，一開始建議可以先打勾。

<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/publish-repository_pgzwk6.webp" width = "768" height = "423" alt="publish-repository" align=center />

此時你再登入自己的 Github 帳號，就會看到 "Repositories" 的地方，出現這個 "Logseq-Pub" 了。

---

## 第三階段：將 Github repository 與 Netlify 綁定

### 步驟一：Add new site

登入自己的 Netlify 帳號後，點選上方選單的 "Sites" ，然後點選 "Add new site" ，此時可以選擇 "Import an existing project" （備註：在這邊如果要選 Deploy manually 也完全可行，等於你就每次手動把你從 Logseq 輸出的整包內容直接放上去就好，這樣做的話可以不用設定 Github ，也不用綁定 Github。）

### 步驟二：Import an existing project

點下 Import 頁面後，會看到一個選單，在這邊因為我是選用 Github ，所以就選擇連結 Github ，點下去以後會有一些認證授權的步驟，全部完成後，在「Pick a repository from GitHub」這邊，選擇你在上個階段設定好的 repository （logseq-pub)。

### 步驟三：Deploy！

成功讀到後，接下來的頁面什麼都可以不用選，直接按下「Deploy Site」就好！

---

## 大功告成

如果一切進行順利，按下 Deploy 後，過一兩分鐘， Netlify 上面就會出現綠色的 "Published" 字樣，代表已經順利發布完成。此時選擇 "Preview" 就可以看到網站上線的樣子了。

但如果想要有非亂碼的網域，或者是要設定自己的網域，則需要再到 Netlify 上面的 domain management 設定。這只要照著官方說明一步一步做，就可以完成了。

整個流程若是完全沒做過的人，或許要花 30 分鐘到一小時可以順利完成，但只要完成一次，接下來每次要更新時幾乎就是「10秒內」可以完成的事。

之後每次更新只要：
- 輸出 Logseq graph 到同一個資料夾。
- 在 Github desktop 點選 commit to master/main ，再選 publish

就可以在 Netlify 看到它自動幫你把內容放上去，非常自動簡單。而且重點是，不管是 Logseq, Github, Netlify ，都可以免費使用。

---

## 後記：建立一個公開的個人 wiki 的好處

自從開始嘗試經營這個公開的個人 wiki 後，一個多月來我幾乎天天都會抽空更新內容到站上。

這個習慣讓我有更多動力去吸收更多知識，也讓「分享」這件事更降低阻力，因為不特別把連結放到社群上的話，其實沒人知道你「分享、更新」了什麼。但是這些內容「會放在網路上公開」的這個事實，也會促使自己稍微用心組織一下內容以及文字。

對我來說這是一個很剛好的平衡，所以推薦有興趣的人也可以試試看！

下兩篇文章就來寫：
- 如何透過 Dendron 及 Netlify 建立個人 wiki 
以及
- 為什麼我選擇用 Dendron 而不是 Logseq 建立個人 wiki。
