---
title: 為何我想為網站加上搜索功能？
date: 2023-01-10
description: 我覺得好像是想讓瀏覽的人有更多機會接觸他想看到的內容，無論是什麼，只要搜尋當下有某個念頭，而我又正好寫過相關的東西，相信那樣的體驗一定會很不錯。
path: snapshots/why/why-do-i-want-to-implement-search-function-in-this-site
taxonomies:
  kinds: 
    - Daily Why
  tags: 
    - Search
    - Meilisearch
    - Pagefind
---

在去年七月時，看到 Owen 這篇「[给Zola博客增加搜索功能](https://www.owenyoung.com/blog/add-search/)」文章後非常心動，就很想要找機會幫自己的網站也加上類似的功能，不過後來一直遲遲未展開研究。

前幾個禮拜，看到 [Pagefind](https://pagefind.app/) 這個工具，好像可以為靜態網站建立搜尋 index ，又激起了我的興趣。

今天終於認真想來研究一下，結果發現 Pagefind 對目前的我好像還是有點太進階了。我能夠照著它的教學，在我電腦裡的網站 directory 成功生成 index，但我不知道該怎樣把這個流程也套用到 Netlify 上面，不知道該怎麼讓網站在自動 build 的同時也可以透過 Pagefind 產生 index ，所以就暫且先放棄。

這時又回頭看 Owen 那篇文章，發現我還是很想要有站內搜尋的功能，而且看起來或許可以試試看 Owen 在用的 [Meilisearch](https://github.com/meilisearch/meilisearch) ，不過這部分就過幾天再來研究了。

那麼，為什麼我會想要網站裡有搜尋功能呢？我覺得好像是想讓瀏覽的人有更多機會接觸他想看到的內容，無論是什麼，只要搜尋當下有某個念頭，而我又正好寫過相關的東西，相信那樣的體驗一定會很不錯。

所以為了促成這樣的體驗有機會能真正發生，這幾個月一定要嘗試把搜索功能做出來！（立 flag ）