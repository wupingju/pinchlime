---
title: 建構我的 wiki site
date: 2022-05-06
updated: 2022-05-06
description: 上週透過 Logseq 內建的 export 功能，很順利地把頁面整個輸出成靜態頁面，並且上傳到自己的網域裡面，開始建立自己的小小 wiki page
path: snapshots/what-i-tried-today/first-try-to-build-my-wiki-site
taxonomies:
  kinds: 
    - What I Tried Today
  tags: 
    - Personal Wiki
---

- 上週透過 Logseq 內建的 export 功能，很順利地把頁面整個輸出成靜態頁面，並且上傳到自己的網域裡面，開始建立自己的小小 wiki page。
- 不過這個方式以目前少少的測試頁面內容量來說，打開就需要一點載入時間，而且也無法自訂各種內容（包含 logo 、metadata 等），有點不滿意。
- 所以就開始思考＆研究其他的解決方案，此時看到一篇文章提到可以把 Tiddlywiki 輸出成靜態頁面，就嘗試研究了一下，但研究一晚下來覺得， Tiddlywiki 學習曲線感覺頗高，而且整體編輯或維護的流程有點...繁瑣（可能是我還不太會用），好像也沒有很符合需求。
- 還有一個選項是透過 Logseq 的 [Schrödinger 插件](https://github.com/sawhney17/logseq-schrodinger)，把 Logseq 頁面直接轉成 Hugo 的靜態頁面。 
- 但這個方案感覺起來，反而是以「文章」為主了，不像 Logseq 內建的 Export 功能，在輸出後，還是可以在頁面上面操作它的大綱型介面以及雙向連結。
- 感覺一時之間好像找不太到好的解決方案，需求：
    1. 每月低於 $5 的費用（ Obsidian Publish 好貴）
    2. 能在本機迅速編輯，並且迅速匯出成靜態網頁
    3. 要有雙向連結功能（被連的頁面能看到誰連到它）
    4. 輸出的網頁有辦法自訂一些 metadata
- 結論：我再研究（慢慢等）看看好惹