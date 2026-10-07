# 《護國神山：台積電ADR (TSM) 守護戰》 Cyber Trading Arena

> 國立臺中科技大學 資訊管理系 / 研究所 商業智慧課程課堂實作專案  
> 線上試玩展示：[https://tsmc-adr-battle-arena.netlify.app](https://tsmc-adr-battle-arena.netlify.app)

---

## 專案簡介 (Introduction)

本專案是以**台灣半導體權值王「台積電 ADR (TSM)」美股即時行情為背景**所打造的 Web 卡牌對抗對決與即時走勢圖互動系統。

將金融市場交易、技術指標與卡牌 Roguelike 機制融合：
- **美股每股計價**：以台積電 ADR 真實波動情境為模擬標的，無台股 10% 漲跌停限制，體現國際資金流動。
- **即時 K 線渲染與縮放系統**：
  - 支援滑鼠滾輪自由放大/縮小（Zoom In / Out）歷史與即時 K 線走勢。
  - 支援滑鼠拖曳平移（Pan）及「一鍵回歸最新 (LIVE)」機制。
  - 即時計算成交量柱狀圖、技術均線與盤中震盪指標。
- **戰略卡牌攻防系統**：包含「突破進場」、「W底築底多單」、「止損保險支援」、「大單追繳」等多樣化策略卡牌。
- **賽博風格沉浸視效**：內建 3D 擬真地球節點旋轉渲染、霓虹戰術介面與 Web Audio API 原生音效。

---

## 專案架構 (Project Structure)

```
.
├── index.html            # 專案首頁 / 完整對戰遊戲入口 (包含完整 K 線引擎、卡牌系統與 3D 視覺)
├── tsmc_battle_game.html # 遊戲原始獨立檔案
├── dashboard.html        # 台中市外送員交通事故數據分析儀表板 (2022-2026)
├── wooldridge-cre-ppt/   # 📊 Wooldridge (2019) CRE 非平衡面板計量文獻導讀網頁 PPT
├── cat-healthcare-ppt/   # 🐱 貓咪日常健康與預防醫學指南網頁 PPT
└── README.md             # 專案說明文件
```

---

## 網頁簡報展示 (Interactive Web Slide Decks)

基於 `guizang-ppt-skill` 生成的單文件橫向翻頁高階雜誌風格 PPT：

1. **📊 Wooldridge (2019) 計量經濟學論文導讀 PPT**
   - **論文**: *Correlated random effects models with unbalanced panels* (*Journal of Econometrics*)
   - **線上展示**: [https://arieslibra318.github.io/20261007-bi-practice/wooldridge-cre-ppt/](https://arieslibra318.github.io/20261007-bi-practice/wooldridge-cre-ppt/)
   - **特點**: 12 頁學術深度剖析、Theorem 2.1 代數等價性推導、異方差 Probit 參數化、完全叢集穩健 Hausman 檢定、全配演講備忘稿（按 `P` 鍵開啟演講者雙屏視圖）。

2. **🐱 貓咪日常健康與預防醫學指南 PPT**
   - **主題**: 從演化天性到預防醫學的日常照護指南（風格 A · 森林墨）
   - **線上展示**: [https://arieslibra318.github.io/20261007-bi-practice/cat-healthcare-ppt/](https://arieslibra318.github.io/20261007-bi-practice/cat-healthcare-ppt/)
   - **特點**: 10 頁雜誌風格、FGS 痛覺表情量表五聯徵、雙軌流水線動效。


---

## 快速啟動 (Quick Start)

本專案為零外部套件依賴的純前端 Single Page Application (SPA)，支援任意現代瀏覽器：

### 方法一：直接本機開啟
直接雙擊點開 `index.html`，即可於 Chrome、Edge、Safari 或 Firefox 中暢玩。

### 方法二：透過本機 HTTP 伺服器
```bash
# 使用 Python 內建伺服器
python -m http.server 8000

# 或使用 Node.js npx serve
npx serve .
```
開啟瀏覽器前往 `http://localhost:8000` 即可。

---

## 技術棧 (Tech Stack)

* **Core**: Vanilla JavaScript (ES6+), HTML5 Canvas 2D / 3D
* **Styling**: Tailwind CSS CDN, Cyberpunk Dark UI Design
* **Audio**: Web Audio API (免載入外部音效檔，原生合成音頻)
* **Deployment**: Netlify / GitHub Pages
