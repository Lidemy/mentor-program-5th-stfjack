## 請解釋後端與前端的差異。

前端主要是建立使用者看的到的東西，要讓東西能夠跟使用者作互動，並且增加使用時的體驗。像是運用 Html 為網頁增添骨幹的內容架構、CSS 增加版型和網站的美觀、JavaScript 為網頁增加動畫、設計按鈕選項 。
後端則是使用者看不到的部分，包含使用者帳戶、輸入資料的資料庫儲存跟管理，伺服器的架設與部署。

## 假設我今天去 Google 首頁搜尋框打上：JavaScript 並且按下 Enter，請說出從這一刻開始到我看到搜尋結果為止發生在背後的事情。

當按下 Enter 鍵的那一刻，我們下的指令會由瀏覽器，經由操作系統(Operation System)傳遞給網路卡對目標進行通訊，會先透過 DNS SERVER 找到 Google.com 這個網址對應的 IP Address。
然後透過 Client 對 Google Server 端發送 Http request，使用 TCP/IP 網路通訊協定。當 Server 端收到來自 Client 端的 Request。
如果 Server 同意請求，Server 端就會去它所連接的 database 撈資料出來，Responese 給使用者。Client 端就可以就可以跟 Server 端進行封包數據傳輸及互相確認。
Google 檢索主要是由它們派發 bot 去逛網頁，透過找尋例如 html 中標題關鍵字檢索，網站更新頻率，關鍵字提到的次數，頁面重複性質等眾多考量指標而定，最後加入它們的檢索資料庫清單。
再經由使用者的搜尋請求，依據檢索分數排行指標排序，回應呈現給使用者。檢索到的內容也會跟使用者所在的區域、語言，和使用者偏好習慣有所差異。當然也會有一些商業投放廣告的呈現可能。(Google Ads)
傳輸到本地完成的網頁資料副本，會放在本地的快取暫存中，然後經過讀取顯示出來。就是我們看到的網頁顯示的檢索結果。

參考 google developer 提供的資料。[搜尋服務的運作方式 (基礎知識)](https://developers.google.com/search/docs/basics/how-search-works)

## 請列舉出 3 個「課程沒有提到」的 command line 指令並且說明功用

1. head "file name" : 快速檢視文件前面 10 行，也可以打 head -20 "file name"，檢視文件前面20行
2. tail "file name" : 快速檢視文件後面 10 行
3. history : 列出所有操作過的指令，可以用來快速檢索剛剛進行了哪些指令輸入。