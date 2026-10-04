# ⚡️ 排班填休秒殺神器 - Google Form iOS Sniper

> 每月 20 號 16:00 搶填休假不再落後！專為 Google 表單排班搶休最佳化，0.1 秒全自動填妥並秒送出。

---

## 📖 專案簡介 (Introduction)

在許多排班制的職場中，每個月固定時間（例如 20 號 16:00）主管會釋出 Google 表單讓同仁登記休假。由於休假熱門名額有限，用手機手動輸入「姓名」與繁瑣的「日期假別」經常會落後。

**排班填休秒殺神器** 是一個純前端（Client-Side）、零資料外洩的輔助產生器工具。它針對 Google 表單前兩道常見題目（第 1 題姓名、第 2 題排班內容）進行智慧定位，提供多種搶單自動化腳本，即使每個月發出的 Google 表單網址不同也能通用！

---

## ✨ 核心特色 (Features)

1. **純前端無後端架構**：所有姓名與排班設定僅在使用者本機端瀏覽器計算，無任何外部伺服器傳輸，注重個人隱私與資安。
2. **快速排班組裝工具**：視覺化選擇月份、日期範圍與假別（休假、特休、補休等），自動以頓號連接，免去手動輸入符號出錯的困擾。
3. **三種自動化搶單方案**：
   - **方案 A（Userscripts 全自動外掛，推薦）**：搭配 Safari Userscripts 延伸模組，表單打開瞬間 0.1 秒內自動填入並送出，零點擊最快！**現已支援一鍵下載 `.user.js` 腳本檔案**，方便直接匯入 iOS / macOS 的 Userscripts App。
   - **方案 B（Safari 魔法書籤 Bookmarklet）**：免安裝任何額外 App，存入 Safari 書籤後，點一下書籤瞬間填完提交。
   - **方案 C（iPhone 輸入法替代文字）**：純原生系統設定，透過自訂輸入碼快速帶出長字串。
4. **手機端 0.1 秒極速模擬沙盒**：內建模擬 Google 表單與高精度測速器（`performance.now()`），直觀驗證腳本自動填表與送出流程。
5. **完整 iPhone 圖文設定教學**：包含最重要的 **LINE Labs 預設瀏覽器避坑指南**，避免因 LINE 內建瀏覽器無法執行擴充功能而翻車。

---

## 🛠 技術棧 (Tech Stack)

- **HTML5 & CSS3**：語意化標籤與響應式排版
- **Tailwind CSS (CDN)**：現代化 UI 設計系統、iOS 擬物風格（毛玻璃、卡片式設計、iOS Switch 開關）
- **Vanilla JavaScript (ES6+)**：
  - `MutationObserver`：監聽非同步表單 DOM 渲染，確保輸入框掛載完畢立即注入
  - `Event.dispatchEvent`：分發 `input` 與 `change` 事件以觸發 Google 表單內部狀態綁定
  - `Navigator.clipboard` + 降級相容機制：支援一鍵複製
  - `performance.now()`：高精度微秒級測試計時

---

## 🚀 部署與線上訪問 (Live Demo)

- **GitHub 專案位址**：[https://github.com/xuanlii/google-form-sniper](https://github.com/xuanlii/google-form-sniper)
- **GitHub Pages 公開網址**：[https://xuanlii.github.io/google-form-sniper/](https://xuanlii.github.io/google-form-sniper/)

---

## 📄 授權條款 (License)

MIT License. 本工具僅供個人日常工作排班輔助使用。
