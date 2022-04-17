---
title: Pin 起來改版了！從 Wordpress 搬家到 Zola！
date: 2022-04-17
updated: 2022-04-17
draft: true
taxonomies:
  categories: 
    - Pinchlime
  tags: 
    - Wordpress
    - Zola
    - Netlify
    - Github
    - Markdown
---

來跟大家分享以及更新一下，目前看到的這個網站「 Pin 起來 ／ Pinchlime.com 」，在今天（2022.04.17）進行了一次大改版。

改版前，這個網站是透過 [Wordpress.com](https://wordpress.com/) 運作的，包含網域的託管，以及內容的管理與撰寫，都是在 Wordpress.com 上面進行。

改版後，這個網站的運作則切成了幾個不同的部分：

- 網站內容的撰寫：透過 markdown 文件進行
- 網站的生成：透過 [Zola](https://www.getzola.org/) 這個靜態網站產生器，將 markdown 文件轉成 html 檔案。
- 網站的部署：將不同頁面的 html 檔案，透過 [Netlify](https://www.netlify.com/) 這個讓人託管網站的網站來部署。
- 各部分的串接：透過 Github 來進行。

為何我要把原本看起來單純的「Wordpress.com 一站式託管」變成這麼複雜的流程？

<!-- more -->