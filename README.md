# 國立臺中科技大學 商業智慧與多媒體互動實作專案 (BI & Interactive Applications)

> 作者：[@arieslibra318](https://github.com/arieslibra318)  
> 線上體驗與展示：
> - 📈 **《護國神山：台積電ADR (TSM) 守護戰》**：[線上試玩 (Netlify)](https://tsmc-adr-battle-arena.netlify.app)
> - 🐱 **貓咪日常健康與預防醫學指南 PPT**：[網頁簡報展示](https://arieslibra318.github.io/20261007-bi-practice/cat-healthcare-ppt/)
> - 📊 **台中市外送員交通事故數據分析儀表板**：[`dashboard.html`](dashboard.html)

---

## 專案一：📈《護國神山：台積電ADR (TSM) 守護戰》 Cyber Trading Arena

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

## 專案目錄結構 (Project Structure)

```
├── index.html                             # 📈 台積電 ADR 守護戰首頁 / 完整對戰遊戲入口
├── tsmc_battle_game.html                  # 遊戲原始獨立檔案
├── dashboard.html                         # 📊 台中市外送員交通事故數據分析儀表板
├── cat-healthcare-ppt/                    # 🐱 貓咪日常健康與預防醫學指南網頁 PPT
└── README.md                              # 專案說明文件
```

---

## 快速啟動 (Quick Start)

本專案所有遊戲與頁面皆為零外部重型套件依賴的純前端 Single Page Application (SPA)，支援任意現代瀏覽器：

### 方法一：直接本機開啟
直接以瀏覽器雙擊點開：
- `index.html` 暢玩台積電 ADR 守護戰

### 方法二：透過本機 HTTP 伺服器
```bash
# 使用 Python 內建伺服器
python -m http.server 8000

# 或使用 Node.js npx serve
npx serve .

---

## 技術棧 (Tech Stack)

* **Core**: Vanilla JavaScript (ES6+), HTML5 Canvas 2D / 3D, HTML5 Video API
* **Styling**: Tailwind CSS CDN, Retro 8-Bit Pixel Art CSS, Cyberpunk Dark UI Design
* **Audio**: Web Audio API (免載入外部音訊套件，原生振盪器合成音頻)
* **Deployment**: GitHub Pages / Netlify
