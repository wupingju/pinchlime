---
title: 為何我不想再用 Substack 寄送電子報？
date: 2023-02-05
updated: 2023-02-05
description:  Substack 的問題在於它讓寫作者無法選擇「不追蹤讀者」；另一方面，它也讓讀者無法選擇「不被追蹤」，假設有任一方可以行使積極同意權，我覺得對我來說都很好，但 Substack 沒給大家這樣的選擇機會。
path: newsletters/why-i-dont-want-to-use-substack-anymore
extra:
  issues: 18
---

在幾天前[發現 Buttondown 這個電子報服務](@/blog/first-impression-of-buttondown.md)後，我就決定要搬離 Substack ，不再使用 Substack 寄我的電子報。

核心的原因除了 Buttondown 有一些非常切合我需求的功能之外，最重要的「推力」，還是 Substack 自身的問題。

簡單來說，因為 Substack 追蹤了不少讀者的開信與讀信數據，我覺得這裡面有一大部分是屬於讀者的隱私，但 Substack 沒有辦法讓寫作者選擇「不追蹤」，因此我思考一陣子後，決定不再使用 Substack 。


<!-- more -->
---

## Substack 追蹤了什麼？

打開 Substack 後台，每一封電子報都可以看到一些基本的統計數據，例如觀看次數、開信率、以及連結的點擊次數等等，也可以看到流量的來源佔比，如下圖：

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/substack-stats-1_pxMPci.webp" data-fancybox data-caption="substack-stats-1">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/substack-stats-1_pxMPci.webp" loading="lazy" alt="substack-stats-1" align="center" />
</a>

接著，若點進每一篇的數據頁面，可以看到不同訂閱者的瀏覽資訊，例如該篇電子報，不同訂閱者個別點開了幾次、點擊了幾個連結等等，如下圖：

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/substack-stats-2_Xx0Tvg.webp" data-fancybox data-caption="substack-stats-2">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/substack-stats-2_Xx0Tvg.webp" loading="lazy" alt="substack-stats-2" align="center" />
</a>

還沒完，假設我點到個別訂閱者，還可以看到他過往所有的瀏覽與點擊紀錄：

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/substack-stats-3_fhvnsh.webp" data-fancybox data-caption="substack-stats-3">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/substack-stats-3_fhvnsh.webp" loading="lazy" alt="substack-stats-3" align="center" />
</a>

等於說，我可以從 Substack 的後台，知道不同訂閱者對我的哪封信特別有感、看很多次、比較喜歡點擊哪個連結等等。



---

## Substack 是怎麼辦到的？

以我的理解，這是透過一個 1x1 的 “pixel image” ，就是在電子報中放入一個人眼看不到的一像素圖片連結，每當使用者點開信件，就會向 Substack 的伺服器請求下載該圖片，因此 Substack 就可以知道使用者的點擊與瀏覽資訊。

而在連結方面，每一個信內的連結都會被植入特定的追蹤碼，因此 Substack 可以識別哪個連結有被點擊、甚至可以識別「是誰」點擊了連結。

而不只是 Substack 而已，我理解絕大多數的電子報服務都會這樣做，我不確定不同電子報服務的後台看到的資訊有哪些，但通常來說都可以追蹤到：

* 你是否有打開信件

* 你在何時打開信件（每次都可以單獨紀錄）

而有的還可以追蹤到：

* 你打開信件時的 IP 

* 你在什麼裝置、作業系統打開

---

## Substack 這樣做有什麼問題嗎？

這個問題我自己也思考蠻久，我很早很早，一開始使用 Substack 時，就知道這件事，我也知道絕大多數的電子報服務都是這樣做。但我感覺真正知道「自己會被這樣全方位追蹤」的人，可能不是特別多。

所以每次我點開電子報的後台，我都會有一番小小的掙扎。

站在寫作者的角度，當我看到某些人在單一信件重複查閱，我會感到很開心、滿足，甚至我可以認出某些訂閱者的信箱，因此我雖然平常沒有在社群上跟這些人特別互動，但知道他們都有持續在看我電子報的感覺也很好。

但站在一個讀者的角度，當我想到我訂閱的電子報作者，有可能知道我在何時打開他的信、甚至是打開幾次，就會讓我感覺有一點點不自在。雖然我會訂閱的人大多已經是我信任或有好感的人，但如果可以，我還是希望能夠保有一點隱私。

這兩個心態在我心中互相較量的結果是，讀者角度贏了！

但，即使我已經知道我更傾向讀者的隱私，每次發送信件後，我仍是會忍不住點開後台，看個數據。所以我知道，對我來說最好的做法，就是只追蹤必要的數據，或者是完全不追蹤。

站在我自己作為讀者的角度，我可以接受的是「去識別化」的追蹤，意思是例如上面的第一張圖那樣，作者只會知道每封信的「加總」數據，但不知道個別使用者的狀況。

但無論是去識別化的追蹤、或者是「完全不追蹤」，在 Substack 裡面都行不通。

---

## Substack 不讓你選擇「說不」

在 Substack 的後台裡，作者沒辦法「關閉」追蹤的功能，只能夠選擇要追加更多的追蹤選項，例如你可以加入 GTM 、 GA 、 Facebook Pixel 等等不同追蹤工具的 ID 。

而我有稍微搜尋過「如何在 Substack 關閉追蹤」這個議題，找到一篇很好的文章：[Substack spies - by Saar Drimer - Assortment](https://saar.substack.com/p/substack-spies) 。在裡面作者有嘗試直接聯絡 Substack ，詢問：

> \* Will you commit to reduce the amount of tracking?\
> \* Will you provide a way for me to reduce the amount of tracking in my\
> newsletters?
>
> I feel that if that you won't I will look for another way to publish.

結果 Substack 的回答是

> We can't commit to changing our stats, nor can we provide a way to reduce the stats on the dashboard of your own publication. 
>
> If that's not for you, and you decide to publish elsewhere, I understand!

簡單來說， Substack 的立場是，「我們不會減少對使用者的追蹤，如果你打算離開，我們可以理解。」

在大約幾個禮拜前看到這篇文章後，我感覺到我終究要找個別的地方來發送我的電子信。

而在本週，我發現了 Buttondown 這個服務，它「也有」追蹤的功能，但是它可以讓我選擇「不開啟追蹤」，如下圖。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/buttondown-tracking_79EmE6.webp" data-fancybox data-caption="buttondown-tracking">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/buttondown-tracking_79EmE6.webp" loading="lazy" alt="buttondown-tracking" align="center" />
</a>

我目前暫時設定的結果是，在五個追蹤設定選項裡面我只開啟了 UTM parameters ，這會在 email 裡面放置的超連結後面增加一小串資訊，描述這個連結是來自我的電子報。因此「被連結到」的網站主假設有設定追蹤，就可以知道有一部分的流量是來自我的電子報，但他不會知道這個人是誰，我也不會知道有誰點擊過這個連結。

我覺得這是我可以接受的最低程度、去識別化的追蹤方式。

---

## 所以，Substack 壞壞？我該怎麼辦？

我自己好像還沒有這麼強烈的情緒去控訴 Substack ，一方面是因為我知道這樣的追蹤功能對創作者的誘因以及實質幫助，另一方面是並非只有 Substack 這樣做，絕大多數的電子報服務都會這樣做，甚至會主打更詳細的追蹤與數據分析。

但對於有在使用 Substack 的我來說， Substack 的問題在於**它讓寫作者無法選擇「不追蹤讀者」**；另一方面，**它也讓讀者無法選擇「不被追蹤」**，假設有任一方可以行使積極同意權，我覺得對我來說都很好，但 Substack 沒給大家這樣的選擇機會。

當然，這或許就是為何可以寫作者可以免費使用 Substack 寄信的原因吧。

而回到一般讀者身分，假設不想被 Substack 或者寫作者追蹤，可以怎麼做？

### 選用抗追蹤的 email 服務

例如我有在用的 [Hey](https://www.hey.com/) 或者是 [Proton Mail](https://proton.me/) 都有抗追蹤的功能，以 Hey 來說，他們會攔截掉前文講的那個 1x1 pixel ，甚至把所有信中的圖片都轉透過 Hey 的伺服器中繼，這樣你在 Hey 裡面讀信時，就不會觸發 Substack 的追蹤。（具體說明請參考 Hey 的官方說明： [Spies don’t like us](https://www.hey.com/spy-trackers/) ）

而在 Hey 裡面假設收到帶有追蹤碼的信件，還會有一個望遠鏡的符號告訴你這封信有追蹤，我覺得這是很棒的一個功能，所以看到那些沒有追蹤的電子信時，我都會覺得特別加分。

### 用獨立的 email 收電子信

要申請免洗 email 很容易，創立一個全新的 email 後，大概只有 email 服務商可能知道你是誰，其他人都不知道。所以即使被追蹤，也不用擔心被認出。

另外，像是 Inoreader 或者是 Readwise Reader 等閱讀服務也都有提供獨立的收電子報 email 地址，用這種地址訂閱的話也幾乎不會被識別出來。

不過， Hey, Proton, Inoreader, Readwise Reader 這些服務都要付費，因此若在意這個議題，又不想花錢，可能還是註冊一個新帳號最快，而若不在意的話，那就更沒問題了！

---

## 未來的 Pin 起來電子報不會追蹤你

在發現 Buttondown 可以設定成「不追蹤」後，我透過 Hey 測試了一下，確實如此。

如截圖，在 Hey 裡面，上半部是 Buttondown 寄出的信，旁邊沒有「望遠鏡」的標籤，下半部則是 Substack 寄出的信，旁邊有代表追蹤的「望遠鏡」。
<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/buttondown-vs-substack_aGe3he.webp" data-fancybox data-caption="buttondown-vs-substack">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/buttondown-vs-substack_aGe3he.webp" loading="lazy" alt="buttondown-vs-substack" align="center" />
</a>

而在 Buttondown 的後台，點進使用者的個別頁面後，也只看得到「信有沒有寄到」這個資訊，而無法再看到其他是否有打開、點擊連結的資訊。（ open rate 跟 click rate 也都是 0% ）

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/buttondown-subscriber-events_TLKHLA.webp" data-fancybox data-caption="buttondown-subscriber-events">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/buttondown-subscriber-events_TLKHLA.webp" loading="lazy" alt="buttondown-subscriber-events" align="center" />
</a>

所以在測試後我可以大聲宣布，未來這份電子報不會追蹤你，請放心閱讀（或不讀）。

---

## 我和你的下一步行動

今天這期電子報會是透過 Substack 發出的最後一期，未來都會透過 Buttondown 寄送，對收信的你來說，會有下列變化：

1. 寄件者會由 pinchlime@substack.com 改為我自己網域的 pj@pinchlime.com ，若方便的話，可以請你將這個地址加入聯絡人，避免未來發送的信件被送到垃圾信箱。

2. 由於 Buttondown 的設定更靈活彈性，未來的信件不會像 Substack 一樣，有一個單獨的 Substack 版本連結，而是會直接將網頁版設定為 Pin 起來網站上的連結。

3. 在信件的樣式方面， Buttondown 目前我感覺比 Substack 還要「不好看」一點，如果你有排版或者是字體大小、顏色等等的建議，都歡迎跟我說，我會盡量客製化設定看看。

---

另外，假設你已經順利看到這邊，我想**邀請你訂閱更完整的 Pin 起來網站內容**。

是這樣的， Buttondown 提供了一個為訂閱者分組的功能，並且可以在寄信時選擇「不公開寄送」，透過「不公開寄送」發表的內容，就只會寄給使用者的信箱，不會公布在 Archive 裡面。

對我來說，這兩個功能加在一起的好處是，我可以分別推送不同類型的內容給不同的人。

我目前在 [Pin 起來網站](https://pinchlime.com/)上，把內容分成三類：

1. [電子報](https://pinchlime.com/newsletters/)，是你現在在閱讀的內容，目前是每週固定會發布一篇。

2. [Blog](https://pinchlime.com/blog/)，是我比較完整的文章，通常是介紹一個產品或服務、網站新功能上線、或者是比較完整的論述與工作流分享。

3. [Snapshots](https://pinchlime.com/snapshots/)，是我比較短的、不成熟的想法，可能是我對某件事的疑問，或者是我發現了、嘗試了什麼東西的心得。


先前會透過電子報發送的，只有第一類的內容，而後兩類的 Blog 與 Snapshots 內容我會不定期更新，更新過後通常也只會在 Twitter 上面分享，或者是完全不分享，留給有心人自己瀏覽＆閱讀。


但在開始使用 Buttondown 以後，我覺得也可以透過電子報推送 Blog 與 Snapshots 的內容，所以我會透過 Buttondown 的分組功能來設定。

因此，

* 假設你未來有興趣收到所有類型的 Pin 起來內容，請你透過[這個連結](https://buttondown.email/pinchlime?tag=All)訂閱一次。

* 假設你未來有興趣收到電子報及部落格的內容更新（不包含比較零散的 snapshots ），請你透過[這個連結](https://buttondown.email/pinchlime?tag=Blog)訂閱一次。

* 假設你只想繼續收到電子報，你可以什麼都不做，或者透過[這個連結](https://buttondown.email/pinchlime?tag=Letter)訂閱一次。

什麼都不做的人，我會在下週一次把所有信箱都從 Substack 導入 Buttondown ，並且標記為「只收電子報」。因此即使沒有任何行動，還是可以繼續如以往一樣，收到電子報。

---

## 小結：我不想太依賴 Substack

我這個禮拜一直在想，我到底要不要轉移陣地，其中有兩件事讓我想了一下，

第一件事是，假設 Substack 經營的越來越好，那麼勢必會有這個平台帶來的陌生流量，這會對我有幫助，無論是創作者的互相推薦、或者是隨機的推送與瀏覽，都有機會讓更多人訂閱我的電子報。

第二件事是，以我現在的訂閱人數來說，已經超過了 Buttondown 免費的門檻（一百人），所以我一移轉，就必須開始支付每個月 $9 美元的訂閱費用，而若哪天有幸（不幸？）超過 1000 個訂閱者，費用就會再往上，變成一個月 $29 美元。

關於第一件事，我想完以後覺得，我想讓自己不那麼依賴 Substack （以及任何一個平台），所以在我還沒開始依賴的時候，就更轉向 Buttondown 這種接近自營運的模式，我覺得很好。

而關於第二件事，若是 $9 美元的級距還可以接受＆負擔，若到 $29 的區間，也許我會考慮開放電子報中的廣告版位，或者是接受 donate ，就到時候再說吧！

整體來說，我對「離開 Substack 」這個決策很滿意，

若你也欣賞這樣的轉變，歡迎回信給我跟我說，或是分享這篇文給更多人！

祝一切順利，下期再見！