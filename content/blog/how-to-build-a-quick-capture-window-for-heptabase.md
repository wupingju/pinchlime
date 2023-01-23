---
title: 如何自己打造一個 Heptabase 的快速輸入視窗
date: 2023-01-08
path: blog/how-to-build-a-quick-capture-window-for-heptabase
description: 我在任何地方按下 F2 後，就會跑完上述一連串的流程，然後出現一個 Heptabase 的縮小版輸入視窗，鎖定在今天的 Journal 頁面，可以讓自己快速輸入想法。
taxonomies:
  categories: 
    - Workflows
  tags: 
    - Heptabase
    - Keyboard Maestro
    - BetterTouchTool
    - Quick Capture
---

昨晚在 Heptabase 的 discord 裡，有個名叫 LiteC 的用戶[分享了一個很讚的想法](https://discord.com/channels/812292969183969301/839550981695340544/1061314941996515389)，他透過幾個工具的串接，達到以下的效果：

1. 可以透過 hot corner 叫出 Heptabase Journal 的 Today 介面
2. 這個介面還設定成 Always on top，也就是不會被其他視窗干擾

這個分享讓我非常興奮，因為之前一直覺得 Heptabase 暫時還缺了一個好用的「快速輸入」介面，但沒想到可以不用等官方製作，自己就有機會辦到了。

<!-- more -->

---

於是我今天也自己用手邊的工具做了一個版本，我用到的工具組合是 BetterTouchTool 以及 Keyboard Maestro，而我採用的是熱鍵觸發而不是 hot corner 觸發。

我的步驟如下：

透過 Keyboard Maestro 快速啟動固定尺寸的輸入視窗：

1. 設定熱鍵，啟動 Heptabase
2. Show Heptabase （把它拉到最前面的視窗）
3. 設定 Resize ，我是用「Resize Front Window to Pixels」的功能，設定為寬 480px，高 720px。
4. 移動到畫面右下角，我是用「Move Front Window to Position」這個 action 去設定的。
5. 最後為整串的 Keyboard Maestro 腳本設定一個熱鍵，我是設定為很容易按到的 F2。

這樣做的效果是，我在任何地方按下 F2 後，就會跑完上述一連串的流程，然後出現一個 Heptabase 的縮小版輸入視窗，鎖定在今天的 Journal 頁面，可以讓自己快速輸入想法。輸入後就可以把它關閉，而不會打擾原本的工作流。

而若要把視窗「固定住」，則要透過 BetterTouchTool，我設定的觸發條件是「用右鍵按左上角橘黃色的縮小按鈕」。

不過我目前測試這個功能還不太穩定，可能沒辦法常態使用，但偶爾有需要時可以用用看。

以下是簡單的螢幕錄影示意：

<img src="https://pinchlime-screenshots.s3.ap-northeast-1.amazonaws.com/heptabase-quick-capture_W9DtLe.gif" loading="lazy" alt="heptabase-quick-capture" align=center />


我在瀏覽網頁時按下熱鍵後，就叫出了右下角的這個輸入視窗，並且可以按一下我指定的觸發按鈕使視窗固定在最上層，以方便剪貼或編輯文字。


這個功能同樣可以用在「把 Heptabase 叫出來查找內容，只要叫出視窗後，按下內建的 Command + O 就可以了！


備註：
- 感謝 LiteC 的分享，期待未來 Heptabase 也能推出內建的 quick capture 功能。
- 很多工具可能都可以達到類似的「快速啟動」效果，也不一定要 resize ，所以未必要用到本文提到的兩個工具。完全可以依照個人需求打造適合的啟動方案。