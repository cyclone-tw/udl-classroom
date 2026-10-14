# UDL 課堂教材（115 南一國語）

給老師與學生用的離線課文朗讀器目錄。打開以後先輸入老師給的課堂密碼。

- 網站：<https://cyclone-tw.github.io/udl-classroom/>
- 內容：115 學年度南一國語四年級上第 1–12 課；三年級上目前第 1–3 課
- 每課有原文朗讀、簡易版、識字、小測驗；三上另有句子練習

<!-- udl-family-block v1 -->
> **UDL 教學家族**：本 repo 是課堂朗讀器的成品網站（公開，過渡）；每頁都加密，平台上線後朗讀器搬進平台、本 repo 退休。
> 上游：`udl-learning`（朗讀器組裝與 `encrypt_site.mjs` 加密）；下游：學生裝置（GitHub Pages 網頁，輸入課堂密碼才看得到）。
> 家族地圖正本：`cyclone-tw/udl-learning` 的 `docs/family-map.md`（私人 repo）。要改本 repo 的角色或串接方式，先改地圖。
<!-- /udl-family-block -->

## 怎麼給學生或其他老師

1. 把上面的網站網址傳出去。
2. 另外用口頭、聯絡簿或私訊告訴對方課堂密碼。不要把密碼寫在這個 repo 或公開貼文。
3. 請用 Safari 或 Chrome。若畫面或聲音怪怪的，關掉舊分頁再從目錄重開。

## 版權

課文原句來自南一書局 115 學年度國小國語，僅供班級課堂使用，請勿轉載。  
插圖、簡易版與朗讀器組裝是資源班自製教材。課文 PDF／教師手冊不在這個 repo。

## 工程備註

播放器與組裝腳本在私人 repo `cyclone-tw/udl-learning`。這個公開站的每個 HTML 都用課堂密碼加密（AES-256-GCM，金鑰由 PBKDF2 從密碼推出；udl-learning#126）。檔案裡只有密文，沒有密碼就看不到課文和音檔。`gate.json` 是加密用的鹽與次數，公開無妨。新增或更新頁面一律用 udl-learning 的 `prototypes/lesson-reader/scripts/encrypt_site.mjs` 加密後再 push。
