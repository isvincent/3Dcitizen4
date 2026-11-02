# 所有權法治小鎮｜3D 公民互動教材

## 功能
- Three.js WebGL 實體幾何模型（Mesh）、陰影與物件深度遮擋，真正支援任意角度旋轉、縮放、平移。
- 7 座可點擊低多邊形建築，含鏡頭聚焦與全島導航。
- 七站學習內容、選擇題解鎖、解析、筆記、教師模式、雙節課教學流程。
- localStorage 儲存完成情況、分數與筆記；匯出 JSON / TXT。
- 手機、平板、桌機 RWD；含 Web App Manifest 與 Service Worker。

## 檔案
- `index.html`：網頁、3D 模型、互動及教材。
- `manifest.webmanifest`：PWA 設定。
- `sw.js`：網頁同來源檔案快取。

## 部署 GitHub Pages
1. 建立公開 GitHub Repository，將三個檔案上傳至根目錄。
2. Settings → Pages → Build and deployment → Deploy from a branch。
3. Branch 選 `main`，資料夾選 `/(root)`，儲存。
4. 等待 Pages 網站部署後，以 HTTPS 網址開啟即可使用。

## 在電腦本機測試
在資料夾中執行 `python -m http.server 8000`，打開 `http://localhost:8000`。直接雙擊 `index.html` 可能因瀏覽器安全策略而無法啟動模組。

## 網路及離線限制
Three.js 及 OrbitControls 從 jsDelivr CDN 載入，因此首次使用必須連網。PWA 只保證本網站本身資源可快取，**不保證離線時 3D 引擎可用**；若需可靠完整離線使用，應將 Three.js 模組及相依檔案下載至專案並修改 import map。

## 教材依據
上傳檔案《公民(所有權的物權特性)(1).pdf》，7 頁（原書頁碼 109–115）。包含所有權意義、四項特性、民法 767 條救濟、物權法定、不動產登記、公共利益及智慧財產權。

## 教師模式
首頁按「教師模式」，可跳轉未解鎖建築；學生模式需逐站答對才能解鎖。所有資料僅在使用者當前瀏覽器儲存，沒有帳號、資料庫或老師端收件功能。

## 使用注意
本頁法律內容為根據指定教材改寫的教學案例，不構成法律意見。完整課程可搭配法規最新版本核對；各題答對後不重複計分。
