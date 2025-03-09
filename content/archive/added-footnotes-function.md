---
title: 部落格新增了 Footnotes 註腳的功能
date: 2022-04-30
updated: 2022-04-30
description: 最符合我期待的 footnotes 實踐方式，是讓比較與原文段落無關的補充，能夠出現在一個特定的地方，讀者可以「想看就找得到，不想看也不用看」。
path: blog/added-footnotes-function
---

昨天在 Zola 的官方討論區看到[有人在提問某個程式碼的問題](https://zola.discourse.group/t/getting-markdown-without-paragraph/1282)，但發現他那段程式碼的目的是想要自訂 footnotes ，也就是註腳的功能，這就讓我很感興趣。

雖然我一開始完全看不懂他的 code ，但還是留言詢問了一下可否分享他寫的完整代碼給我，結果他真的很好心地分享，還寫了一段說明。我簡單照著做之後，就真的實現了這個功能，覺得這對我來說是個很有意義的功能，因此想簡單分享（搬運）一下他的做法。

<!-- more -->
---

## Footnotes 是什麼？

Footnotes 簡單來說，就像這樣{{ ftnt_refs( idxs=[1]) }}。

這種東西通常在學術文件或研究報告裡面出現，主要功能用於補充解釋本文{{ ftnt_refs( idxs=[2]) }}，或者是標註參考資料的來源。而許多 pdf 或者網頁也都可以點選註腳後跳到特定段落。我對註腳的理解是，他是某種需要額外附加的功能，例如以前在 Wordpress 裡面寫的時候，就可以在那個相當複雜的古騰堡編輯器裡面，找到「註腳」這樣的元件用來插入段落。

因此在剛架好這個部落格時，我也曾嘗試透過 \[^1] 這種 markdown 格式比較常見的的方式來設定註腳，嘗試後是可以製造出註腳的效果，但卻會有樣式跑掉的問題，改了一下 CSS 後發現不太知道怎麼用，就放棄了。而 Zola 的官方說明文件裡面也沒有相關說明，對於 Zola 這種相當簡單的靜態網站產生器來說，官方文件裡面沒有的功能，我都先當成沒有。

但這次簡單測試網友 ghlecl 的做法後，發現他的做法非常簡單，而且完全可以用！

---

## Footnotes 功能是怎麼實現在 Zola 的？

如果有看上面開頭那串原始連結，就可以看到網友 ghlecl 詳盡的說明，我在這邊嘗試用更簡單的方式介紹一下：

一、透過 "[Shortcodes](https://www.getzola.org/documentation/content/shortcodes/)" 這個 Zola 內建的功能 ，建立了兩個 shortcodes ，一個叫做 ftnt_refs.html (footnote references)，一個叫做 ftnt.html (footnote)。

二、ftnt.refs.html 提供的是「註腳編號小標」的功能，只要在任何文章想要放註腳編號的段落，放上 `{{ ftnt_refs( idxs=[n]) }}` 這個 shortcode （裡面 \[n] 的數字 可以代換成想要的數字），他就會在該文字的後方右上角，出現設定的數字，並且可以透過超連結連到「ftnt.html」這個 shortcode 裡面同數字的註腳內容。

三、ftnt.html 提供的是設定「註腳具體內容」的功能，只要在文章的任何段落，想要放置註腳內容的地方，放上下面這段 shortcode ，就可以在該段落創造一個「註腳段落」，並且產生一個「跳轉」的超連結，讓人在看完註腳內容後，可以跳轉回原段落。

```rust
{% ftnt( idx = n ) %}
這邊放入註腳 n 想要放的註腳內容
{% end %}
```

---

## 具體的 Shortcodes 是怎麼寫的？

ftnt_refs.html 的代碼是：

```rust
{%- set arr_len = idxs | length -%}
{%- set last_idx = arr_len - 1 -%}
{%- for i in range(end=arr_len) -%}
{%- set idx = idxs | nth( n=i ) -%}
<sup {%- if not no_back_ref %} id="ftntref:{{- idx -}}"{%- endif -%}><a href="#ftnt:{{- idx -}}">{{- idx -}}</a>{%- if i != last_idx -%}, {% endif -%}</sup>
{%- endfor -%}
```

ftnt.html 的代碼是：

```rust
{%- set idx_str = idx | as_str -%}
<p id="ftnt:{{- idx_str -}}"><sup>[{{- idx_str -}}]</sup>&nbsp;{{- body | markdown( inline = true ) | safe -}}
{%- if not no_back_ref -%}
&nbsp;<a href="#ftntref:{{- idx_str -}}">&#8617;&#65038;</a>
{%- endif -%}
</p>
```

坦白說，我還沒有完全理解這裡面在寫什麼，只知道這兩段代碼有互相使用對方，因此串連在一起。但我還不太知道可以怎麼改，大致上只知道可以改超連結的內容跟文字，以及改這兩個 shortcodes 的名稱（裡面對應的段落也要跟著改）。

如果未來懂更多，我應該會改成更符合自己想像的樣子。

---

## 為何想要有 Footnote 功能？

我曾在 [Eugene Wei 的網站](https://www.eugenewei.com/) 裡面看到我想像中的 footnotes 功能該有的樣子，點進去裡面隨意一篇文章都可以看到， footnotes 是直接出現在原文的右側，而且是直接與該段落平行。而若螢幕較小，也會變成「點擊後出現」。我覺得這是最符合我期待的 footnotes 實踐方式，讓比較與原文段落無關的補充，能夠出現在一個特定的地方，讀者可以「想看就找得到，不想看也不用看」。

不過目前透過這兩段 shortcodes 能夠達成基本的 footnotes 功能，我也很滿意了，而且這樣的功能完全不需要安裝任何插件，相關內容是在 「build」 網站的過程中就產生了，可以說是很符合靜態網站理念的一種實作方式。

---

{% ftnt( idx = 1 ) %}
註腳的具體內容可以放在文章最下面，並且可以透過超連結和返回的按鈕跳轉。
{% end %}

{% ftnt( idx = 2 ) %}
我的理解是，這個解釋如果放在本文裡面會讓本文顯得太繁瑣，但又是一個最好可以提供，或者說，作者很想講的補充，所以就會放一個註腳，把比較完整的話放在註腳裡面，而讓本文維持語意的簡潔與完整。
{% end %}