---
title: Make sense of complex topics with Alan Chan, co-founder of Heptabase
date: 2023-12-16
updated: 2023-12-16
description: 使用 Heptabase 的「頓悟時刻」是，當你逐漸從愈來愈多的地方，累積愈來愈多的卡片，你會發現你在白板上面建立理解的過程會非常流暢，很容易就進入思考的心流，幾個小時後，你會發現你已經針對這個主題建立了屬於你的獨特理解。你會知道接下來你該閱讀什麼、你該如何將新學到的知識與你既有的知識結合，並且你也會知道這些屬於你的理解，將永遠透過視覺化的方式儲存在這裡。
path: library/translations/alan-chan-heptabase-featured-tool
draft: true
extra:
  page_type: archive
  image: https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/heptabase-interview-1_rFJlXH.webp
---

- [Original link](https://nesslabs.com/heptabase-featured-tool)
- Original post date: 2023.12.08


Welcome to this edition of our Tools for Thought series, where we interview founders on a mission to help us make the most of our mind. Alan Chan is the co-founder of Heptabase,  a visual note-taking tool that helps you learn complex topics.

歡迎來到我們的「思考工具」（Tools for Thought）系列的這一期，我們在這裡採訪那些致力於幫助我們充分利用心智的創辦人。 Alan Chan 是 Heptabase 的共同創辦人，這是一款視覺化筆記工具，可以幫助你學習複雜的主題。


In this interview, we talked about the inherent dilemma of intelligent product design, how to create a co-evolution system to address this dilemma, the five parts of the knowledge lifecycle, how to solve interoperability across use cases with meta-apps, how to support both individual and collective knowledge creation, and much more. Enjoy the read!

在這次採訪中，我們討論了產品設計上兩難困境，以及如何創建一個共同進化的系統來解決這個困境。也討論了知識生命週期的五個階段、如何透過 “meta-apps” 的概念解決橫跨不同使用情境的互相串聯操作問題，以及 Heptabase 是如何幫助個人和集體的知識創造等等。祝你閱讀愉快！

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/heptabase-interview-1_rFJlXH.webp" data-fancybox data-caption="heptabase-interview-1">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/heptabase-interview-1_rFJlXH.webp" loading="lazy" alt="heptabase-interview-1" align="center" />
</a>

---

**Hi Alan, thanks so much for agreeing to this interview. Let’s start with your vision. You want to build a truly universal Open Hyperdocument System. What does that mean?**

嗨，Alan，謝謝你同意這次採訪。讓我們從你的願景開始談起。你想要建立一個真正普遍的「開放超文本系統」（Open Hyperdocument System, OHS）。這是什麼意思？

Our vision at Heptabase is to create a world where anyone can effectively establish a deep understanding of anything. And this universal Open Hyperdocument System (OHS) is a means to that vision. It’s hard to explain what OHS is without context, so I’d like to first share the story of how I encountered this concept.

Heptabase 的願景是創造人們可以有效地對任何事物建立深度理解的世界。而這個「開放超文本系統」（OHS）就是實現我們願景的手段之一。OHS 這個概念有點難直接在去脈絡的狀況下介紹，所以我想先分享我是如何接觸到這個概念的故事。

So, one of the most enjoyable things in my life is learning things that are interesting to me. In middle school, that thing was math. In high school, it’s physics. That’s why, when I went to college, I double majored in Physics and Mathematics.

在我人生中最愉快的事情之一，就是學習那些我感興趣的事物。在國中時是數學，到了高中則是物理。這也是我上大學時選擇雙主修物理和數學的原因。

One thing that I really appreciate in these disciplines is how one concept in Mathematics can be applied to so many different areas of Physics, and one theory of Physics can explain so many phenomena in the world. There were many moments when I started to understand how all these things are interconnected and how things are simple yet complex at the same time. That’s what I mean by “deep understanding.”

我欣賞這些學科的其中一點是，數學裡的一個概念可以應用到物理的許多不同領域，而物理的一個理論又可以解釋世界上的許多現象。當我開始理解這些事是如何相互連接的，以及他們可以同時這麼簡單又這麼複雜時，我得到了很多啟發。這是我想表達的「深度理解」。

In my sophomore year, I wanted to spend more time exploring other disciplines such as history, psychology, computer science, business, and many others. I had this fundamental desire to make sense of everything in the world, and I wanted to try my best to read as much as I could and see how far I could get.

在大二那年，我想花更多時間探索其他學科，例如歷史、心理學、電腦科學、商業等等。我有一種很深層的渴望想要理解世界上的一切。我也希望盡可能地閱讀多一點，看看我能走多遠。

So, I dropped out of college and bought a lot of books to read and started building my own knowledge system to manage all the reading notes I wrote. I used Evernote for a while and switched to Notion a bit later, and I immediately noticed that Notion has many interesting and powerful capabilities.

於是，我退學了，買了很多書來閱讀，並開始構建自己的知識系統來管理所有我寫的閱讀筆記。我曾使用 Evernote 一段時間，後來轉用 Notion，我馬上發現 Notion 有許多有趣且強大的功能。

I looked into Notion’s website and found these big names in HCI: Douglas Engelbart, Alan Kay, Ted Nelson, Bret Victor, etc. I read and watched everything on Bret Victor’s website. I read most of the things on Doug Engelbart Institute’s website, including the Augment Human Intellect report. I read a lot of Alan Kay’s essays, Ted Nelson’s Literary Machines, and Seymour Papert’s Mindstorms. And then I read this mind-blowing book called The Dream Machine, which I still think is the best book about computer history.

我查看了 Notion 的網站，發現了他們提到一些人機交互（HCI）領域的大名鼎鼎的人物，例如 Douglas Engelbart、Alan Kay、Ted Nelson、Bret Victor 等等。我接著讀了看了 Bret Victor 網站上的所有內容。我讀了 Doug Engelbart Institute 網站上的大部分內容，包括《*Augment Human Intellect*》報告。我讀了很多 Alan Kay 的文章，Ted Nelson 的《*Literary Machines*》，以及Seymour Papert的《*Mindstorms*》。然後我讀了一本令人震驚的書《*The Dream Machine*》，我認為這是關於電腦發展史上的最佳著作。

After reading all this stuff, one thing that inspired me the most was how these computer pioneers and thinkers think about how humans and computers can work together to solve complex problems.

讀完這些東西後，最讓我感到啟發的事情，是知道這些電腦科學先驅和思想家，都是怎麼思考人類和電腦如何共同合作解決複雜問題的。

For example, Engelbart has this approach of using computers to improve the collective IQ of a group of people. What he’s suggesting was building a new kind of tool called Dynamic Knowledge Repositories (DKRs) that can integrate and update the latest knowledge from a group of people, and all the DKRs in the world will be powered by the same Open Hyperdocument System (OHS).

例如，Engelbart 提出了使用電腦提高一群人集體智商的方法。他的建議是建立一種新型的工具，叫做動態知識庫（Dynamic Knowledge Repositories，DKRs），可以整合與更新一群人的最新知識，而世界上所有的 DKRs 都將由同一個開放超文本系統（OHS）支持。

That caught my attention, so I looked into the specs of OHS, and then I noticed that its capabilities look so much like Notion. Then I realized what Notion did was they implemented many of OHS’s specs and wrapped it with a modern UI and sold it as a team collaboration product. But fundamentally, it’s very similar to Engelbart’s OHS specs.

這引起了我的注意，所以我研究了 OHS 的功能描述，我注意到它提到的能力跟 Notion 非常相似。我因此意識到，Notion 在做的事情就是把 OHS 包裝在一個更現代化的使用者介面，並且增加了團隊協作的功能。但從根本上來看，它與 Engelbart 提出的 OHS 非常相似。

So, the next thing that came to my mind was: why implement an old spec from the late 20th century? How will Engelbart design OHS if he lives in the 21st century and is familiar with all the computer technologies we have now?

接下來我想到的是：為什麼要導入 20 世紀末提出的架構呢？如果 Engelbart 生活在 21 世紀，並熟悉我們現在擁有的所有電腦技術，他將如何設計 OHS ？

Engelbart’s intention was to augment human collective intelligence, and I think modern digital collaborative workspaces are still far from that. The original OHS system doesn’t seem to address much about the process of how humans discover and distill knowledge and foster deep understanding on different topics, and which part of the process happens independently and which part happens collectively.

Engelbart 的目的是增強人類的集體智力，我認為現代的數位協作空間離這個目標還有一段距離。原始的 OHS 系統似乎不太關注人們如何發現和提煉知識、在不同主題上建立深度理解的過程，以及這個過程的哪些部分是獨立進行的，哪些部分是集體進行的。

Thinking about this was intellectually stimulating, and this question had been on my mind for a few years. And that was the time the idea of Heptabase started to take shape. I wanted to design and create a new Open Hyperdocument System in the 21st century that serves as the foundation of all modern knowledge repositories.

思考這些事情為我帶來很多靈感與想法，這個問題在我腦中不斷盤旋了幾年，這時，Heptabase 的想法開始成形。我希望在 21 世紀設計並建立一個全新的開放超文本系統，作為所有現代知識庫的基礎。

Everything built on top of this system should have the inherent capabilities to empower people to effectively create a deep understanding of anything they’re learning and researching.

建立在這個系統之上的一切，都應該能夠賦予人們能力，讓人們更有效率地針對他們正在學習和研究的任何事物，建立深度的理解。

---

**What a journey. Why do you think this vision is so challenging to bring to life?**

你覺得實現這個願景具有哪些挑戰？

I think the most challenging part is that you’ll face this dilemma between building a system that is general enough to become the foundation for many things, and building a product that is useful enough for end-users to solve their problems.

我認為最具挑戰的地方在於，你會面臨一個兩難的困境，一方面你想要建立一個足夠通用的系統來成為許多事物的基礎，但另一方面你又要建構一個對許多用戶來說有用的產品，解決他們特定的問題。

One thing I’ve seen many companies do is to begin by considering what a perfect system would look like and what capabilities it should have. They write clear specs for that system and then build everything based on these specs. The biggest challenge of this approach is that you end up with a Swiss knife that has a wide range of capabilities, and while it might be able to do many things, it can be intimidating for end-users.

我看到許多公司會做的事情是，先考慮一個完美個系統應該是什麼樣子，以及它應該具備哪些能力。接著他們為這個系統撰寫清楚的規格，然後基於這些規格建構一切。這種方法的最大挑戰是，你最終得到的是一個功能廣泛的瑞士軍刀，儘管它可能可以做到很多事情，但可能會複雜到嚇跑一般用戶。

Most people just want to find a solution that solves their problem out of the box. Most people don’t care about all the concepts and capabilities you introduced in your system. And no matter how good your technology is, if not many people use it, you’ll end up going nowhere. So, these companies usually have to spend a lot of time working on improving usability, simplifying their product, and understanding their users’ needs.

大多數的人只想要找到一個能夠直接解決他們特定問題的方案，他們不太關心你在系統裡面導入的各種概念與功能，即使你的技術再好，如果沒有用戶使用你的系統，你最終還是無路可走。所以這類的公司通常需要花費大量的時間來提升產品的易用性，努力簡化產品，並且了解用戶的需求。

Personally, I prefer the approach of fostering a “co-evolution” process between the design of the system and the users’ jobs to be done. This is another important concept from Engelbart, in which he used to describe the back-and-forth process of how humans evolve with the tools they use and how tools evolve with the humans using them.

我個人則是更傾向於另一種作法，也就是促進系統設計與用戶需求之間的「共同進化」過程。這是 Engelbart 提出的另一個重要概念，他用它來描述人類如何與他們使用的工具共同進化，以及工具如何與使用它們的人共同進化的往返過程。

One great example of such a process is Bret Victor’s project called Dynamicland, which I think of as an environment where people can explore and understand systems and have data-driven conversations through authoring dynamic visual representations of data. The system includes a lot of paper cards that contain programs, and a protocol that enables people to make claims and wishes on these cards to facilitate communication across programs.

另一個很好的例子是 Bret Victor 的專案 Dynamicland，我認為它是一個人們可以自由探索和理解系統的環境，在這之中還能夠透過創造動態的視覺化資料，來進行資料驅動的對話。這個系統裡有著許多能編寫程式的紙卡，以及一套能讓用戶自己在卡片上提出聲明與願望的協議，這些都能夠促進不同程式之間的互相溝通。

What fascinates me is how they built the system—they invited many people with different backgrounds to come to Dynamicland and observe how these people interact with Dynamicland, and then use such learning to evolve the design and the protocol of the entire system.

讓我著迷的是他們如何構建系統——他們邀請了許多不同背景的人來到 Dynamicland，觀察這些人如何與 Dynamicland 互動，然後利用這些觀察後的成果來演進整個系統的設計以及打造更好的協議。

So, the biggest difference between these two approaches is how much you believe you know and how much you believe you don’t know. If you think you know everything, then you design the entire system from the beginning, and the risk is that you might be wrong about many things.

我想上述這兩種作法最大的差異在於，你知道自己知道與不知道多少事情。如果你認為你自己已經知道一切，那你可能會在一開始就設計一個完整的系統，但這樣做的風險是你可能會在許多事情上面出錯。

If you think you know just a few things, then you start by designing a system that handles these few things well, put it out and see how people use it, gain more knowledge on how people work, and use this knowledge to evolve your system to accommodate more capabilities while taking care of usability.

如果你認為你只知道一些事，那麼你可以從這些事情開始，建立一個系統把這些事情處理好，把它推出給別人用用看，得到更多關於別人怎麼用它的知識，再利用這些知識繼續讓系統進化，以在承載更多功能的前提下能夠兼顧易用性。

The most challenging part of this approach is to resist the urge to try to design a perfect system from the start and admit that there are still things you don’t know. Once you admit that, you’ll start thinking about how you can acquire those insights from your users.

這種作法最困難的地方在於，你必須要抵抗從一開始就設計一個完美系統的衝動，並且承認有許多事情你還不知道。當你承認了這件事，你就會開始思考如何從你的用戶身上獲得這些洞察。

---

**So how is Heptabase approaching this?**

Heptabase 是如何進行這項工作的？

When building Heptabase, there are some mental models and guiding principles that I have been using since the very beginning.

從開始打造 Heptabase 以來，我就遵循了一些心智模型與指導原則。

The first mental model is called “The Knowledge Lifecycle”, which consists of five parts: exploring, collecting, thinking, creating, and sharing. We want to ensure that knowledge can be seamlessly passed from one part to another, and we want to ensure that for each part of the lifecycle so we can design and build a great solution that addresses the problems people face really well. In the end, it’s all about whether we can create this synergy across all five parts of the cycle. We have been working on the “thinking” part since 2021, and then the “collecting” and “creating” parts since 2023, and will work on the “sharing” and “exploring” parts in 2024.

第一個心智模型是「知識的生命週期」（The Knowledge Lifecycle），它包含五個階段：探索、收集、思考、創作和分享。

我們希望確保知識可以從一個階段順暢地過渡到另一個階段，並且確保能夠為每個部分，都設計和打造出非常好的解決方案，來解決人們在這些階段會遇到的問題，最終則是希望這五個階段能夠互相創造出協同的效應。

從 2021 年以來我們一直致力於打造「思考」這個階段的體驗，接著是從 2023 年開始的「收集」與「創造」，而在 2024 年我們將開始致力於「分享」以及「探索」階段。

The second mental model is system layering. The way I abstract the system we’re building is that there will be multiple independent layers, each focusing on one unique job. For example, a contextual layer for preserving thinking context, a descriptive layer for managing categories and adding properties, an annotation layer for annotating static files, an integration layer for creating aliases for third-party data, a communication layer for enabling a group of people to construct a deep understanding of complex topics, and an application layer for users to build card-based software on top of our system in the future, and so on.

第二個心智模型是系統分層（system layering），我把我們正在建構的系統分成幾個互相獨立的抽象層，每一層都專注於一件獨立的事情。例如，有一個專注於保存思考脈絡的 Contextual Layer；有一個用於管理類別並增加屬性的 Descriptive Layer；有一個讓你註解靜態文件的 Annotation Layer；有一個為第三方應用和資料準備的 Integration Layer；有一個讓一群人能夠共同對複雜主題建立深度理解的 Communication Layer，以及一個讓用戶在未來能夠基於卡片，建構各種應用程式的 Application Layer。

So when many users request a feature, the first thing I think about is which part of the knowledge lifecycle it belongs to and how we can design and integrate this feature with our existing solution in this part of the lifecycle.

因此，當用戶們請求某個功能時，我首先會思考這個功能屬於知識生命週期的哪個階段，以及我們可以如何將這個功能與我們既有的解決方案設計整合在一起。

The second thing I think about is which abstraction layer this feature belongs to, so I can have a clear picture of how the system design is evolving. On the other hand, sometimes we reach a point where we believe we have done great work in building one abstraction layer and want to shift our focus to building the capability of the next abstraction layer. I will then consider which part of the knowledge lifecycle this capability can be useful for and how it can solve real-world users’ problems. The process of switching between these two mental models while building the product is what I mean by “co-evolution.”

接著我會思考的是這個功能屬於哪個抽象層，這樣我就能清楚地看到系統設計是如何演進的。另一方面，有時我們會覺得，我們現在已經在某個抽象層上面做得很好了，接著我們就會把開發的重心轉移到另一個抽象層上。這時我也會考慮這個功能是否可以在哪個知識生命週期的階段派上用場。簡單來說，打造產品時在這兩個模型之間切換的過程，就是我前面提到的「共同進化」。

And then, in execution, there are two major guiding principles. The most important principle in our company is that we want to ensure that everything we’re building is aligned with our ultimate goal of helping people acquire and establish a deep understanding of the things they care about. We’re very conscious of not getting distracted by other purposes. The second principle is that we want the product to be as friendly and intuitive as possible. Our target users should be able to get into the flow of thinking as soon as they open the product.

而在實際執行上有兩個主要的指導原則。第一個最重要的是，我們要確保我們建構的一切都與我們的最終目標對齊一致，也就是幫助人們針對他們關心的事情建立與獲得深度理解。我們非常小心不要被其他的目標分散注意力。

第二個原則是，我們希望打造出來的產品能夠使用者友善與直觀，我們期待用戶可以一打開產品就馬上進入思考的心流。

---

**It’s great to hear that you have solid foundational mental models underlying the product vision. Now, tell us: how does Heptabase actually work?**

很高興聽到你們的產品願景背後有著堅實的基礎心智模型。現在請告訴我們：Heptabase 實際上是如何運作的？

At this moment, you can think of Heptabase as a visual note-taking tool that helps you learn and research complex topics. We currently only focus on the individual use case because we want to make sure everyone is first equipped with the best tool for independent thinking before we build the communication layer for collective thinking.

目前，你可以將 Heptabase 想成一個視覺化的筆記工具，可以用來幫助你學習與研究複雜的主題。我們目前專注於個人的使用情境，因為我們希望在我們建立能夠進行集體思考的 Communication Layer 前，每個人都可以得到最好的獨立思考工具。

So, the current product focuses on solving the problem in the collecting → thinking → creating parts of the knowledge lifecycle. Most users use Heptabase to digest complex literature, integrating this knowledge with their own ideas to create high-quality outcomes.

因此，目前的產品專注於解決知識生命週期中的收集 → 思考 → 創造這幾個階段的問題。我們大多數的用戶會使用 Heptabase 來消化複雜的文獻，並且將消化後的知識與自己的想法整合起來，創造出高品質的成果。

Like I mentioned previously, in 2021-2022, we primarily focused on the “thinking” part. During this time, we built a whiteboard specifically designed for empowering complex knowledge work, rather than just drawing and brainstorming.

在 2021-2022 年，我們主要專注於「思考」的階段。在這段時間，我們打造了專門為了促成複雜知識工作而設計的白板。

Heptabase’s whiteboard is designed with two insights. The first one is obvious: humans think much better when they think visually. The second one is less obvious: to gain a deep understanding on a topic through visual thinking, you need to first atomize the concept you learned. Real deep understanding doesn’t come from the “relationship between two books” but from the “relationship between all the concepts in these two books.”

Heptabase 的白板不是主打讓你繪圖或進行創意發想，而是基於兩個洞察設計的。第一個洞察比較明顯：當人們透過視覺思考的時候，可以思考地更清晰。第二個洞察比較沒那麼明顯：如果要透過視覺思考建立深度理解，你需要先將你學到的概念原子化。
我們認為，真正的深度理解並不會來自「兩本書之間的關係」，而是來自於「這兩本書之中所有概念彼此之間的關係」。

That’s why in Heptabase’s whiteboard, you can easily break down lengthy card notes into atomic concept notes. I believe this process of “extracting concepts” is the real foundation of deep understanding.

基於這些洞察，在 Heptabase 的白板裡面，你可以非常輕鬆地把很長的筆記卡片拆解成比較短的原子概念卡片。我相信這個「提煉概念」的過程是建立深度理解的基礎。

Once you break down these concepts, you can use sections, mind maps, nested whiteboards, and many other features we have built to make sense of them and even reuse a concept across whiteboards. If you want to learn more about how this process works with real-world examples, I recommend checking out an article I wrote titled The Best Way to Acquire Knowledge from Readings.

一旦你拆解出這些原子概念，你就可以使用 Heptabase 裡面的 Sections 區塊、心智圖、層狀白板、以及我們建構的其他功能來更加深理解，並且把這些概念重複使用在不同的白板上面。

如果你想要更了解這方面的運作流程以及實際範例，我推薦你參考我曾寫過的文章[《The Best Way to Acquire Knowledge from Readings》](https://wiki.heptabase.com/the-best-way-to-acquire-knowledge-from-readings)。

In 2023, we allocated more resources to improving the “collecting” part of the knowledge lifecycle. Apart from the obvious tasks, such as launching mobile apps and web apps on all platforms, a significant amount of work here focuses on helping you collect knowledge from different types of sources. For example, you can bring PDFs, audios, videos, images, and Readwise highlights into Heptabase. For PDFs, you can perform the exact same process of “extracting concepts” by creating highlights and annotations and dragging them onto the whiteboards.

在 2023 年，我們投入了更多開發資源來改善知識生命週期中的「收集」階段，例如開發 Task App 、推出手機版本以及網頁版本。除了這些明顯的任務以外，我們也讓用戶可以更容易透過不同類型的素材來收集知識，例如你可以把 PDF 、影片、音檔、圖片、或者是 Readwise 的畫線內容全部都導入 Heptabase ，你可以在 Heptabase 裡面幫 PDF 畫線、註解，並且把這些內容拖到白板裡面，進行完全相同的「提煉概念」流程。

In the next few months, we’re going to let you extract concepts from audios, videos, and images. If you open a browser side by side with Heptabase, you can also drag contents from the web to Heptabase’s whiteboard and turn them into cards. Essentially, we want to ensure that you can extract concepts from any type of knowledge sources and build your library of concept cards, so you can reuse and apply all the knowledge you’ve learned anytime you want.

在接下來的幾個月內，我們將讓你更容易從影片、音檔與圖片中提煉概念。如果你在瀏覽器開啟一個網頁並且放在 Heptabase 視窗旁邊，你會發現你可以直接把網頁上的內容拖放到 Heptabase 的白板裡。我們做的這些是，都是希望確保你可以從任何類型的知識資源裡面提煉出概念、建立自己的概念卡片庫，進而隨時重複應用這些你學到的知識。

It’s hard to cover everything on how Heptabase works here. So, if you want to learn more, you can check out our public wiki.

我們很難在這個專訪裡面提到所有關於 Heptabase 如何運作的細節，如果你有興趣了解更多，歡迎參考我們的 [Public Wiki](https://wiki.heptabase.com/getting-started-with-heptabase)。

---

**What about the interoperability of the information you store in Heptabase? This is a complaint many knowledge workers have with modern tools for thought.**

讓我們來聊聊 Heptabase 裡面儲存的資訊是否可以在其他地方使用？這是許多知識工作者針對現代的「思考工具」最常抱怨的地方。

Before discussing how Heptabase thinks about interoperability, I want to first share how most other companies think about it so you can see how we think differently. There are two common ways to think about interoperability. One is the interoperability across use cases, and the other is the interoperability across applications.

在討論 Heptabase 如何看待「互操作性」前，我想要先分享一下我認為其他公司對這件事的想法，這樣你可能可以更容易理解我們的作法有什麼不同。

關於互操作性有兩種常見的思考方式。一種是「跨使用情境」的互操作性，另一種是「跨應用程式」的互操作性。

The common approaches to solving interoperability across use cases are either building an all-in-one product that can accommodate many use cases through customization, or allowing third-party users to build feature-level plugins on top of your product, so that you can install multiple plugins to add features for your specific use case.

解決跨使用情境互操作性的常見方式，要嘛是建構一個能夠透過豐富的自訂性，滿足所有使用情境的全能型產品，要嘛是允許用戶在你的產品上面打造各種功能插件，透過這些不同的插件來滿足特定使用情境的功能需求。

Both approaches will introduce complexity and increase the learning curve of the product. While there are many people who love customizing their system, there are also many people who hate it because they do not want to learn and set up a whole bunch of things just to get simple work done.

這兩種方法都會讓產品變得複雜，並且讓產品變得更難上手。雖然許多人喜歡自訂他們的系統，但也有許多人討厭這樣做，因為他們不想要只為了完成簡單的工作就需要學習和設置一堆東西。

As for the interoperability across applications, there are also two common approaches. You either use APIs to expose your data for another app to use, or use a common file format another app can read, like Markdown. Both approaches have their own problems.

而關於跨應用程式的互操作性，也有兩種常見的作法。要嘛使用 API 來讓你的資料可以被其他應用程式使用，要嘛使用其他應用程式也能夠讀取的通用文件格式，例如 Markdown 。但這兩種方式也都有各自的問題。

In the API approach, you need both apps to have APIs and build integrations to make the data interoperable. You can never guarantee that it will happen. In the Markdown file approach, you’ll notice that there are tons of features that Markdown doesn’t support, so people will add extra metadata on top of these Markdown files to support those features. And if you open these files with different apps, they still won’t know how to handle this metadata, or they might handle it differently and break things, as there’s no common protocol on what you can read and write to those files.

以 API 的方式來說，你需要兩個應用程式都具有 API 的接口，並且把他們串接在一起，讓資料可以互相操作。但你沒辦法確保這件事會持續穩定運作。而以 Markdown 文件的方式來說，你會發現有許多功能是 Markdown 格式不支援的，而為了建構這些功能，人們就會在 Markdown 文件上面增加額外的 metadata ，但假設你換了一個應用程式，他還是不知道該如何處理別的應用程式上面的 metadata，或者他們會以不同的方式處理並破壞這些 metadata ，因為這些做法之間並不遵守共同的協議。

So, the way I think about how we can solve the problem of interoperability across use cases and across applications is that I want Heptabase to eventually become a system where people can build and launch their own “meta-apps” on top of it. Although we don’t allow third-party developers to build meta-apps at the moment, we have already built six native meta-apps inside Heptabase. These meta-apps are not database templates or feature-level plugins that provide new views for existing data. They are service-level applications with their unique UIs, workflows, and features that help you deal with a specific use case.


因此，我在思考我們該怎麼解決跨使用情境與跨應用程式的互操作性問題時，我希望 Heptabase 最終能夠成為一個系統，讓人們可以在上面建構和發布自己的 meta apps 。

雖然我們目前還不允許第三方開發者建構 meta apps ，但我們已經在 Heptabase 裡面打造了六個原生的 meta apps （Journal, Map, Card Library, Tag, Task, Highlight），這些 meta apps 並不是數據庫的模板或者是某些只提供特定功能的插件，他們是具有獨特 UI 介面、工作流程以及不同功能的應用程式，可以幫你解決特定使用情境下的問題。

The cool thing about meta-apps is that they all run on top of “cards” which are the primitives of Heptabase’s system. We currently have note cards, journal cards, PDF cards, and will soon introduce highlight cards, audio cards, video cards, image cards, and more. These cards are interoperable across meta-apps, and every meta-app will read and write application-specific metadata on these cards, following the same protocol.

這些 meta apps 最酷的地方在於，他們都運作在「卡片」這個 Heptabase 系統裡面最基礎的元素之上。我們目前有筆記卡片、日記卡片、PDF 卡片，並且很快就會推出 Highlight 卡片、音檔卡片、影片卡片、圖片卡片等等。這些卡片可以在不同的 meta apps 之間互相操作使用，每個 meta app 都會讀寫這些卡片上面特定的 meta data ，遵循相同的協議。

With this approach, Heptabase is essentially an OS for meta-apps and a browser for cards at the same time. And the benefit is that we can reduce the complexity of trying to install a lot of feature-level plugins or set up a lot of properties and views just to deal with a simple use case. We also don’t need to waste time building API integrations between meta-apps.

藉由這種方式，可以把 Heptabase 想成是這些 meta apps 的操作系統以及卡片的瀏覽器。而這樣做的好處是，我們可以不需要安裝特定插件或設置特定數據庫模板，降低這方面的複雜性。我們也不需要花時間串接不同 meta apps 之間的 API 。

And of course, there will still be times when you want to connect Heptabase with applications that are outside of our ecosystem, so we still support exporting all data into Markdown + YAML format, and will eventually have our APIs for others to use. But I think over time, as the entire meta-apps ecosystem grows and matures, there will be fewer needs for that.

當然，有時你還是會想要將 Heptabase 與我們生態系之外的應用程式串連使用，因此我們仍然支援把所有數據都匯出成 Markdown + YAML 格式，最終也會提供我們的 API 給大家使用。但我認為隨著整個 meta apps 的系統越來越成熟，這方面的需求會越來越少。

---

**Another challenge is to support both individual and collective knowledge creation.**

你們的另一個挑戰是如何同時支援個人以及集體的知識創造？

Definitely. Although we’ve been focusing on the individual learning and research process since 2021, collective research is one of the major problems that we plan to tackle in 2024. It is important because most important problems humans have solved, we have solved them collectively. We have to put together knowledge puzzles that were scattered across people’s brains.

確實，雖然從 2021 年以來，我們一直專注於個人的學習和研究過程，但集體之間的研究是我們計畫在 20424 年解決的主要問題之一。我們認為這非常重要，因為人類解決大多重要問題的方式都是集體一起解決的，我們想要把散落在不同人大腦中的知識拼圖都拼起來。

The tricky thing about modern solutions for collective research is that people seem to believe that all you need is a collaborative workspace where a group of people can edit and connect documents together. Solutions like this are great for building a wiki or ensuring that people are aligned on a project, but I think it doesn’t really address the core problem of collective research, which is how everyone’s input on a topic can gradually lead to a deeper understanding of that topic for everyone.

這件事情困難的地方在於，當代針對集體研究這件事的解決方案，似乎都是認為你只需要一個共同協作的空間，讓一群人可以共同編輯和連結不同文件就好。

我們認為這種解決方案很適合拿來建構 wiki 系統或者是確保人們對於某個專案的理解是一致的，但這並未解決集體研究的核心問題：該怎麼讓每個人對於一個主題的持續輸入演進為對於這個主題的更深度理解。

It’s obvious that you need a place where everyone can contribute their knowledge and ideas. The non-obvious part is how to structure this information in a way that can avoid groupthink, direct your attention to things that are useful to you, ensure that everyone can still perform independent thinking processes while leveraging the knowledge others have contributed, and facilitate the discussions that can lead to establishing a deeper understanding of the topic. These are some of the problems that we’ll be working on when building a communication layer on top of Heptabase.

針對這件事的解決方式，比較明顯的是你需要一個地方讓每個人都能夠貢獻他自己的知識與想法。但比較幽微的部分則是如何為這些資訊建立架構，以避免團體迷思；還有如何引導你的注意力到對你有用的事情上，確保每個人在利用他人貢獻的知識時，仍然可以進行獨立思考，並且讓這些討論能夠促成對於這個主題更深度的理解。這些是我們在打造 Heptabase 的 Communication Layer 時要解決的問題。

There are two core ideas on how we plan to address this problem at the beginning. The first is to create a back-and-forth process between personal workspace and collective workspace, so people can still have their own independent thinking process. The second is to help people in the collective workspace to create objectives, structure these objectives, and create different representations for the same objectives using their collective knowledge. Designing this will be a huge challenge, and I don’t think we can get it right in the first version. What we will do is conduct internal testing and see how it works for the entire Heptabase team. Then, we can involve more community members and gradually open it up to more people.

在解決這個問題的最一開始，我們有兩個核心的想法。第一個是要打造一個個人工作區與集體工作之間的來回流程，讓人們可以在貢獻集體知識時仍然保有個人的獨立思考空間。另一個則是協助集體工作區裡面的用戶建立他們的目標（objectives），結構化這些目標，並且利用他們的集體知識，針對這些目標創造不同的表達方式。

這方面的設計是個巨大的挑戰，我不認為我們可以在第一個版本就達到完美，但我們將先進行團隊的內部測試，看看運作起來效果如何，接著我們會向更多社群成員開放，並繼續開放給更多人。

---

**What about you, how do you use Heptabase?**

那你呢？你自己是如何使用Heptabase的？

I mainly use Heptabase for learning, research, planning, and writing. Every morning, I’ll first open my journal and see the tasks I need to do for that day. There will be a bunch of to-dos that I wrote or assigned a few days ago. Let’s say it’s the end of the month and I need to write an investor update. I also want to research the design of this new product feature, spend some time on the growth strategy, and read another chapter of the book I’m currently reading.

我主要使用 Heptabase 學習、研究、規劃和寫作。每天早上，我首先會打開我的 Journal 日記，看看那天我需要做的任務。這時通常會有一堆我在幾天前寫下或指派的待辦事項。比如說現在是月底，我需要寫一份給投資人的更新；我也想針對某個產品的新功能研究一下該如何設計；我還打算花一些時間思考產品增長的策略，並且閱讀我目前正在讀的書的另一章。

One of my favorite features about Heptabase is that whenever I open a whiteboard, a card, or a tag, I can open them like a browser tab on my left sidebar. I can pin the tabs that I commonly visit and create tab groups for different types of work.

我最喜歡 Heptabase 的一個地方是，每當我打開一個白板、一張卡片或一個標籤時，我可以像瀏覽器分頁一樣在左側欄打開它們。我可以將我常訪問的分頁釘選起來，並為不同類型的工作建立分頁群組。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/heptabase-interview-2_cXjRSe.webp" data-fancybox data-caption="heptabase-interview-2">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/heptabase-interview-2_cXjRSe.webp" loading="lazy" alt="heptabase-interview-2" align="center" />
</a>

For example, I want to first write that investor update. I’ll go to the “Company Operation” tab group, open the #investor-update tag, and create a new card to start writing. While writing, I might search for and open some existing cards on the right sidebar as a reference.

舉例來說，我想先寫那份投資人更新，我會到「公司營運」的分頁群組，然後打開「#investor-update」這個標籤，並且建立一張卡片開始寫作。寫作時我可能會在右側邊欄搜索並且開啟一些卡片作為參考。

After I finish writing, I’ll check the to-do in my journal and move on to product research. I’ll go to the “Product Research” tab group, open a pinned whiteboard called “Better Collecting → Thinking” which has all my product ideas and user insights on this problem. I might add some new ideas, stare at them, rearrange them, group them, and refine the whiteboard structure until I feel like I have a better understanding of this problem. Then I’ll write a feature specification using the ideas on this whiteboard and send that spec to the designer for feedback.

寫完後，我會回到我的日記裡面把這項待辦事項打勾，接著繼續進行產品的研究。這時我會去「產品研究」這個分頁群組，打開一個叫做「Better Collecting → Thinking」的固定白板。在這個白板裡面涵蓋了我對這個問題的所有產品想法以及來自用戶的各種洞察。我這時可能會增加一些新的想法、單純盯著某些卡片看，或重新排列與分類這些卡片，直到我覺得我針對這個問題有了更好的理解，這時我會把這些想法寫成一份功能規格的卡片，並且提供給我們的設計師看看他有沒有什麼回饋。

Once done, I’ll check the to-do list in my journal and go to the “Growth Research” tab group, and open the “Retention & Engagement” whiteboard. I have clipped several long articles from the web in that whiteboard, and I will break these long cards into smaller concept cards, rewriting the knowledge I learned in my own words. The title of each concept card is usually a sentence, and the content consists of supporting arguments and evidence

完成後，我會回到日記裡面把這項待辦事項打勾，接著到「增長策略」的分頁組，打開「用戶留存與參與」這個白板。我在這個白板裡面貼上了幾篇我在網路上看到的長文章，我會把這些文章拆解成更小的概念卡片，並且用我自己的話來描述我學到的知識，每個概念卡片的標題通常就是一句話，而內容則是支持這句話的論點與證據。

One thing I love doing is reading a lot of articles, distilling the knowledge, and forming my unique understanding on the whiteboard using the knowledge I’ve gained from all these articles. Then, I devise the growth strategy based on this understanding.

我最喜歡做的一件事就是閱讀大量的文章，並且從中提煉知識，接著利用白板上面所有我獲得的知識，建立屬於我的獨立理解。接著，我會再根據這些理解，來制定我們的增長策略。

Now that I’ve completed all the work for today, I’ll go to the “Personal Learning” tab group, and open the “Reading Notes” whiteboard. Let’s say I’m reading this book called Innovator’s Dilemma, and I’ll have a sub-whiteboard for it with the book title as its name. In this sub-whiteboard, I also break down all the knowledge I’ve learned from this book into concept cards.

這時，我已完成了今天的所有工作，我會前往「個人學習」這個分頁組，打開我的「閱讀筆記」白板。例如我正在閱讀《創新的兩難》這本書，我會再為它建立一個以它為名的子白板，然後把我在這本書裡面學到的所有知識都拆解成原子概念卡片。

Assuming today I’m reading this chapter about competition in the hard drive market, and I create many concept cards about it. This reminds me of other concept cards that I created for other books that are also about competition. So another thing I love doing is that I might create a whiteboard called “Competition Philosophy,” and then import all the concept cards I have about competition from the “Innovator’s Dilemma” whiteboard and other books’ whiteboards like Zero to One, The Art of War, and Chip War.

假設今天我正在閱讀有關硬碟市場競爭的這個章節，這時我會建立許多相關的概念卡片。這又讓我想起我在讀其他書的時候建立的，也是關於競爭的概念卡片。這時我可能會做、也最喜歡做的事情是，再建立一個叫做「競爭哲學」的白板，然後把我在《創新的兩難》這本書裡面、還有《從零到一》、《孫子兵法》、和《晶片戰爭》這幾本書裡面關於競爭的概念卡片都放進來。

This is something that I’ve done a lot in Heptabase, which is essentially creating whiteboards on different topics, and reusing the concept cards that I extracted from different books, articles, videos, and PDFs for these topics’ whiteboards and gradually forming a deeper understanding over time.

這是我反覆在 Heptabase 裡面做的事情，簡單來說就是創立不同主題的白板，然後重複使用我在不同書籍、文章、影片和 PDF 裡面提煉的概念卡片，並隨著時間與累積，逐漸形成更深度的理解。

---

**How do you recommend someone get started with Heptabase?**

你建議人們該怎麼上手 Heptabase ？

I think the best way to get started with Heptabase is simply to find a topic or a book you’re interested in and create a whiteboard for it.

我想，要上手 Heptabase 的最好方法，就是找到一個你感興趣的主題或一本書，然後為它建立一個白板。

For example, if you’re interested in Deep Learning and there are these three long articles that you want to read, you can open the articles side by side with Heptabase and extract content to Heptabase’s whiteboard to create concept cards. Each concept card should contain an idea that you think is important.

舉例來說，如果你對深度學習感興趣，並且你已經知道有三篇很長的文章你想閱讀，你可以直接把這文章與 Heptabase 並排打開，並且把裡面的知識提煉到 Heptabase 的白板上面，並且建立概念卡片。每張卡片應該只包含一個你認為最重要的想法。

The “aha” moment of Heptabase is that you gradually accumulate more and more cards from more and more sources, and you’ll find the sense-making process on the whiteboard very smooth. You will find it very easy to get into the flow of thinking, and several hours later, you’ll have formed this unique understanding of the topic. You will know what you’re going to read next, how you’re going to integrate new knowledge with existing knowledge, and you will know that this understanding will be stored visually here forever.

使用 Heptabase 的「頓悟時刻」是，當你逐漸從愈來愈多的地方，累積愈來愈多的卡片，你會發現你在白板上面建立理解的過程會非常流暢，很容易就進入思考的心流，幾個小時後，你會發現你已經針對這個主題建立了屬於你的獨特理解。你會知道接下來你該閱讀什麼、你該如何將新學到的知識與你既有的知識結合，並且你也會知道這些屬於你的理解，將永遠透過視覺化的方式儲存在這裡。

<a href="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/heptabase-interview-3_F8Gu3d.webp" data-fancybox data-caption="heptabase-interview-3">
  <img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/heptabase-interview-3_F8Gu3d.webp" loading="lazy" alt="heptabase-interview-3" align="center" />
</a>

---

**And finally… What’s next for Heptabase?**

最後，Heptabase 接下來有什麼計畫？

In the next quarter, we have three priorities. First, as I mentioned earlier, we want to introduce more types of cards, especially multimedia, and allow users to highlight, annotate, and extract knowledge from these different types of cards. The second priority is to build a communication layer on top of Heptabase to enable the collective research process. The third priority is to upgrade our backend infrastructure as we are now facing a much larger user scale than in 2022.

在下一季，我們有三件最優先的事。第一個，就如我先前提到的，我們將引入更多種類型的卡片，特別是多媒體的卡片。並且我們也將讓用戶可以針對這些不同的多媒體卡片去 highlight、備註以及提取知識。第二個優先事項是在 Heptabase 上面建構 Communication Layer，以促進集體的知識研究。第三件事是升級我們的後端系統，因為我們現在有比 2022 年更多的用戶了。

And of course, we will continue to refine and improve the experience of existing features like whiteboards, cards, and tags, which are the foundation of everything we have built. In the end, it all points back to our vision, which is that we are doing everything we can to create a world where everyone can effectively establish a deep understanding of anything.

當然，我們也會繼續完善與改進既有功能的體驗，例如白板、卡片編輯器、標籤等等，這些都是 Heptabase 的基礎。最終，這些不同的功能都是指向我們的願景，我們正努力地打造一個，能夠讓任何人有效地對任何事物建立深度理解的世界。

---

**Thank you so much for your time, Alan! Where can people learn more about Heptabase?**

非常感謝你的時間！大家可以在哪邊了解更多關於 Heptabase 的消息呢？

You can try out Heptabase from our website. The best place to learn more about it is our public wiki. If you want to learn about our philosophy, I recommend reading My Vision – The Roadmap and The best way to acquire knowledge from readings. If you just want to learn about how the current product works, I recommend checking out Getting Started with Heptabase and Heptabase 1.0. We have an active Discord community with more than 12,800 members that we welcome you to join. We also occasionally share some product updates on Twitter (X).

你可以到我們的[官網試用 Heptabase]((https://get.heptabase.com/nesslabs)) ，而了解更多資訊的最佳管道是我們的 [Public Wiki](https://wiki.heptabase.com/?lang=zh-Hant)。如果你想要了解我們的理念與願景，我推薦你閱讀 [My Vision - The Roadmap](https://wiki.heptabase.com/the-roadmap?lang=zh-Hant) 以及 [The best way to acquire knowledge from readings](https://wiki.heptabase.com/the-best-way-to-acquire-knowledge-from-readings?lang=zh-Hant) 這兩篇文章。

如果你只是想了解目前 Heptabase 怎麼運作，我推薦你閱讀 [Getting Started with Heptabase](https://wiki.heptabase.com/getting-started-with-heptabase?lang=zh-Hant) 以及 [Heptabase 1.0](https://wiki.heptabase.com/version-one?lang=zh-Hant) 這兩篇文章。

我們有一個活躍的 [Discord 社群](https://discord.com/servers/heptabase-812292969183969301)，裡面有超過 12,800 個用戶，歡迎你加入。我們也會偶爾在 [Twitter（X）](https://twitter.com/Heptabase)上面分享一些產品更新的內容。
