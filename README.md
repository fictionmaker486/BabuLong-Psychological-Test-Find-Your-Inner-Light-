# BabuLong-Psychological-Test-Find-Your-Inner-Light-
你好！為配合今年的螢火蟲季行銷活動，我們規劃了一個「尋找內在微光」的互動式心理測驗。 附上的 HTML 檔案是我們製作的 Prototype（原型），已經包含了完整的前端版面、測驗邏輯與動態特效。  希望將此頁面部署為一個獨立的活動網頁 (Campaign Site)。以下是相關的技術規格與協作需求，再麻煩協助調整與上線！
🌊 巴部農 2026 螢火蟲季：尋找內在微光 心理測驗活動

📝 專案簡介 (Project Overview)

你好！為配合今年的螢火蟲季行銷活動，我們規劃了一個「尋找內在微光」的互動式心理測驗。

本專案目錄內包含了我們製作的 Web App Prototype（原型），該檔案已經包含了完整的前端版面、測驗邏輯與動態特效。我們的最終目標，是將此頁面部署為一個獨立的活動網頁 (Campaign Site)，確保消費者在參與測驗時不受主站其他資訊干擾，享受最純粹的品牌沉浸體驗。

✨ 核心功能 (Key Features)

沉浸式視覺體驗：深邃森林背景搭配純 CSS 打造的「螢火蟲漂浮閃爍」動態特效。

毛玻璃 UI (Glassmorphism)：採用符合巴部農高端品牌調性的半透明質感介面。

完整測驗邏輯：4 道精品生活情境題，自動計算權重並導向 4 種對應的「微光人格」結果。

導購與分享機制：結果頁包含針對不同人格的專屬折扣碼、推薦商品，以及社群（IG 限動）分享的 Call-to-Action。

🛠️ 技術架構 (Tech Stack)

為了讓網頁載入極致輕量且易於接手，本原型採用以下技術：

核心：HTML5 + 原生 JavaScript (Vanilla JS)

樣式：Tailwind CSS (透過 CDN 引入，極速構建響應式排版)

動畫：純 CSS Keyframes (高效能的螢火蟲粒子特效與淡入淡出轉場)

字體：Google Fonts - Noto Serif TC (思源宋體，營造精品雜誌感)

🚀 啟動與測試 (How to Run)

本專案為純靜態的單頁應用程式 (SPA)。

無需安裝任何環境或依賴套件。

直接使用任何現代瀏覽器（Chrome, Safari, Edge）打開 babulong_quiz.html 即可完整體驗動態效果與測驗流程。

📋 工程師接手待辦清單 (To-Do for Dev Team)

為了將此 Prototype 轉為正式上線的活動網站，請參考同目錄下的 developer_brief.md，主要待辦事項包含：

替換靜態資產：置換正式版背景圖與設定全站 OG 標籤。

串接購物車連結：將結果頁的按鈕跳轉至對應的商品結帳頁，並自動帶入優惠碼。

埋設追蹤碼：於「開始測驗」、「完成測驗」與「點擊購買」等事件綁定 GA4 / Meta Pixel。

Designed & Planned by BabuLong Marketing Team | 2026 Firefly Campaign

有任何前端邏輯或設計需調整的地方，隨時與行銷部討論，辛苦了！
