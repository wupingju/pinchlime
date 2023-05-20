---
title: 讓 ChatGPT 維持脈絡以及提供把握度
date: 2023-02-27
description: 我覺得「脈絡問題」與「把握度問題」，在我身上造成的影響主要是浪費時間，我必須反覆重新對話以取得符合上下文脈絡的回答，我也必須花額外的時間去驗證不熟悉答案的正確性。這些都會降低我的使用效率。
path: newsletters/keeps-chatgpt-in-the-context-and-provide-certainty
extra:
  issues: 21
---

## 閒聊

Hi 大家好，由於昨天出遊，所以電子報晚一天發出。

上週的電子報裡面，我有說接下來會把內容更簡化一些，另外也會多一段「閒聊」的段落。發出後有收到一些回饋，大致上都是說這樣調整還不錯，比較容易順順地讀完。因此這個模式應該會繼續試一陣子看看。

另外，這禮拜的電子報內容也有一點不一樣，因為我對於想講的主題有很多想法，字數已經很多，所以就不提供選讀內容了。

在進入本週的主題之前，我想先分享一下前幾天在做的東西： Stream 。它是我網站上的一個新頁面，詳細的介紹可以看這篇：「[建了一個迷你版的個人 Twitter ： Stream](@/blog/built-a-personal-twitter-the-stream.md)」，會想做這個的原因是，我感覺在 Twitter 上面分享想法或內容時，大多還是會帶有某種「這個東西會被人看到」的預先認知，因此寫出來的東西會有更多一點的包裝跟編排。

但某些時候還是會有種包袱，比方說擔心一直分享東西會太洗版，或者是分享我自己還沒有很理解的東西可能會被認為是在跟風或誤導，雖然大家都說 Twitter 是樹洞，但以我的使用方式來說，還是會有一些自我審查存在。

但我想像中的 Stream 就不太一樣了，平常不會特別去分享那個頁面，在這一兩篇介紹文之後，會不小心點去看的人可能也不多，我好像會更願意把更零碎的發現與想法放在上面。而我也不擔心有人很頻繁地去看，因為那代表這個人可能對我的文字或想法很感興趣，這樣也很好。

總之，Stream 是我再次切分出來的某種表現形式，對我來說，不同形式的內容可能適合以不同方式呈現，當我釐清、也認可自己的分類後，我在呈現這種內容時就會更無阻礙。

以下是今天的主題，讓 ChatGPT 維持脈絡以及提供把握度。

<!-- more -->

---

## 脈絡與把握度

這週比較沒有在使用 new Bing ，但仍然花了不少時間在跟 ChatGPT 對話，我甚至在想要開一個頁面專門放比較有趣、有價值的那些對話了。

在跟 ChatGPT 反覆對話的過程中，我常常在思考怎樣可以得到更符合我需求的回答，此時我發現我對 ChatGPT 還不夠滿意的地方，主要有兩件事：

1. 在有一定長度的對話裡面，ChatGPT 會「突然間」忘記之前下過的指令與對話紀錄，然後就回覆給你完全莫名其妙的答案。

2. 因為 ChatGPT 無法聯網、所掌握的資料只到 2021 年底，因此它在回答時有時候會唬爛。如果是自己本來就知道的事那還好，馬上就可以看穿它在亂講話，但我們在使用時，時常會詢問的是自己也不一定有把握的事情，此時就會需要額外的驗證時間。

我覺得「脈絡問題」與「把握度問題」，在我身上造成的影響主要是浪費時間，我必須反覆重新對話以取得符合上下文脈絡的回答，我也必須花額外的時間去驗證不熟悉答案的正確性。這些都會降低我的使用效率。

針對脈絡問題，剛好，本週我看到[一篇文章](https://blog.meathill.com/tech/everything-i-know-about-chatgpt-develop-further-limitation-future-effects.html#4097-tokens)說 ChatGPT 的對話不僅是「單次對話」有字數限制，就連它保留的上下文情境也有字數限制。在得知這個資訊後，我開始測試是否真的是這樣，也思考該如何應對這個限制。

而針對把握度的問題，我則是嘗試讓 ChatGPT 去自行分類他回答內容的把握度。以下簡單說明一下兩個方面的收穫。

---

## 維持脈絡的關鍵：控制字數，持續總結

### ChatGPT 的字數限制

我實測字數限制的結果是， ChatGPT 真的會在輸入 2000 字左右時，就開始忘掉前面的設定。我的測試方式很簡單：

1. 我先跟他約定某個通關密語：「context」

2. 我開始輸入無腦字串，例如總長 500 字的「測試」兩個字。

3. 接著我問他我們的通關密語是什麼？正常狀況下他會回答是「context」

4. 重複這個流程，當我輸入第 1501-2000 個「測試」以後，下一次問他通關密語時，他不再回答「context」，而是會亂掰，像是什麼「開啟新世界的鑰匙」之類的。

---

### 解決方案

為了解決這個問題，我想出來的方法是，要監控字數並保持安全水位。

我用的是蘋果內建的 pages 來確認字數，每當我發現我的輸入字數已經超過 1500 時，就不能再繼續輸入，必須要「總結」先前討論的內容。

例如，當他照著我的內容規範，持續用某種風格撰寫文字，已經撰寫了三段，還有剩下五段。

此時我會請他先各用一句話總結前面三段的內容。接著，重啟新局。

但在重啟新局時，除了預先設定好的內容規範，我也會提醒他，我們先前已經寫過三段的內容，每段的概要是什麼，接著再請他依據內容規範往下處理。

透過這種持續總結、重複提醒規則的作法，就能更好地讓 ChatGPT 始終處於對話脈絡中，不會跑到一半就岔題、忘記之前的約定是什麼。

不過這種做法仍有限制，例如，當討論的內容很難被簡單總結時，這套做法就行不通，一定會遇到脈絡儲存的上限。另外，即使可以儲存脈絡的摘要，但持續產出再壓縮，還是會讓摘要越來越多，最終也會遇到上限。因此還是趕快期待 ChatGPT 把限制打開，讓我們可以維持更長的對話脈絡吧。

---

## 驗證把握度的關鍵：為回答分類

### 兩種常見的錯誤狀況

對於 ChatGPT 有可能鬼扯的狀況，我目前比較常遇到的有兩種類型：

1. 針對他「不完全知道」的事，他為了湊出答案，會自動填充錯誤內容

2. 針對他「以為他知道」的事，他會講的斬釘截鐵，不考慮可能的錯誤狀況。

第一種類型，舉例來說，當我用中文問他台灣的某某地方有什麼美食時，它會亂湊資訊，講得煞有其事。其中可能有部分內容是正確的，但也有完全亂掰的。

第二種類型，舉例來說，當我問他「現任 Twitter 的 CEO 是誰？」它會很有把握地說「Jack Dorsey」，但那個資訊已經過時了。這種回答跟第一種類型不一樣的地方在於，它以某個時間點來說是完全正確的，但時間會變，此時就開始變得不一定正確。

---

### 三種不同的回答方式

基於上面這兩種類型，我嘗試出一套預設指令，我請他在回覆問題時，除了回覆內容之外，也一併回覆他的「把握程度」。並且我定義了三種不同的回答方式。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/reply-rules-about-certainty_HgmtFc.webp" data-fancybox data-caption="reply-rules-about-certainty">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/reply-rules-about-certainty_HgmtFc.webp" loading="lazy" alt="reply-rules-about-certainty" align="center" />
</a>

第一種是針對那些通常「有標準答案」的問題，請他回覆時回答「 100% 有把握」。

第二種是針對那些具有時效性的問題，請他回覆時要提到這個侷限。

第三種是，假設不屬於前兩者的問題，請他回答時，一併回覆「這個問題可能還有其他的版本或說法。」

我發現，在這樣子指示後，雖然結果還不能說 100% 滿意，但至少比沒有下指令的方式好。

例如第一種類型的狀況：

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/first-type-answer_tfyrtA.webp" data-fancybox data-caption="first-type-answer">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/first-type-answer_tfyrtA.webp" loading="lazy" alt="first-type-answer" align="center" />
</a>

第二種類型的狀況：

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/second-type-answer_b40CwB.webp" data-fancybox data-caption="second-type-answer">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/second-type-answer_b40CwB.webp" loading="lazy" alt="second-type-answer" align="center" />
</a>

第三種類型的狀況，框起來的是錯誤資訊或是根本沒這東西。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/third-type-answer_jx4W4r.webp" data-fancybox data-caption="third-type-answer">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/third-type-answer_jx4W4r.webp" loading="lazy" alt="third-type-answer" align="center" />
</a>

我覺得一定還有更省力的指令、或者是其他不同的「錯誤狀況」可以去細分，但能夠讓 ChatGPT 每次回覆時都多帶一句把握度的資訊，我覺得是很不錯的一件事。

---

### 小結：掌握規則與限制有助於提高效率

在進行這些測試時，我有一直在思考「為什麼我要測這些東西？」

坦白說，即使知道可以照今天的作法使用，我仍然不會去問 ChatGPT 事實層面的資訊，因為那不是目前他擅長的事。但除了知道他不擅長以外，我還是會好奇，雖然不擅長，但有沒有哪些類型是屬於「非常不擅長」，哪些是屬於「普通不擅長」？

這種更細微的程度區分，是我很好奇的事。

為什麼好奇呢？我覺得好像跟我的個性有關，從小就很喜歡設定規則與探索規則，長大以後發現除了明文規則以外還有大家都心照不宣的潛規則，或者是明明有訂，但卻沒有特別被說明的規則。

以我的經驗來說，若能夠摸清這些規則的邊界，在做事時就可以更輕鬆、更有效率。那為何想更輕鬆、更有效率？我想是因為懶惰吧！


_最後，若你有更好的指令方式或者是想要討論、更正我的說法做法，都很歡迎你跟我分享！_