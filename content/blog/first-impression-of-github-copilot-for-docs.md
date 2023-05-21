---
title: Github Copilot for Docs 初體驗
date: 2023-05-21
description: 我覺得 Copilot for Docs 最令我最期待的地方是它能夠改善 ChatGPT 的 "halucination" 問題，也就是說，我期待 Copilot for Docs 是真的能夠針對特定的技術文件，根據其中的內容回答「正確的答案」，而不是像 ChatGPT 一樣，回答出一些看起來很像答案，但實際上可能繞遠路、有錯誤的內容。
path: blog/first-impression-of-github-copilot-for-docs
taxonomies:
  categories: 
    - Tools
  tags: 
    - Github Copilot
---


<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/github-copilot-for-docs_hQZo2U.webp" data-fancybox data-caption="github-copilot-for-docs">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/github-copilot-for-docs_hQZo2U.webp" loading="lazy" alt="github-copilot-for-docs" align="center" />
</a>
<br>

---

## 簡介
[Github Copilot for Docs](https://githubnext.com/projects/copilot-for-docs) 是 Github 在 2023 年 3 月推出的新產品，可以讓使用者透過對話的方式，讓 AI 根據不同的技術文件回答問題。

我在一推出的當下就申請了 [waitlist](https://githubnext.com/projects/copilot-for-docs) ，等了一個多月，終於在 5 月 21 日收到了邀請函，可以開始使用這個新產品了。

---

## 為何我對 Copilot for Docs 感興趣

我覺得 Copilot for Docs 最令我最期待的地方是它能夠改善 ChatGPT 的 "halucination" 問題，也就是說，我期待 Copilot for Docs 是真的能夠針對特定的技術文件，根據其中的內容回答「正確的答案」，而不是像 ChatGPT 一樣，回答出一些看起來很像答案，但實際上可能繞遠路、有錯誤的內容。

---

## 第一印象
登入 Github 帳號後第一眼看到的是幾組不同的 Docsets ，包含 Github, React, MDN, Typescript 等等，每組 Docset 都可以選擇「Start a new thread」，按下去後就會進入一個類似 Google 的搜尋介面，並且搭配三組可以調整回答內容的 bar ，分別對應到的是：

- 自己是程式新手還是老手
- 自己對這組 Docset 的熟悉程度
- 希望單純得到答案還是詳細的解釋

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/github-copilot-for-docs-2_fcy1b8.webp" data-fancybox data-caption="github-copilot-for-docs-2">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/github-copilot-for-docs-2_fcy1b8.webp" loading="lazy" alt="github-copilot-for-docs-2" align="center" />
</a>
<br>

點擊搜尋框後，會直接顯示預設的幾組常見問題，當然也可以自己輸入搜尋。這時候就可以看到 Copilot 的 AI 回答了，整體的體驗就像是 ChatGPT 或 Bing AI 一樣，並且回答後還會出現「You might also want to know」的區塊，顯示其他可能自己有興趣的問題。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/github-copilot-for-docs-3_dGKqBd.webp" data-fancybox data-caption="github-copilot-for-docs-3">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/github-copilot-for-docs-3_dGKqBd.webp" loading="lazy" alt="github-copilot-for-docs-3" align="center" />
</a>
<br>

我因為不是工程師，對這些技術文件不是那麼熟悉，因此不太確定目前 Copilot for Docs 的回答水準如何。另外，目前也還沒辦法讓 Copilot for Docs 存取預設 Docsets 以外的技術文件，所以也沒辦法問他我比較熟悉的技術文件，例如我架站的 [Zola 系統](https://www.getzola.org/documentation/getting-started/overview/)，或是關於其他任何專案 Repo 的問題。

## 未來的發展

不過這些看起來都是未來有機會達到的，官網的 "Future directions" 也有提到未來會發展的幾個面向，包含：

- Include other content

    能夠納入更多 Github 上的 issues 與相關的討論。

- Include `code`

    能夠基於程式碼來回答問題，而非僅僅基於為了解釋程式碼而製作的技術文件。若這點能成功，甚至能反過來協助開發者撰寫技術文件。

- Combine information across libraries

    官方舉的例子是，針對某個問題，能夠跨越不同的 Libraries 如 Tailwind CSS 與 Next.js 來收集答案並回答問題。

- Growing a trusted knowledgebase

    能夠讓使用者 Star threads 以及 highlight 特定段落、寫筆記。讓這個系統能直接擔任用戶的知識庫。

最終官方想達到的願景是，讓開發者更容易地創造及維護文件，也讓使用者更容易地找到不同文件的答案。

期待繼續 Copilot for Docs 能繼續納入不同的 Docsets 與開發更多功能！