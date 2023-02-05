---
title: 訂閱 Pin 起來
description: 訂閱 Pin 起來
date: 2023-02-04
path: subscribe/
template: subscribe.html
---

Hi ，若你有興趣持續收到這個網站的內容更新，可以透過 Email 或 RSS 訂閱：

---

## 透過 Email 訂閱

在這個網站裡有三大類的內容，你都可以透過 Email 訂閱。並且可以選擇要訂閱其中一種組合方案。

<div style="background: #f5f5f5;text-align: center">
<h3>基本版：只訂閱 Pin 起來電子報</h3>

<p style="padding: 1rem 4rem">Pin 起來電子報涵蓋我的各方面的選讀內容，以及當週特別想分享的事。我每週會固定發送一篇。
<br>我覺得電子報最適合所有人閱讀，也最適合透過 Email 收到，因此我把它放在基本版的方案。你可以透過 <a href="/newsletters/archive">電子報歸檔</a> 瀏覽過去的內容。
</p>
</div>

---

<br>
<div style="background: #f5f5f5;text-align: center">
<h3>進階版：基本版 ＋ Blog 更新</h3>
<p style="padding: 1rem 4rem">Blog 包含這個站上比較完整的文章，通常是介紹一個產品或服務、網站新功能上線的介紹、或者是比較完整的論述與工作流分享。發送的頻率並不固定，你可以透過 <a href="/archive">Blog 歸檔</a> 瀏覽過去的內容。
</p>
</div>

---

<br>
<div style="background: #f5f5f5;text-align: center">
<h3>完整版：進階版 ＋ Snapshots 更新</h3>

<p style="padding: 1rem 4rem">除了電子報與 Blog 之外，網站上還有一部分的內容屬於 Snapshots ，這些是我比較短的、不成熟的想法，可能是我對某件事的疑問，或者是我發現了、嘗試了什麼東西的心得。發送的頻率不固定，但應該是最常更新的內容，你可以透過 <a href="/snapshots/archive">Snapshots 歸檔</a> 瀏覽過去的內容。
</p>
</div>

---

<br>
<form
  action="https://buttondown.email/api/emails/embed-subscribe/pinchlime"
  method="post"
  target="popupwindow"
  onsubmit="window.open('https://buttondown.email/pinchlime', 'popupwindow')"
  class="embeddable-buttondown-form"
>
  <label for="email" style="text-align: center;font-size: 1.4rem">若要訂閱，請輸入你的 Email</label>
  <input
    type="email"
    name="email"
    placeholder="you@gmail.com"
    style="display: block; border-radius: 0.5rem; padding: 0.5rem 1rem; width: 100%; margin: 1rem auto; text-align: center; background-color: #ffffff;font-size:1.2rem "
  />
  <br>
  <label for="email" style="font-size: 1.4rem;">接著，請選擇訂閱方案</label>
  <ul>
        <input type="radio" id="Letter" name="tag" value="Letter">
        <label for="Letter">基本版：只訂閱 Pin 起來電子報</label>
        <br>
        <input type="radio" id="Blog" name="tag" value="Blog">
        <label for="Blog">進階版：基本版 ＋ Blog 更新</label>
        <br>
        <input type="radio" id="All" name="tag" value="All">
        <label for="All">完整版：進階版 ＋ Snapshots 更新</label>
  </ul>

  <input type="hidden" value="1" name="embed" />
  <input type="submit" value="點我訂閱" style="display: block; border-radius: 0.5rem; padding: 0.5rem; width: 25%; margin: 0 auto; text-align: center; background-color: #003C6D; color: #ffffff;font-size:1.2rem">

</form>
<br>

---

## 透過 RSS 訂閱

本站也有支援 RSS 訂閱，你可以[訂閱全站的 RSS](/atom.xml)，也可以針對你有興趣的子項目單獨訂閱。

例如，你可以透過下列連結，只訂閱特定主類別的內容：

- [Blog](/blog/atom.xml)
- [Newsletters](/newsletters/atom.xml)
- [Snapshots](/snapshots/atom.xml)

你也可以針對 [tags](/tags) 裡面的個別 tag 項目訂閱，你就點開這個標籤的連結，並且在後面加上 `/atom.xml` ，就可以單獨訂閱了。

例如，若你只對 Heptabase 這個標籤相關的更新有興趣，你就可以透過 <https://pinchlime.com/tags/heptabase/atom.xml> 單獨訂閱 Heptabase 這個 tag 的相關內容。 

---
