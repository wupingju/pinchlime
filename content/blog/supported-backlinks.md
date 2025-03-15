---
title: 部落格加上了 Backlinks 的功能
date: 2023-01-20
updated: 2023-01-20
description: 自動 backlinks 是我一直很想要放在網站上的功能，它能夠讓讀者更有機會在站內穿梭瀏覽，甚至是發現其他相關的、可能有興趣的內容。
path: blog/supported-backlinks
taxonomies:
  categories: 
    - Pinchlime
extra:
  page_type: blog
  image: https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/backlinks-demo_fu67Vw.webp
---

### 先前的失敗經驗

先前 Zola 在更新到 [0.16.0 版本](https://github.com/getzola/zola/releases/tag/v0.16.0)時，上線了 backlinks 的功能，但當時看不太懂該怎麼裝設。過了一陣子看到 [Owen 的部落格有設定成功](https://www.owenyoung.com/en/changelog/#2022-07-09-support-backlinks)，但我照著做以後仍然卡關失敗，就先暫時放棄了。

今天逛到 Owen 的部落格時又看到一次，決定再來挑戰看看。

一開始仍然失敗，無法抓到任何的 backlinks ，於是我再次跑去看 Zola 的官方文件，發現還是看不懂；又自己亂改了一下，也仍然失敗，甚至叫了 ChatGPT 幫忙，也沒有用。

<!-- more -->
---

### 原來跟站內連結的設定方式有關

最後我快放棄時，在 Zola 的官方論壇裡面找到 Zola 開發者提供的[一個關鍵的提示](https://github.com/getzola/zola/issues/1496#issuecomment-1215446770)：必須要使用 Zola 的 internal links 格式才行。

原先我設定站內連結的方式是設置相對路徑，例如某篇文章的對外路徑是：
https://pinchlime.com/blog/article ，

我在設置站內連結時，就會設定為它的相對路徑 `/blog/article`。

但根據 Zola 論壇的這個資訊，站內連結要依照 Zola 的規則，設定為 `@/blog/article.md` ，這樣設定後，Zola 才會識別為站內連結，並且能夠跑出 backlinks 的內容。

照著調整後，終於成功了！

---

### Backlinks 對我的意義

設定成功的當下真的是非常開心，因為自動 backlinks 是我一直很想要放在網站上的功能，它能夠讓讀者更有機會在站內穿梭瀏覽，甚至是發現其他相關的、可能有興趣的內容。

---

### Zola Backlinks 的侷限

不過在簡單設定以後，發現目前 Zola 支援的 backlinks 資訊只有「連結」跟「標題」而已。

換句話說，我暫時還沒辦法如 [Andy Matuschak 的網站](https://notes.andymatuschak.org/About_these_notes?stackedNotes=z4SDCZQeRo4xFEQ8H4qrSqd68ucpgE6LU155C)這樣，直接在下方呈現 backlinks 的摘要或描述文字。我也沒辦法顯示 backlinks 在我網站裡的分類與發布日期。



不過我覺得已經很棒了，光是「自動產生連結」這件事，就能夠省去我很多手動編輯的時間。

---

### 最後設定的結果

我最後選擇把 backlinks 區塊放在內文段落的下方、留言段落的上方，並且也微調了一下這個區塊的標題。

原先在考慮是否該使用「Backlinks」，但我覺得這個詞對於一般人來說可能有點陌生、無法理解，因此我還是參考了上面提到的 Andy Matuschak 網站，把這個區塊命名為「Links to this page」，並且參考 Owen 的程式碼，加上了數量的資訊，如下圖，這是「迅速迭代功能的 Heptabase 已成為我最愛用的知識管理工具」這篇文顯示的 backlinks 區塊。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/backlinks-demo_fu67Vw.webp" data-fancybox data-caption="backlinks-demo">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/backlinks-demo_fu67Vw.webp" loading="lazy" alt="backlinks-demo" align="center" />
</a>

如果你有其他建議或回饋，也歡迎跟我分享，感謝！