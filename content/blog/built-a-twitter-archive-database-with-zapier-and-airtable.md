---
title: 透過 Zapier 與 Airtable 建立自己的 Twitter 備份資料庫
date: 2022-12-28
path: blog/built-a-twitter-archive-database-with-zapier-and-airtable
description: 未來我不僅能夠同步紀錄 Twitter 備份，也可以依照規則，自動推送我想要的資料給我。
taxonomies:
  categories: 
    - Tools
  tags: 
    - Twitter
    - Zapier
    - Airtable
---

<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/zapier-airtable-1_Vg8dJX.webp" loading="lazy" alt="zapier-airtable-1" align=center />

隨著使用 Twitter 的頻率越來越高，有時會想要找過去推過的文然後繼續補充，有時只是好奇想看一下自己以前推了什麼文，雖然 Twitter 內建的進階搜尋就可以找到，但一直以來都想要有一個自己掌握的資料庫，裡面放自己所有的 tweets 備份。

這兩天心血來潮想試試看自動化的串接方式，就想到了之前聽過，但一直沒用過的 [Zapier](https://zapier.com) 。我對 Zapier 的最粗淺認識與理解是，他是一個與 IFTTT 很像的工具，但好像更強大一些。


<!-- more -->
---

而我想透過 Zapier 完成的，是未來我每次在 Twitter 發推時，Zapier 會直接幫我把這則推的一些基本資訊存在 Airtable 的資料庫（表格）裡面。而我未來可能可以再透過 Airtable 去應用這些資料。

## 步驟

嘗試的結果非常順利，Airtable 跟 Zapier 都非常直覺好用，簡單來說步驟如下：

1. [註冊 Zapier 帳號](https://zapier.com/sign-up)

2. [註冊 Airtable 帳號](https://airtable.com/signup)（我原本就有了）

3. 在 Zapier 裡面選擇 Create Zap

4. 第一步驟「Trigger」選擇 Twitter
<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/zapier-airtable-2_POoGIL.webp" loading="lazy" alt="zapier-airtable-2" align=center />


5. Event 選擇 My Tweet （還有其他的 triggers ，之後再玩玩）

6. 並且登入 Twitter 授權給 Zapier，此時他會測試你的 Trigger ，抓一篇近期的推文，如附圖，剛好抓到我測試完 Zapier 的推文。
<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/zapier-airtable-3_Gi8BIF.webp" loading="lazy" alt="zapier-airtable-3" align=center />



7. 測試完畢後就可以設定第二步驟的「Action」，選擇 Airtable （應該也可以用 Google Sheets 或別的）
<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/zapier-airtable-4_PBAqRS.webp" loading="lazy" alt="zapier-airtable-4" align=center />

8. Event 選擇 Create Record

9. 登入 Airtable 帳號，選定要串接紀錄的 Base（大表）跟 Table（分頁）

10. 選定後，會顯示該 Table 的欄位，也可以設定想要對應的 Twitter 資料，邊對應邊設定，以我來說，我就在 Airtable 裡面設定了 Text、URL、User name、Date 這些欄位，並且選取對應的 Twitter 資料。（設定的當下可以同步更改 Airtable 後按 Refresh Fields 就會重新整理）
<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/zapier-airtable-5_ZWnN64.webp" loading="lazy" alt="zapier-airtable-5" align=center />


11. 全部設定好後可以測試整個流程，若都順利，就會在 Airtable 看到這筆記錄了，沒問題後就按下 Publish ，之後就可以自動享受 Zapier 為你服務了。


以上看起來步驟有點多，但一點也不困難，Zappier 的 UI 介面非常直覺好操作，可能需要注意的是 Airtable 這邊的欄位要設定成可以對應 Twitter 資料的格式，例如日期這邊好像就串不太起來，因此我在 Airtable 是先以純文字的方式儲存日期的資訊。


## 後記

就在打這篇的過程中，我開始思考該拿這些資料做什麼，結果發現 Airtable 裡面也有類似的「Automations」功能，而且也非常容易設定，結果我就順利做出了：

「**寄信給我提醒我一年前 PO 過的推文**」這個後續操作。

具體來說步驟如下：
1. 在 Airtable 裡新增一欄是「Created」，他會自動抓到這串紀錄的創造時間。（因為我不太清楚如何把 Twitter 給的日期字串轉換成 Airtable 可讀取的資料，所以必須用這種比較笨一點的方法）。
2. 到 Airtable 的 Automations 設定條件，「When record matches conditions」，然後條件設定為「365 天前 created」。
3. 設定 Action 是寄送 email 給自己，並且在預設的模板裡面加入推文文字、時間、連結等資訊。

等於說，未來我不僅能夠同步紀錄 Twitter 備份，也可以依照規則，自動推送我想要的資料給我。

有興趣的人可以嘗試看看 Zapier，免費版本每個月有 100 次任務的額度，例如執行一次推文備份就是 1 次，我感覺我應該蠻夠用的，如果不夠用可能也可以設定一下進階的規則，或者付費。