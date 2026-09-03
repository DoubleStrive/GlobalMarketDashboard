# 全球資產市場看板 (Global Market Dashboard)

輕量、純前端架構的金融監控看板。整合 TradingView 圖表與公開 API，即時追蹤核心外匯、美債 ETF 與國際現貨黃金。

## 核心功能

* 零建置環境：單一 index.html 檔案即可運行，無需 Node.js、npm 或後端伺服器。
* TradingView 圖表：支援多週期（1分 / 5分 / 1小時 / 日K）與樣式（折線 / K線）切換。
* 多面板佈局：支援 3x2 分割網格、單欄縱向清單，並可將單一圖表最大化檢視。
* 寬螢幕適應：提供 100% 邊緣滿版與 1380px 居中寬版切換。
* 自動更新機制：內建毫秒級倒數計時器（預設 60 秒），支援一鍵暫停與手動即時更新。
* 交叉匯率換算：支援美元、台幣、日圓、人民幣、泰銖雙向換算，以及 1 盎司黃金兌台幣速算。
* 深淺色模式：預設暗色交易室介面，支援切換為淺色主題並自動儲存偏好。

## 監控標的與資料來源

| 標的 | 代號 | 類型 | 圖表來源 | 報價來源 |
| --- | --- | --- | --- | --- |
| 美元 / 新台幣 | USD/TWD | 外匯 | TradingView | ExchangeRate-API |
| 美元 / 人民幣 | USD/CNY | 外匯 | TradingView | ExchangeRate-API |
| 美元 / 日圓 | USD/JPY | 外匯 | TradingView | ExchangeRate-API |
| 美元 / 泰銖 | USD/THB | 外匯 | TradingView | ExchangeRate-API |
| 20+年美債 ETF | TLT | 美債 ETF | TradingView | TradingView 即時連動 |
| 國際現貨黃金 | XAU/USD | 貴金屬現貨 | TradingView | Gold API |

備註：因 TradingView 對國債殖利率原始數據 (TVC:US20Y) 設有外嵌限制，本專案採用美債基準標的 NASDAQ:TLT (iShares 20+ Year Treasury Bond ETF)。

## 快速使用

### 本地直接執行
下載專案後，直接使用瀏覽器開啟 index.html 即可。

### 部署至 GitHub Pages
1. 將專案 Push 至 GitHub Repository。
2. 進入 Repository 的 Settings > Pages。
3. 在 Build and deployment > Branch 選擇 main 分支與 / (root) 目錄，點擊 Save。
4. 稍等約 1 分鐘即可透過 GitHub 給予的線上網址存取。

## 免責聲明

本專案提供之市場數據與圖表均來自第三方公開 API 與 TradingView 外部元件，報價可能存在延遲。本工具僅供個人研究與市場觀察使用，不構成任何形式的投資建議。

## 授權

MIT License
