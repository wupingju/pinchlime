---
title: 嘗試讓 ChatGPT 扮演 Midjourney prompt 產生器
date: 2023-04-04
description: ChatGPT 最擅長模仿文字，所以關鍵在於找出你覺得好的範例，讓他模仿。只要把握這個概念，我相信你也可以做出最符合自己喜好的 Midjourney prompt 產生器，甚至是用在其他的場合，製作不同類型的產生器。
path: blog/let-chatgpt-act-as-a-midjourney-prompt-generator
extra:
  page_type: archive
  image: https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/secret_SEkJBl.webp
---


一直都沒有好好花時間玩 Midjourney ，一方面是因為我沒有什麼美術或視覺的天份或想像力，從小到大無論是美術課拿到一張白紙，或者是玩各種「我畫你猜」的遊戲，我永遠只會畫一棵樹、一個太陽、幾朵雲這樣的情境，因此我自己很清楚，即使用了 Midjourney ，我也不知道該怎麼描述我想要的情境，因為我根本沒有想要描述的東西。

但昨天在 Twitter 上面偶然被演算法推薦了 [Tatiana Tsiguleva](https://twitter.com/ciguleva) 這個帳號，該帳號最近正在進行 Midjourney 100 days 的計畫，分享了許多 Midjourney 的圖以及相關的 prompts ，重點是，有不少圖他都有用一兩個簡單的詞彙描述「主題」。

例如，在這篇[推文](https://twitter.com/ciguleva/status/1637233764656107520)裡她提到的主題是 ”holographic background” ，而附帶的 prompt 是 `digital background, gradient, soft light, low contrast, minimalist, foil holographic --ar 3:2 --v 5 --stop 75` 

在另一則推文裡她提到的主題是 “Tokyo, Japan” ，附帶的 prompt 是 `Tokyo, Japan, street, architecture, minimalistic, abstract, mist, vector, flat, unreal engine, by jewel tones, scandi style, morning, fog, blue and grey, 4k --ar 3:2 --v 4`  

看到這些東西，我突然充滿靈感，覺得好像可以透過 ChatGPT 弄一個「 Midjourney prompt 產生器」出來。於是我就訂閱了 Midjourney 的 basic plan ，一個月 $10 美元，可以產大約 200 張圖，然後就開始測試。

<!-- more -->

---

## Prompt 產生器的 Prompt

我最初版的 prompt 是這樣寫的，請忽略裡面很破的英文用詞與文法：

```markdown
You are a prompt generator, who is an expert for generating prompts from users' input into specific formats.

For example,
when user inputs "holographic background", you will output "digital background, gradient, soft light, low contrast, minimalist, foil holographic";
when user inputs "Tokyo, Japan", you will output "Tokyo, Japan, street, architecture, minimalistic, abstract, mist, vector, flat, unreal engine, by jewel tones, scandi style, morning, fog, blue and grey";
when user inputs "polygons", you will output "digital background, origami, soft light, low contrast, minimalist, foil holographic";
when user inputs "Spacetime" , you will output "Spacetime , minimalistic, abstract, mist, vector, flat, unreal engine, cinematic".

Please give user 3 different prompts with slightly different styles or descriptions, and you will add "4k --ar 3:2 --v 5" in the end of each prompt.

Here is the user input: {{input}}
```

只要把這串文字貼給 ChatGPT ，然後把 “input” 替換成你想要產生的原始項目，它就會幫你產出三段風格各異，有模有樣的 prompts。

例如，我輸入 “a cozy dog in the backyard” ，他就給我這三段 prompts：

* `"a cozy dog in the backyard, warm tones, soft focus, tranquil, vintage, rustic, golden hour, natural light, nostalgic, 4k --ar 3:2 --v 5"`

* `"a cozy dog in the backyard, playful, greenery, sunlit, bokeh, candid, organic, lush, peaceful, 4k --ar 3:2 --v 5"`

* `"a cozy dog in the backyard, hygge, serene, pastel colors, gentle, textured, inviting, cottagecore, charming, 4k --ar 3:2 --v 5"`


這三段 prompts 分別跑出來的是下列這三組圖：

"a cozy dog in the backyard, warm tones, soft focus, tranquil, vintage, rustic, golden hour, natural light, nostalgic, 4k --ar 3:2 --v 5"

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/PJ_Wu_a_cozy_dog_in_the_backyard_warm_tones_soft_focus_tranquil_e6c7266c-5998-400b-a354-737b11487b14_Fl44uD.webp" data-fancybox data-caption="a cozy dog in the backyard, warm tones, soft focus, tranquil, vintage, rustic, golden hour, natural light, nostalgic, 4k --ar 3:2 --v 5">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/PJ_Wu_a_cozy_dog_in_the_backyard_warm_tones_soft_focus_tranquil_e6c7266c-5998-400b-a354-737b11487b14_Fl44uD.webp" loading="lazy" alt="a cozy dog in the backyard, warm tones, soft focus, tranquil, vintage, rustic, golden hour, natural light, nostalgic, 4k --ar 3:2 --v 5" align="center" />
</a>

<br>

---

"a cozy dog in the backyard, playful, greenery, sunlit, bokeh, candid, organic, lush, peaceful, 4k --ar 3:2 --v 5"

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/PJ_Wu_a_cozy_dog_in_the_backyard_playful_greenery_sunlit_bokeh__ccea284a-35f4-4c19-a10a-8ee76859e40b_UQWct1.webp" data-fancybox data-caption="a cozy dog in the backyard, playful, greenery, sunlit, bokeh, candid, organic, lush, peaceful, 4k --ar 3:2 --v 5">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/PJ_Wu_a_cozy_dog_in_the_backyard_playful_greenery_sunlit_bokeh__ccea284a-35f4-4c19-a10a-8ee76859e40b_UQWct1.webp" loading="lazy" alt="a cozy dog in the backyard, playful, greenery, sunlit, bokeh, candid, organic, lush, peaceful, 4k --ar 3:2 --v 5" align="center" />
</a>

<br>

---

"a cozy dog in the backyard, hygge, serene, pastel colors, gentle, textured, inviting, cottagecore, charming, 4k --ar 3:2 --v 5"

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/PJ_Wu_a_cozy_dog_in_the_backyard_hygge_serene_pastel_colors_gen_4509af04-7faa-454a-90c2-bf34a9be627b_hBDTmF.webp" data-fancybox data-caption="a cozy dog in the backyard, hygge, serene, pastel colors, gentle, textured, inviting, cottagecore, charming, 4k --ar 3:2 --v 5">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/PJ_Wu_a_cozy_dog_in_the_backyard_hygge_serene_pastel_colors_gen_4509af04-7faa-454a-90c2-bf34a9be627b_hBDTmF.webp" loading="lazy" alt="a cozy dog in the backyard, hygge, serene, pastel colors, gentle, textured, inviting, cottagecore, charming, 4k --ar 3:2 --v 5" align="center" />
</a>

<br>

---

而若只是單純貼上 “a cozy dog in the backyard” ，V5 版本的 Midjourney 跑出來的圖則是這樣（好啦，也很棒）：

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/PJ_Wu_a_cozy_dog_in_the_backyard_72552e35-d1a0-4415-a218-751b554d1809_5WzqZ6.webp" data-fancybox data-caption="a cozy dog in the backyard">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/PJ_Wu_a_cozy_dog_in_the_backyard_72552e35-d1a0-4415-a218-751b554d1809_5WzqZ6.webp" loading="lazy" alt="a cozy dog in the backyard" align="center" />
</a>

第一次嘗試做這個產生器就有這樣的效果，我已經相當滿意了，但我覺得那個初版的 prompt 只是一個起點，一定可以有更好的版本，所以我接著來分享一下這個 prompt 背後的思路！

---

## 這個 Prompt 產生器背後的原理是什麼？

先前有提過， ChatGPT 很擅長「**模仿文字**」，當你給它幾段固定格式的文字，它就可以學得有模有樣。而他的模仿不只是能夠模仿特殊的「**行文風格**」（例如 midjourney 這種以單詞堆疊的 prompt）而已，還能夠模仿「**邏輯關係**」。

所以我就直接將現成的、網路上看到的這種邏輯關係，設置成這個產生器的預設邏輯，整個概念白話來說是：「當 user 輸入某個單詞 X ，你就輸出一段與這個單詞 X 相關的擴展描述給他」，並且給它幾組範例，讓他能夠照著這些範例的邏輯關係去依樣畫葫蘆。

例如，以前面的 "a cozy dog in the backyard" 為例， ChatGPT 會補足一些常常跟這個詞一起出現的關鍵字，像是 natural light, playful, charming 之類的，假設你輸入不同的詞，他也會給出一些「相關詞描述」。


當它熟悉了這種對應關係，接下來我只要輸入簡單的詞彙， ChatGPT 不僅可以抓到與這個詞彙相關的描述詞，也可以使用類似的文字風格來回覆，所以 prompt 產生器就直接完成了。


不過，這個初版的產生器還很粗糙，因為：

* 我只參考了一個人提供的幾組 prompts ，他們彼此之間的風格很接近，例如都有 minimalist, flat, abstract 之類的關鍵字，這樣可能會誤導 ChatGPT。

* 可能還有一些影響產圖的關鍵資訊需要提供，但恰好這些 prompts 都沒有，所以 ChatGPT 也不會憑空生成這些關鍵。

但我覺得這些問題都還算好解決，假設我能再給出更多有意義且具有多樣性的範例，那麼 ChatGPT 的表現應該就會更好了。

---

## 若你想要也做一個，我推薦你這樣做

首先，你可以跟我一樣，以目前這個版本作為起點，然後去丟你想要產的東西，交給 ChatGPT 完善細節。

接著，把 ChatGPT 給你的 prompts 拿到 Midjourney 去跑，記得可以自己調整一些比例之類的參數。

當你跑出好的結果時，**太好了**，因為這個好的結果，就是一個現成的，可以強化 prompt 產生器的「範例」，你可以馬上把它更新到產生器裡面。

例如，我用產生器測試了 “car, cyberpunk style” ，結果 prompt 產生器給了我這段：” cyberpunk style, car, neon, futuristic, glowing, chrome, metallic, smoke, city, monochromatic, hologram “ ，然後跑出的圖是下面這組我非常滿意的圖：

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/PJ_Wu_cyberpunk_style_car_neon_futuristic_glowing_chrome_metall_2b2479f3-0469-483c-ae7e-e02c9df018e5_AfsRcz.webp" data-fancybox data-caption="cyberpunk style, car, neon, futuristic, glowing, chrome, metallic, smoke, city, monochromatic, hologram">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/PJ_Wu_cyberpunk_style_car_neon_futuristic_glowing_chrome_metall_2b2479f3-0469-483c-ae7e-e02c9df018e5_AfsRcz.webp" loading="lazy" alt="cyberpunk style, car, neon, futuristic, glowing, chrome, metallic, smoke, city, monochromatic, hologram" align="center" />
</a>

只要這樣跑個幾輪，把提供給 ChatGPT 的「範例」換上你實踐過，喜歡的「邏輯對應關係」，你就可以大幅強化這個產生器的能力。

同時，你也可以在這過程中慢慢建立自己對這些描述的偏好，例如，你可以補上一些條件，請他只能選用某幾種風格、或者是避免選用某些風格與關鍵字等等。

這樣持續迭代後，我相信 ChatGPT 會給你很好的結果，讓你每次都能迅速拿到一組符合自己審美的 prompt ，再去交給 Midjourney 跑圖。

---

## 小結：

我覺得在嘗試做這件事的過程中，幾乎沒有什麼卡關的地方，因為 ChatGPT 實在是太聰明、而 Midjourney 經過多次迭代後， V5 版本幾乎也是隨便就能產出美圖。

唯一出自於我自己的，好像也只是某段概念而已：

> ChatGPT 最擅長模仿文字，所以關鍵在於找出你覺得好的範例，讓他模仿。

只要把握這個概念，我相信你也可以做出最符合自己喜好的 Midjourney prompt 產生器，甚至是用在其他的場合，製作不同類型的產生器。

若這篇文章對你有幫助，讓你做出了很棒的東西，歡迎跟我分享，我很期待收到這樣的回饋！

最後附上一張我透過這個產生器產的圖，歡迎猜猜我是用什麼關鍵字產的！

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/secret_SEkJBl.webp" data-fancybox data-caption="secret">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/secret_SEkJBl.webp" loading="lazy" alt="secret" align="center" />
</a>