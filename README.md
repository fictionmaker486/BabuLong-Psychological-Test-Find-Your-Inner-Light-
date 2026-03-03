# BabuLong-Psychological-Test-Find-Your-Inner-Light-
你好！為配合今年的螢火蟲季行銷活動，我們規劃了一個「尋找內在微光」的互動式心理測驗。 附上的 HTML 檔案是我們製作的 Prototype（原型），已經包含了完整的前端版面、測驗邏輯與動態特效。  希望將此頁面部署為一個獨立的活動網頁 (Campaign Site)。以下是相關的技術規格與協作需求，再麻煩協助調整與上線！
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

類型 D：跳轉至 達文西聯名限定版 850ml (帶入碼 ART88)

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
