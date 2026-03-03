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
🌊 巴部農 2026 螢火蟲季：心理測驗活動網站 交接需求單

To: 網頁工程團隊
From: 行銷部

你好！為配合今年的螢火蟲季行銷活動，我們規劃了一個「尋找內在微光」的互動式心理測驗。
附上的 HTML 檔案是我們製作的 Prototype（原型），已經包含了完整的前端版面、測驗邏輯與動態特效。

希望將此頁面部署為一個獨立的活動網頁 (Campaign Site)。以下是相關的技術規格與協作需求，再麻煩協助調整與上線！

1. 網站架構與網址建議

為了品牌一致性，建議將此單頁應用程式（SPA）掛載於我們的官方網域下。

首選（子網域）：https://event.babulong.com.tw/2026-firefly

次選（子目錄）：https://www.babulong.com.tw/events/2026-firefly

2. 技術規格 (Tech Stack)

原型的撰寫非常輕量，方便你們快速接手：

核心：純 HTML5 + 原生 JavaScript (Vanilla JS)

樣式：Tailwind CSS (目前為 CDN 載入，若需打包可改為專案內建)

字體：Google Fonts (Noto Serif TC 襯線體，請保留以維持精品感)

動畫：純 CSS Keyframes (螢火蟲背景特效已寫在 <style> 中)

3. 工程師待辦清單 (Action Items)

請協助將 Prototype 中的假資料替換為正式的營運設定：

🛠️ A. 靜態資產替換 (Assets Replacement)

背景圖片：請將 CSS 中 .bg-forest 的 background-image 替換為我們提供的官方高畫質森林背景圖。

分享首圖 (OG Image)：請於 <head> 中補上完整的 Meta Tags，確保用戶在 LINE / FB 分享網址時，會抓到正確的標題與預覽圖。

<meta property="og:title" content="巴部農｜測測你是哪一種珍稀微光？">
<meta property="og:description" content="閉上眼，聽聽這段跨越 4,500 年的聲音。尋找專屬於你的微光與精品水...">
<meta property="og:image" content="【請填入官方 OG 圖片網址】">


🔗 B. 購物車連結串接 (CTA Links)

在 JS 程式碼的 resultsData 中，有四種結果的 CTA 按鈕。請協助將 copyAndNotify 函式改寫為跳轉至對應的商品頁面，並自動帶入優惠碼（或直接跳轉至結帳頁面）：

類型 A：跳轉至 1250ml 慢飲典藏組 (帶入碼 WISDOM100)

類型 B：跳轉至 330ml 質感隨行瓶 (帶入碼 GLOW2026)

類型 C：跳轉至 你喝水，我種樹 年購組

類型 D：跳轉至 限定商品網頁 (帶入碼 ART88)

📊 C. 追蹤碼埋設 (Tracking & Analytics)

為了行銷成效歸因，請協助在以下動作發生時，觸發 GA4 / Meta Pixel 的事件 (Events)：

開始測驗：點擊「開始測驗」按鈕時 (event: start_quiz)

完成測驗：進入 renderLoading 或 renderResult 時 (event: generate_lead 或 quiz_completed，並記錄出哪一種結果 A/B/C/D)

點擊前往購買：點擊結果頁的導購按鈕時 (event: click_to_buy)

📱 D. IG 限動分享功能 (進階需求，可評估)

目前的「分享至 IG 限時動態」按鈕 (shareResult()) 是 Alert 提示。
如果技術上允許，請協助串接 Web Share API，或是自動生成一張帶有該用戶結果的圖片讓他們長按儲存。若時程來不及，可改為：「長按截圖此畫面，分享至 IG 限動」。

4. 預期上線時程

測試站 (Staging) 審閱：[填寫日期]

正式上線 (Production)：[填寫日期]

有任何前端邏輯或設計需調整的地方，隨時與行銷部討論，辛苦了！
