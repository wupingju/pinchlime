---
title: 如何將 Dendron 輸出成靜態網站並部署到 Netlify？
date: 2022-05-07
updated: 2022-05-07
description: 未來的自動部署也不一定要透過桌面版的 Dendron 進行，只要 repository 有變動， Netlify 就會自動部署差異的內容。
path: snapshots/how/how-to-publish-dendron-notes-to-a-static-website-and-deploy-it-on-netlify
taxonomies:
  kinds: 
    - Daily How
  tags: 
    - Dendron
    - Static Websites
    - Netlify
---

- 今天一整天都在嘗試使用 Dendron 建構我的 wiki site，詳細的步驟之後再來分享，中間遇到了好幾次障礙，差點想放棄。
- 在這邊簡單描述一下整件事的概念，其實跟之前在部落格寫的 [Pin 起來改版了！從 Wordpress 搬家到 Zola！](@/blog/rebuilt-pinchlime.md) Zola 部署概念很像。
- 在 Dendron 資料的根目錄裡面，配置好 `Netlify.toml` 以及依照[官網教學文件](https://wiki.dendron.so/notes/yetuum6o9wZi6eVJQBbQb/)建立的 `dendron-publish-site.sh` 文件後，就可以在 Netlify 裡面直接抓取整個 repository ，並且進行自動部署。
- 換句話說，未來的自動部署也不一定要透過桌面版的 Dendron 進行，只要 repository 有變動， Netlify 就會自動部署差異的內容。
- 這點跟 Zola 的部署方式很像，差異可能在客製化程度以及部署的時間，但兩者類似的流程讓我可以用類似的工具來經營，覺得這是很棒的事。