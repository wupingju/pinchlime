---
title: 讓 ChatGPT 搭配 Midjourney 一起以圖產圖
date: 2023-04-08
updated: 2023-04-08
description: ChatGPT 很適合拿來處理這種整合、重組文字的工作，我相信若再測試更多輪，人工微調 prompt ，它整合的效果會更好。
path: blog/let-chatgpt-boost-midjourney-image-to-image
extra:
  page_type: archive
  image: https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/animals-merged_ipmegk.webp
---

前幾天分享的『[嘗試讓 ChatGPT 扮演 Midjourney prompt 產生器](@/archive/let-chatgpt-act-as-a-midjourney-prompt-generator.md)』，得到不少迴響，很感謝大家。

今天繼續來分享一個小小的嘗試：透過 ChatGPT 搭配 Midjourney 近期新推出的 /describe 功能，在 Midjourney 裡面「以圖產圖」。

<!-- more -->

---

## 什麼是以圖產圖？

先簡單定義一下，我提到的「以圖產圖」，意思是我希望 AI 工具可以直接把我丟進去的圖，重製成一個新的版本，希望在維持原先概念的情況下，有一些隨機的變化。

目前以我的理解， Midjourney 還沒辦法「直接」做到這件事。Midjourney 有內建 “[image prompts](https://docs.midjourney.com/docs/image-prompts)” 的功能，但沒辦法單純丟一張圖就產不同版本，得要用這張圖搭配某些文字 prompts 才能夠產圖。

不過， Midjourney 本週推出了[新功能 “/describe”](https://twitter.com/midjourney/status/1643053450501169157) ，使用者只要上傳一張圖片，Midjourney 就會識別這張圖片，並且回傳給使用者四段稍微有點不同的描述。使用者可以接著透過這些描述產圖。

例如，我上傳了 Pink Floyd 的 Wish You Were Here 這張專輯的封面， Midjourney 就產出了四段不同的描述。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/midjourney-describe_cPiMn2.webp" data-fancybox data-caption="midjourney-describe">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/midjourney-describe_cPiMn2.webp" loading="lazy" alt="midjourney-describe" align="center" />
</a>
<br>

接著，我只要點選下方的任何一個數字，就可以依照該描述在 Midjourney 裡面產圖。

---

不過，在我測試了幾張圖之後，我發現這樣做的效果大概只到 70 分的程度，常常四個按鈕都試了以後，發現每個都有一些好的地方，但也都有一些不足的地方。如下圖，左上是第一組，右上是第二組，左下是第三組，右下是第四組：

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/wish-you-were-here-described_a2fW7q.webp" data-fancybox data-caption="wish-you-were-here-described">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/wish-you-were-here-described_a2fW7q.webp" loading="lazy" alt="wish-you-were-here-described" align="center" />
</a>
<br>

我猜想可能是因為 describe 這個功能才剛推出，或者是 Midjourney 是想透過這個方式來訓練他們的「圖生文」模型，還沒完全釋放出最精準的辨識能力。

總之我對於 describe 功能還沒有到非常滿意，但此時我又想到了 ChatGPT ！

---

## 先讓 ChatGPT 整合四段描述

我想到的是，我現在已經有四段彼此相關的某個描述了，好像很適合透過 ChatGPT 把它們組合在一起。

因此我就以下列這段 Prompt 簡單嘗試了效果：

>（上半部直接貼上 Midjourney 給你的四段描述）

> Hi chat, the four descriptions above are all generated from a same image using an image-to-text AI recognition method. In other words, they each represent different aspects of the image, just with different degrees of emphasis. I hope you can merge these four descriptions, remove some unimportant parts and choose the most relevant style to create a description that is closest to the original image. I don't want you to just pile these descriptions on top of each other; I hope you can create a meaningful combination so that I can use this recombined description to create a new image that is closest to the original image. Please create a combined description for me in a similar format:


依照這個 Prompt ， ChatGPT 會嘗試組合他接收到的四個描述，轉化為一個新的版本。以上面同樣的 Wish You Were Here 封面為例，他給出的結果是：

> Pink Floyd album cover featuring two men shaking hands on a street, in the style of light orange, bronze, and a hint of indigo, utilizing a photographic source and cinestill 50d. The image captures emotional gestures and a streetscape setting, with brass and chrome-plated elements, creating a dreamlike yet street-inspired atmosphere. The cover art combines influences from group f/64, Danny Lyon, and Frank Miller, showcasing a wry and emotive touch, with subtle McDonaldpunk and chromepunk undertones.

稍微比較一下，確實沒有完全照著疊加描述，好像還不錯！

---

## 再讓 Midjourney 產圖

接著，我再拿這段 prompt 直接丟給 Midjourney 產圖，我覺得表現好像更好了。


<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/wish-you-were-here-merged_TadvUO.webp" data-fancybox data-caption="wish-you-were-here-merged">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/wish-you-were-here-merged_TadvUO.webp" loading="lazy" alt="wish-you-were-here-merged" align="center" />
</a>
<br>

其中我最喜歡的是第二張，因此我請它 upscale 放大，成品如下圖：

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/PJ_Wu_Pink_Floyd_album_cover_featuring_two_men_shaking_hands_on_414bad5a-0522-412e-a673-e11a8df9804b_YgHhwa.webp" data-fancybox data-caption="wish-you-were-here-merged-2">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/PJ_Wu_Pink_Floyd_album_cover_featuring_two_men_shaking_hands_on_414bad5a-0522-412e-a673-e11a8df9804b_YgHhwa.webp" loading="lazy" alt="wish-you-were-here-merged-2" align="center" />
</a>
<br>

我也透過這個方式再測試了兩張 Pink Floyd 的專輯封面，發現透過 ChatGPT 融合過後的版本都更接近原版一些，這邊就直接貼我最喜歡的原版＆成品對照，左邊都是原圖，右邊是 Midjourney 產出的圖。

**Animals**

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/animals-merged_ipmegk.webp" data-fancybox data-caption="animals-merged">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/animals-merged_ipmegk.webp" loading="lazy" alt="animals-merged" align="center" />
</a>
<br>

**The Division Bell**

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/the-division-bell-merged_eMU3bu.webp" data-fancybox data-caption="the-division-bell-merged">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/the-division-bell-merged_eMU3bu.webp" loading="lazy" alt="the-division-bell-merged" align="center" />
</a>
<br>

---

## 小結：

我自己對這次嘗試的成果還蠻滿意的，雖然有可能是因為 Midjourney 本來就相對熟悉 Pink Floyd 的封面美術風格，但我也有嘗試直接丟專輯關鍵字下去跑，效果也沒有 ChatGPT 加持的版本好。

ChatGPT 很適合拿來處理這種整合、重組文字的工作，我相信若再測試更多輪，人工微調 prompt ，它整合的效果會更好。

後續我應該會再繼續嘗試更多不同的圖片類型以及 prompt ，有新的心得再來分享！