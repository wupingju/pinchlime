---
title: My Stream
description: 我在這裡放各種即時的想法、靈感、以及看到的、讀到的內容。
path: stream/2023/
date: 2023-02-23
updated: 2023-02-24
template: stream.html
---

## 2023


### February

{% fleet(num="8",time="Feb 27 14:51",year="2023") %}
今天從 Fox 那邊得知了 GPT 模型裡面的 <a href="https://platform.openai.com/docs/api-reference/completions/create#completions/create-temperature">temperature</a> 概念，之前偶爾都有看到，但一直沒去深入理解。目前我的理解是， temperature 可以控制產生結果的多樣性與隨機性，這個值可以設定在 0-2 ， 0 代表最小的隨機性， 2 則是最大。
<br>
另一個影響多樣性的變數是 top_p ，目前我的理解是， top_p 設定越高（ 0-1 ），生成的文本會「更可信」，但同時會降低文本的「多樣性」。
<br>
我自己目前還沒有找到適合的問題來測試 top_p ，而 temperature 倒是蠻容易測試的，很有趣！
{% end %}


{% fleet(num="7",time="Feb 25 15:04",year="2023") %}
剛剛做了一個簡單的 Keyboard Maestro macro ，可以快速建立新的 stream 內容，如截圖：
<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/quick-add-stream_EvcjNC.gif" loading="lazy" alt="quick-add-stream" align=center /><br>
我只要輸入編號，就會自動幫我帶入當下的時間、年份等資訊。這樣 PO 東西的速度就可以更快了！
{% end %}


{% fleet(num="6",time="Feb 25 10:05",year="2023") %}
剛才調整了一下站內不同頁面的側邊欄。<br>原先的我太貪心，想要盡量在每一頁都塞給讀者更多的可能性。但這幾天思考以及重新閱讀自己的網站後，感覺閱讀動線可能更重要，因此我做了一些調整。<br>
由於最上方已經有個導航列，讀者可以很容易連結到三大主題頁面，所以我把各個主題的側邊欄都簡化，例如，Blog 主頁與相關子頁的側邊欄就只留下 Blog 的內容。<br>調整過後各個頁面感覺更乾淨清爽一點了。
{% end %}


{% fleet(num="5",time="Feb 25 00:39",year="2023") %}
用了兩天多零碎的時間，總算差不多把這個頁面都調整成我想要的樣子了。<br>
目前的感覺是，有一個這樣子可以 murmur 的地方非常讚，它比站上的 Snapshots 更輕便、更私密一些，也因此更能構承載一些零散、破碎的內容，無論是單純放一個連結，或者是丟一段 quote 之類的，都很適合。<br>有一個能夠自由增添內容的網站真的好棒！
{% end %}

{% fleet(num="4",time="Feb 24 23:45",year="2023") %}
在 Twitter 上面分享了<a href="https://twitter.com/WuPingJu/status/1629136041985847298">一串關於 Heptabase AI Assistant 的想法</a>。<br>我感覺我最期待、想要的，應該不只是一個「智能資料庫」，而是一個能夠與我持續對話，能以我累積的思考為基礎，進而能一起討論一些問題、產生新想法的 AI 。<br>
感覺好像很快就可以看到這種東西的雛形了！
{% end %}

{% fleet(num="3",time="Feb 24 09:04",year="2023") %}
昨晚發現了 <a href="https://phind.com/">phind.com</a> 這個感覺也不錯的 AI 搜尋引擎，測試了一下效果蠻好的，呈現 References 的方式我也更喜歡，值得後續繼續研究。
{% end %}

{% fleet_q(num="2",time="Feb 24 08:56",year="2023",source_name="Linus Lee - About the stream",link="https://stream.thesephist.com/about/") %}
<strong>Why not twitter?</strong>
<br>
Lastly, Twitter is great for "in the moment" discussion in public, but it's not so great as a reference you can link to from the future, and as a historical record of my thinking and work. I wanted a place more purpose-built, more focused, and more permanent for my less permanent thoughts and updates.
{% end %}

{% fleet(num="1",time="Feb 23 23:04",year="2023") %}
Hello World !
{% end %}