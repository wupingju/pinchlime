---
title: 更換了網站的字型為「金萱那提」
date: 2023-04-20
updated: 2023-04-20
description: 在全部設定完成後，我發現，我又更喜歡這個網站了！這樣的喜歡，會促使我更想在上面寫東西，即使只是寫給自己看，都非常開心。
path: blog/changed-font-to-jinxuan-latte
taxonomies:
  categories: 
    - Pinchlime
  tags: 
    - Blog
extra:
  page_type: archive
  image: https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/pinchlime-new-font_ATleKx.webp
---

這兩天的下班零碎時間都在做一件事：更換網站的字型。

今天終於全部弄好了！目前看到的這個畫面，就是掛載新字型的 Pin 起來。

這篇來簡單分享一下心得！

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/pinchlime-new-font_ATleKx.webp" data-fancybox data-caption="pinchlime-new-font">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/pinchlime-new-font_ATleKx.webp" loading="lazy" alt="pinchlime-new-font" align="center" />
</a>
<br>
---

## 為什麼要換字型？

原先網站使用的是 [Inter 這個字型](https://fonts.google.com/specimen/Inter) ，我自己的感覺是還算喜歡，但好像就這樣而已，而且一時之間也沒有更好的想法。但一直都想說，若看到更喜歡的，我一定要來換換看。

前天不知道是哪邊突然靈感乍現，想說來研究看看好了，就搜尋了一下之前曾看過不少字型募資專案廣告的 [justfont](https://justfont.com/) ，結果發現，好像…不貴耶。

若直接買斷字型的話是[還蠻貴的](https://store.justfont.com/)（都要數千、甚至上萬台幣），但若要把特定字型放在網站上，要看的會是 [webfont](https://webfont.justfont.com/membership) 的授權，以付費方案來說最便宜的是每年 588 元台幣，可以有 100,000 次 page views 的額度。我算了一下，以目前的流量有可能會超過，但超過的話也不賴（？

總之，購物慾被激發，想說反正可以退費，我就直接刷卡開始試用了。

---

## 我換了什麼字型？

由於這個網站的樣式都是自己設定的，要換字型還算簡單，只要在 CSS 的 font-family 依照 justfont 的指示新增字型代號就好。 justfont 也有還算清楚的[設定說明](https://webfont.justfont.com/cheats)可以參考，我就先把他提供的 javascript 代碼放在網站的 <head> 區塊裡，接著就開始挑選要用哪個字型。

我嘗試了下列幾種：

* 蘭陽明體
* 凝書體
* 金萱
* 金萱那提
* 思源宋體

為了比較，我還把他們都截圖放到 Figma 裡面對照：

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/pinchlime-new-font-2_dAuj9b.webp" data-fancybox data-caption="pinchlime-new-font-2">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/pinchlime-new-font-2_dAuj9b.webp" loading="lazy" alt="pinchlime-new-font-2" align="center" />
</a>
<br>

最後勝出的是由圓體搭配明體設計的[金萱那提](https://justfont.com/jinxuan-latte/)，我自己也有點意外，若單看字型的話，我好像更喜歡的是融合明體與黑體，看起來更典雅的[金萱](https://justfont.com/jinxuan/)，但搭配自己的 blog 文字後，我覺得金萱讀起來好像更嚴肅、更有距離感一點，而金萱那提閱讀起來則是更親近、更自在一點，所以最後就選擇使用金萱那提了。


<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/jinxuan-latte_EhaXlW.webp" data-fancybox data-caption="jinxuan-latte">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/jinxuan-latte_EhaXlW.webp" loading="lazy" alt="jinxuan-latte" align="center" />
</a>
<br>

_圖：金萱那提，來源：[justfont](https://justfont.com/jinxuan-latte/)_

---

## 順便簡化了網站的架構

在換完字型後，我發現整個網站上有三個頁面，不知為何，無法生效。他們分別是 [Blog](/blog), [Newsletters](/newsletters), Snapshots 這三個主頁面，這三個頁面的共通點是，他們都會讀取該類別的所有文章，依照時序倒序呈現概要內容。目前已經修改掉了，[但可以看 wayback machine 的備份頁面參考](http://web.archive.org/web/20230203224114/https://pinchlime.com/blog/)。

我研究後猜測，可能是因為這幾頁都使用到架站系統 Zola 的 “paginator” 功能，有可能是 bug 的原因，導致 justfont 的 script 無法生效。於是我決定，山不轉路轉，直接修改這幾頁的架構。

修改後，這幾頁不再呈現文章的部分預覽內容，而是直接變成列表的形式，只提供標題以及發布日期。

我覺得這樣修改有些好處也有些壞處。

好處是，頁面看起來更簡潔了，基本上第一層的頁面都只有提供列表，讀者要點開文章的連結，才看得到裡面有什麼資訊，以我自己的瀏覽習慣來說，這樣能夠更快速的瀏覽「所有文章」，並且一次開啓自己有興趣的連結。而我猜想，這樣也可以減少被判定為「duplicated pages」的狀況。

壞處是，有些讀者可能更喜歡先大致上瀏覽文章的開頭，再點開有興趣看的文章詳讀。改版後的網站就比較沒辦法這樣。

但任性的我，為了讓新字型能夠完整裝設，決定還是直接修改了這幾個頁面的呈現方式。

---

## 結語

在全部設定完成後，我發現，我又更喜歡這個網站了！這樣的喜歡，會促使我更想在上面寫東西，即使只是寫給自己看（像是 [Stream 頁面](https://pinchlime.com/stream/2023/)），都非常開心。

也希望大家會喜歡放上這個新字型的網站！