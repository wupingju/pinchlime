---
title: 訂閱 Pin 起來
description: 訂閱 Pin 起來
date: 2023-02-04
path: subscribe/
template: subscribe.html
draft: true
---


## 透過 Email 訂閱

Hi ，若你有興趣持續收到這個網站的內容更新，可以透過 Email 或 RSS 訂閱：

<br>
<form
  action="https://buttondown.email/api/emails/embed-subscribe/pinchlime"
  method="post"
  target="popupwindow"
  onsubmit="window.open('https://buttondown.email/pinchlime', 'popupwindow')"
  class="embeddable-buttondown-form"
>
  <label for="email" style="text-align: center;font-size: 1.2rem">若要訂閱，請輸入你的 Email</label>
  <input
    type="email"
    name="email"
    placeholder="you@gmail.com"
    style="display: block; border-radius: 0.5rem; padding: 0.5rem 1rem; width: 100%; margin: 1rem auto; text-align: center; background-color: #ffffff;font-size:1.2rem "
  />
  <br>
  <label for="email" style="font-size: 1.2rem;">接著，請勾選訂閱方案</label>
  <ul>
        <input type="radio" id="Letter" name="tag" value="Letter">
        <label for="Letter">訂閱 Pin 起來電子報</label>
  </ul>

  <input type="hidden" value="1" name="embed" />
  <input type="submit" value="點我訂閱" style="display: block; border-radius: 0.5rem; padding: 0.5rem; width: 25%; margin: 0 auto; text-align: center; background-color: #003C6D; color: #ffffff;font-size:1.2rem">
</form>
<br>

在按下訂閱按鈕後，你應該會在信箱收到一封確認信，請你點擊裡面的確認連結，才算是完成訂閱。若你沒有收到確認信，那麼肯定是哪邊出錯了，此時歡迎你直接寄信到 <pj@pinchlime.com> 給我，由我為你手動訂閱。

若你已經是訂閱用戶，但想要更改訂閱的方案，很抱歉，目前沒有自己調整的方式（連退訂再重新訂閱也不行），所以請你直接寄信給我，我很樂意為你調整！

<br>

---

## 透過 RSS 訂閱

本站也有支援 RSS 訂閱，你可以[訂閱全站的 RSS](/atom.xml)，也可以針對你有興趣的子項目單獨訂閱。

例如，你可以透過下列連結，只訂閱特定主類別的內容：

- [Blog](/blog/atom.xml)
- [Newsletters](/newsletters/atom.xml)

你也可以針對 [tags](/tags) 裡面的個別 tag 項目訂閱，你就點開這個標籤的連結，並且在後面加上 `/atom.xml` ，就可以單獨訂閱了。

例如，若你只對 Heptabase 這個標籤相關的更新有興趣，你就可以透過 <https://pinchlime.com/tags/heptabase/atom.xml> 單獨訂閱 Heptabase 這個 tag 的相關內容。 

---
