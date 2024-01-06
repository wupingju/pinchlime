---
title: 2023 年度回顧 - 已經可以想像 2024 的方向
date: 2024-01-06
path: blog/2023-review
description: 寫完這篇文章後，我察覺到的最大變化是，我實際使用這個系統的時間，開始逐漸超過構建與修改系統的時間。換句話說，我好像開始邁入下一個階段，能夠更專注於解決問題，而不只是一直停留在建立解決問題的框架而已，這對我來說是很鼓舞士氣的一件事，也希望可以繼續維持、甚至更精進。
taxonomies:
  categories: 
    - Reviews
  tags: 
    - Productivity
    - Photography
    - Heptabase
extra:
  image: https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/P1000459_WzVnnd.webp
---

今天是 2024 年 1 月 6 日，新的一年的第一週即將過去了，我覺得我若再不寫 2023 的年度回顧，應該就不會寫，因此我決定今天就要把它寫完，快速寫完。

在寫之前，我重新看了去年寫的三篇年度回顧：

- [2022 年度回顧 - 不成熟的隻字片語也有價值](https://pinchlime.com/blog/2022-yearly-review/)
- [2022 年我不再使用的工具 - 還是喜歡，但用不到了](https://pinchlime.com/blog/2022-tools-i-dont-use-anymore/)
- [2022 年開始進入我工作流的好工具們](https://pinchlime.com/blog/2022-tools-started-entering-my-workflows/)

看完我覺得，我以前真棒，或者說，真有空，竟然可以寫完三篇分開的回顧。不過仔細看看，我發現 2023 跟 2022 相較起來，在「個人生產力工具」的使用上變化沒有到太大。換句話說，我確實達成了當時對 2023 年的預期：

> 我自己感覺 2023 年應該不會像 2022 年一樣，再接觸、甚至替換自己的主力工具了。

不過 2023 年仍有非常非常多值得書寫的事，以下逐段展開。

<!-- more -->

---

## 已經完全融入工作的 GPT

雖然我一直都知道這件事，但我還是很難相信，ChatGPT 與 GPT 3.5 以上的 API 才剛推出滿一年沒多久。在 2023 年裡，我好像就這麼自然而然地，接受、習慣、依賴起 GPT 。準確來說，這邊指的 GPT 並不是 ChatGPT 的對話介面，而是各種 “Plus AI” 的生產力工具。

我目前每天都一定會仰賴 GPT 幫我做某些事，絕大多數是協助我書寫更好的英文，這包含了校正文法、翻譯、精煉語句與更改口吻等等。雖然並不是什麼高大上的情境，但真的讓我做許多事情更有效率、更有把握。

工具方面，我有好幾個會頻繁交換使用的工具：

- Raycast：經過一陣摸索與嘗試，我目前沒有訂閱 Raycast Pro 的 AI ，而是隨意選了一個 extension 然後自己用自己的 API 。原因是 Raycast AI 無法讓我「預設使用 GPT 4」，每次想要用都要自己切換，這對我來講失去了訂閱 Raycast Pro 的意義。
- OpenCat：這是一位中國獨立開發者 Baye 開發的 API 串接工具，有很清楚易用的邏輯，可以自訂 custom instructions，最好的地方是可以把特定的 bot 釘選在 MacOS 的狀態列上，我就把我精製的「中翻英機器人」掛在上面，並且設定為 GPT 4 的 API ，只有遇到特別需要精雕細琢的文字，才會用這個 bot 翻譯，其他則使用 Raycast 的 GPT 3.5 處理。
- Bob translator：這也是一位中國開發者開發的翻譯工具，我可以框選一段文字就翻譯成我想要的語言。我也串上了 GPT 3.5 的 API ，所以臨時想翻譯什麼文字時，也會用它處理。
- Intercom：這比較不是一般人熟悉的生產力工具，他是我到 Heptabase 工作後才開始使用的客服平台，在裡面的對話框有內建的 AI assistant，有時候在回覆客戶訊息時，我會請這個 AI 助手幫忙修改文法。
- Spark mail：若是要書寫英文信件，我則會直接使用 Spark 內建的 AI 助手，根據我的經驗，輸入簡單的需求與意圖後，Spark AI 都能跑出很不錯的信件內容。我覺得對我這種還沒那麼習慣英文書信的人來說很有幫助。
- Notion AI：我偶爾仍會用 Notion AI 幫我 Improve writing 或 Simplify language，不過我最近打算再自己建屬於自己的 bot 來處理這件事。

上述大概是我每週至少都會用到一次的 AI 產品，其餘淺嚐而止或很少使用的就略過不提了。另外值得一提的是，上述工具的「使用」，全部都是指「處理英文文字」。我認為我的英文還不夠好，因此加上 AI 的協助可以讓我更好。

不過以漢字的處理來說，我目前還是非常有信心能夠處理得比 AI 好，而且嘗試過幾次讓 AI 加入我的寫作後，得到的內容都讓我覺得那不是我。因此我短時間內還不會讓 AI 介入我的日常書寫。

除了文字處理以外，因為工作實在太繁忙，我幾乎沒有時間再探索其他不同的 AI 應用。不過我倒也不會著急或焦慮，我覺得目前從使用需求出發的搭配方式，對我來講就是最有效率的方式了。

---

## 加入 Heptabase 團隊

2023 年的下半年，我加入了 Heptabase 團隊，這方面的回顧與心路歷程可以看這兩篇紀錄：

- [離開](https://pinchlime.com/newsletters/exit/)
- [從 Heptabase 的懷疑者到傳教士](https://pinchlime.com/newsletters/from-a-heptabase-doubter-to-a-missionary/)

加入至今已經快半年，幾乎沒有好好說過在裡面的心得與收穫，一方面是實在有太多事可以做、需要做、想要做，因此個人時間顯著下降，另一方面是我自己不太習慣頻繁談論任職公司的事情。

不過，在年度回顧好像還是應該提一下。因為這個轉變對我影響深遠。這幾個月下來的濃縮心得是：比想像中還要更好。

我原本加入前想像的是：「我可以跟一群厲害的人一起打造厲害的東西」，但加入之後的體會是：「我不僅可以跟一群超厲害的人打造超厲害的東西，我也可以繼續進步變得比以前更厲害」。

雖然這句話有點囉唆，但它完整表達了我的情緒與感受，我非常喜歡與敬佩我的團隊夥伴們，也感受到原來我還有這麼多不足、可以學習與加強的地方，而且除了感知到自己的不足以外，我也能夠藉由其他人的實際作為或者提醒，知道我怎麼做可以更好。

我現在還沒有辦法說出具體的內容或事件來支撐這些感受，因為有的太機密，有的太私人，但也許在未來某個時間點，我會再分享更多這方面的內容。

---

## 重拾相機拍照

2023 年，在生活上的另一個重要變化是，我重新拾起相機開始拍照了。在 2023 年 5 月時，我接觸到了[只能拍攝黑白照片的 “Monochrome” 相機](https://pinchlime.com/newsletters/camera-that-can-only-take-black-and-white-photos/)，很快地就為此著迷，購入了一台新相機 Q2 Monochrom。

持有這台相機以後，我每天都好開心，即使到現在已經過了半年多，這種開心仍然每天都會冒出來。

我覺得這是因為，我非常喜歡這台相機的一切，持有它令我感到滿足，每次看到它拍出的照片都讓我感到驚豔與開心，帶著它在街上亂晃隨拍時，我能很快進入十多年前大學時那種專注於捕捉瞬間的心流狀態。這些正面的感受疊加起來，就讓我幸福感大增。

我很訝異一台相機能給我帶來這麼多快樂的感受（而且還持續至今），這真的是我 2023 年買入最值得的東西。

---

## 東京自由行

2023 年 7 月底，我與女友（快要改稱老婆了）一起到東京玩了幾天，這離我上一次出國已經 5 年了，而上一次去東京更是已經完全沒有印象的小學時候，因此我很期待這次旅行。

在這幾天裡面，我們去了一些觀光客打卡景點、去了 Fuji Rock 朝聖，也在東京各處的街頭隨意亂晃，7 月的東京非常炎熱，但我們還是每天都走了十多公里的路，非常過癮。

所有去的地方裡面，我們兩個一致都最喜歡下北澤，我自己喜歡當地的氛圍與街景，幾乎每個轉角都有讓我想按下快門的慾望；除了下北澤之外，澀谷一帶的感覺我也很享受。五六天的行程裡面去的地方幾乎沒有不喜歡的。

當然，這也是因為有個很棒的旅伴，我們可以漫無目的地閒晃，逛累了就隨便找間小咖啡廳進去發呆放空，看到想逛的店就進去晃晃，走在路上若發現附近有想去的地方就繞過去看看，能夠有這種可以一起隨遇而安的另一半一起旅遊，真是幸福。

---

## 個人知識管理系統的迭代

在 2023 年 6 月的端午節連假，我寫了一篇「[我的個人知識管理系統](https://pinchlime.com/blog/my-personal-knowledge-management-system-2023/)」。

這篇文章裡面把知識管理分成探索、捕捉、發展、精煉與交流這五個階段，每個階段都有一些目標以及實踐原則。姑且不論別人看完後的想法，我自己覺得光是寫完這篇，就有滿滿的收穫，我不僅確立了一個可以持續迭代與演進的基礎，也從書寫的過程，就知道自己擅長與不擅長哪些，因此知道下一步該怎麼調整與加強。

而在加入 Heptabase 團隊後，我也更了解 Heptabase 背後的方法論與團隊夥伴們自己的學習方式，這些內容又帶給我更多知識管理系統的想法與靈感。同時，Heptabase 仍持續迭代演化，功能也愈來愈完整，這些新增的能力，也讓我能做到更多事情。

從寫完這篇文章後，我察覺到的最大變化是，我實際使用這個系統的時間，開始逐漸超過構建與修改系統的時間。換句話說，我好像開始邁入下一個階段，能夠更專注於解決問題，而不只是一直停留在建立解決問題的框架而已，這對我來說是很鼓舞士氣的一件事，也希望可以繼續維持、甚至更精進。

---

## 小結：已經可以想像 2024 的方向

整體來說，過完整個忙碌、充實的 2023 後，我好像已經可以想像 2024 的樣貌。無論是生活、工作、學習、個人知識管理等等，好像都已經有明確的方向與目標，這種踏實感真的挺不錯的，期待看到這篇文章的你，也可以感受到這樣的氛圍，讓自己有個更棒的 2024 年！

---

最後也跟大家分享去東京玩的時候拍的幾張喜歡的照片（可以點擊放大）！

<br>
<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/P1000420_A7lTdS.webp" data-fancybox data-caption="2023-tokyo-untitled">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/P1000420_A7lTdS.webp" loading="lazy" alt="2023-tokyo-untitled" align="center" />
</a>
<br>
<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/P1000448_UOyjau.webp" data-fancybox data-caption="2023-tokyo-untitled">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/P1000448_UOyjau.webp" loading="lazy" alt="2023-tokyo-untitled" align="center" />
</a>
<br>
<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/P1000503_Py3jrq.webp" data-fancybox data-caption="2023-tokyo-untitled">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/P1000503_Py3jrq.webp" loading="lazy" alt="2023-tokyo-untitled" align="center" />
</a>
<br>
<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/P1000511_H51OZ9.webp" data-fancybox data-caption="2023-tokyo-untitled">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/P1000511_H51OZ9.webp" loading="lazy" alt="2023-tokyo-untitled" align="center" />
</a>
<br>
<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/P1000499_qM6w8r.webp" data-fancybox data-caption="2023-tokyo-untitled">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/P1000499_qM6w8r.webp" loading="lazy" alt="2023-tokyo-untitled" align="center" />
</a>
<br>
<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/P1000559_aElW4K.webp" data-fancybox data-caption="2023-tokyo-untitled">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/P1000559_aElW4K.webp" loading="lazy" alt="2023-tokyo-untitled" align="center" />
</a>
<br>
<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/P1000556_pNo9MR.webp" data-fancybox data-caption="2023-tokyo-untitled">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/P1000556_pNo9MR.webp" loading="lazy" alt="2023-tokyo-untitled" align="center" />
</a>
<br>
<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/P1000561_3EbFxh.webp" data-fancybox data-caption="2023-tokyo-untitled">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/P1000561_3EbFxh.webp" loading="lazy" alt="2023-tokyo-untitled" align="center" />
</a>
<br>
<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/P1000459_WzVnnd.webp" data-fancybox data-caption="2023-tokyo-untitled">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/P1000459_WzVnnd.webp" loading="lazy" alt="2023-tokyo-untitled" align="center" />
</a>