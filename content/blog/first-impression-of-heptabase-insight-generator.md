---
title: Heptabase 的 Insight Generator 好在哪？ 
date: 2024-09-05
updated: 2024-09-05
path: blog/first-impression-of-heptabase-insight-generator
description: Insight Generator 不試圖代替我理解，而是協助我理解，並且讓我從線性的理解架構解脫，轉為那種「逛地圖」式的快速鳥瞰體驗，這是我強烈感受到的價值。
taxonomies:
  categories: 
    - Heptabase
extra:
  page_type: blog
---

昨天，[Heptabase](https://get.heptabase.com/pinchlime) 推出 v1.36.0 版本，上線了 [Insight Generator](https://www.youtube.com/watch?v=uYGqvEksAz8) 這個功能。他可以透過 AI 的協助，從你選定的文章卡片，產生出幾個 “insight” 段落，並附上相對應的原文段落。

我覺得這個功能並不是「萬用型」的工具，而是一個很適合在特定情境與工作流裡面使用的功能。因此想寫一下我自己的觀察與理解，希望讓更多人能夠更加發揮這個功能的價值。

## Insight Generator 可以節省時間，但不是完全不用花時間

首先，Insight Generator 並不是一個「全文總結／摘要工具」。以我自己的理解，總結或摘要是「用一段較短的話描述整篇文章最重要的概念或資訊」。

以 Paul Graham 這篇 “[Superlinear Returns](https://paulgraham.com/superlinear.html)” 來說，我用 Readwise Reader 產出的摘要是：

> Superlinear returns in business and other fields mean that success grows exponentially rather than linearly. Focusing on learning and curiosity can help individuals tap into these returns and achieve exceptional results. This concept applies broadly, from science to fame, highlighting the importance of pursuing interests deeply.

> 「在商業和其他領域中，超線性回報意味著成功是指數增長而非線性增長。專注於學習和好奇心可以幫助個人利用這些回報，並取得卓越的成果。這個概念廣泛適用，從科學到名聲，強調深入追求興趣的重要性。」

而透過 Heptabase 的 Insight Generator ，會得到的是下圖這些短短的大約 20-50 個字的「直述句」，他們並不是整篇文章的摘要，而是每一小段的摘要，由於摘要通常都是壓縮後的內容，原始的資訊較少，肯定看起來就沒有全文摘要那麼「精煉」或者「有洞見」。但這正是 Heptabase 希望達到的效果。

<a href="https://image-webp.pinchlime.com/CleanShot-2024-09-05-22-26-10_4M35hO.png" data-fancybox>
  <img src="https://image-webp.pinchlime.com/CleanShot-2024-09-05-22-26-10_4M35hO.png" loading="lazy" align="center" />
</a>

對我來說，這個 Insight Generator 的目標並不是幫助你快速得到有價值的洞見，而是希望你大幅降低「閱讀 → 建立自己的理解 → 產生自己的洞見」這個流程所需要花費的時間，核心的重點是「自己的」。

同樣以 Superlinear 這篇文章為例，在看到 Insight Generator 產出的這些內容後，我可以花上一兩分鐘快速閱讀這十幾項短短的「主題」，然後挑我感興趣的點開來看，或者是我先把他們分別都放在白板上，然後把類似的段落一起打開來看，看的過程就會記下筆記、寫下我自己的理解內容。

這個過程比起傳統的閱讀方式還要省時與省力，省時在於，假設我看了一下發現產出的 insights 都是我原本就知道、理解的事，那我就沒必要細讀了，而假設其中只有一兩項是我特別有感的，我就只要讀那一兩項就好，但如果每一項都是我有感覺的東西，我就可以花時間好好精讀，這樣快速篩選判斷可以省去許多不必要的時間浪費。

省力在於，透過 Insight Generator ，我得到的是許多大約 60% 精準程度的摘要總結作為「錨」。有了這些錨之後，我可以更輕鬆地產生想法，例如，我可能會好奇原文提出的論證是什麼，因此就帶著問題意識去閱讀。我可能一看到 insight 就產生了同意或反對的想法，所以這些想法又是什麼？

換句話說，這些原始產出的 insights 就是 prompts ，不斷促使我產生疑問與想法，而不是邊讀邊思考邊回想，讀完還要再從頭做一遍筆記。

我認為， Insight Generator 最有價值的地方是「大幅降低建立深度理解所需要時間」，但不可能完全不花時間，因為如果要真的建立理解與洞見，還是一定要自己讀、自己拆解、整理、重組東西，才會長出自己的東西。

---

## Insight Generator 更適合用來處理複雜的、長篇的文字

如同前面提到的，Insight Generator 是分段去拆解摘要，因此如果原文很短，那其實也沒什麼摘要好拆。如果原文的結構已經非常清楚明確，每一段落的主題與內容量都適中，那 Insight Generator 可能也沒辦法讓這篇文章變得更好讀更好懂。但是針對很複雜的文章（例如夾敘夾議、非母語的文章、自己不熟悉的領域的文章、或者非常長的文章），Insight Generator 就有發揮的空間。

另外，我自己認為 Insight Generator 最適合處理的是 Podcast 訪談的逐字稿。通常有價值的 Podcast 都需要參與對話的人經過一段時間的暖身鋪陳，進入正題，才會在對話之中蹦出一些靈光一閃的火花，這些火花如果沒有實際去聽，真的就感受不到。但是要聽完這些 podcasts 真的太花時間了。

在有了 Insight Generator 後，我大量丟入 podcast 訪談的逐字稿，並且使用 Insight Generator 的 “Transcript” 選項去處理這些逐字稿，得到的結果非常好，我可以更快找到「我感興趣的段落」，然後就去看／聽那一段的內容就好。

這樣做可以省下非常非常多的時間，而且又真的能得到原始對談的 insights。我有使用過其他產品的 AI summary 功能試圖達到這個效果，但都做不到，我總是會懷疑 AI 產生的 summary 到底有沒有過度解讀某些段落，或遺漏了什麼「只有我感興趣」的資訊。

---

Insight Generator 不試圖代替我理解，而是協助我理解，並且讓我從線性的理解架構解脫，轉為那種「逛地圖」式的快速鳥瞰體驗，這是我強烈感受到的價值。

希望看了這篇文章的你，也能感受到這種被 LLM 與整合體驗優秀的好工具賦能的感覺！