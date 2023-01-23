---
title: 嘗試解決 Railway 鎖住導致 umami 跟 Cusdis 失效的問題
date: 2022-07-09
description: 希望以後 Railway 能安穩一點，如果要付費就付吧XD
path: snapshots/what-i-tried-today/tried-to-re-deploy-umami-and-cusdis-after-being-locked-by-railway
taxonomies:
  kinds: 
    - What I Tried Today
  tags: 
    - Railway
    - Umami
    - Cusdis
---

昨晚點開我的 umami dashboard ，想查看這禮拜的 blog 數據，卻突然發現無法登入。

看了一下，發現是 Railway 的免費額度限制，必須要填寫信用卡資訊，如果不填的話資料庫就會被鎖住（不確定是否是這個原因，總之我的資料庫被鎖住不能用）。

於是我就趕快升級方案，但還是卡住，就先去睡了。今天早上起來，發現資料庫是解鎖了，但 umami 跟 Cusdis 還是不能用，花了一個多小時總算搞定它們並且重新上線，也學到兩件事：

1. 目前我的 umami 是部署在 Railway 裡面，他可以選擇要採用哪個 branch ，也可以自動設定要更新 umami repo 的版本，我發現原來選完更新後，他會對我的 umami repo 產生一個 pull-request ，這時我要到 github 上面去 merge ，merge 完畢後，Railway 就會重新開始部署 umami 了（花了四十分鐘），在這之後終於可以重新上線。

2. Cusdis 部分，我則是資料庫放在 Railway，服務部署在 Vercel ，但資料庫解鎖後，Vercel 那邊還是無法 redeploy 成功，看了一下 logs ，發現好像是連不到資料庫。因此重新看了一下變數，發現資料庫的網址好像跟 Railway 那邊不一樣，於是重新填寫後，也順利部署成功了。

希望以後 Railway 能安穩一點，如果要付費就付吧XD ，有付費的話再來更新一下付費心得與資訊。