# 國立臺中科技大學 商業智慧與多媒體互動實作專案 (BI & Interactive Applications)

> 國立臺中科技大學 資訊管理系 / 研究所 商業智慧課程課堂實作專案  
> 作者：[@arieslibra318](https://github.com/arieslibra318)  
> 線上體驗與展示：
> - ⚾ **《逆轉九局：魂之交鋒》8-Bit 像素棒球遊戲**：[`baseball_game.html`](baseball_game.html)
> - 📈 **《護國神山：台積電ADR (TSM) 守護戰》**：[線上試玩 (Netlify)](https://tsmc-adr-battle-arena.netlify.app)
> - 🐱 **貓咪日常健康與預防醫學指南 PPT**：[網頁簡報展示](https://arieslibra318.github.io/20261007-bi-practice/cat-healthcare-ppt/)
> - 📊 **台中市外送員交通事故數據分析儀表板**：[`dashboard.html`](dashboard.html)

---

## 專案一：⚾《逆轉九局：魂之交鋒》8-Bit 像素棒球節奏遊戲

本專案為一款重現 1980 年代紅白機情懷的 **8-Bit 像素風棒球 QTE 節奏打擊網頁遊戲**。玩家扮演在第 9 局下半絕境中登場的關鍵打者，需抓準球路時機揮棒，啟動逆轉勝的史詩動畫！

### 核心特色
1. **三階段動態球路與高精度 QTE 判定系統**：
   - **Stage 1 (滿壘落後一分)**：直球對決，揮出逆轉清壘二壘打（判定寬度 240ms）。
   - **Stage 2 (落後一分僵局)**：變速球與外角滑球，精準打擊追平比分（判定寬度 160ms）。
   - **Stage 3 (落後三分滿壘生死局)**：極限指叉球，抓準紅心擊出「再見滿貫全壘打 (Walk-off Grand Slam)」（判定寬度 110ms）。
2. **多媒體過場劇院 (Cinematic Cutscenes)**：
   - 整合 3 組精緻 8-Bit 動態過場影片（1080p / 7秒）：
     - `baseball_8bit_stage1_female_7s.mp4`：3:2 滿壘逆轉安打過場，清脆擊球音效與清壘跑壘。
     - `baseball_8bit_stage2_female_7s.mp4`：4:3 關鍵二壘安打過場（白色打擊手套、全螢幕像素卡片）。
     - `baseball_8bit_stage3_grandslam_7s.mp4`：7:5 再見滿貫全壘打過場（左上角即時記分板 HUD 與煙火歡呼）。
   - 內建高燃女聲熱血台詞語音與「鏘！！」、「轟！！」清脆金屬球棒打擊音效。
3. **原生 Web Audio API 復古合成音效**：
   - 零外部音效檔依賴，瀏覽器動態合成投球風聲、揮棒落空低鳴、完美擊球音與勝利號角。
4. **完整企劃書與 10 大問題 RCA 修正報告**：
   - 完整記錄遊戲系統架構、影音流水線生成、字幕版型調優、字型疊代與歷程覆盤：
     - Markdown 完整企劃：[`baseball_game_proposal.md`](baseball_game_proposal.md)
     - Word 報告版：[`棒球遊戲企劃書_逆轉九局魂之交鋒.docx`](棒球遊戲企劃書_逆轉九局魂之交鋒.docx) / [`baseball_game_proposal.docx`](baseball_game_proposal.docx)

---

## 專案二：📈《護國神山：台積電ADR (TSM) 守護戰》 Cyber Trading Arena

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
.
├── QTE棒球遊戲/                           # ⚾ 獨立部署資料夾 (最外層 index.html + 影片，符合 GitHub Pages 指引)
│   ├── index.html                        # 棒球遊戲主程式
│   ├── assets/                           # 遊戲過場影片資源
│   ├── baseball_8bit_stage1_female_7s.mp4
│   ├── baseball_8bit_stage2_female_7s.mp4
│   └── baseball_8bit_stage3_grandslam_7s.mp4
├── baseball_game.html                     # ⚾ 8-Bit 像素棒球遊戲主程式
├── baseball_8bit_stage1_female_7s.mp4    # 關卡一：3:2 滿壘逆轉安打過場影片
├── baseball_8bit_stage2_female_7s.mp4    # 關卡二：4:3 追平二壘安打過場影片
├── baseball_8bit_stage3_grandslam_7s.mp4 # 關卡三：7:5 再見滿貫全壘打過場影片
├── baseball_game_proposal.md             # 棒球遊戲完整企劃書與 10 大問題 RCA 覆盤 (Markdown)
├── 棒球遊戲企劃書_逆轉九局魂之交鋒.docx     # 棒球遊戲企劃書 Word 專業排版檔
├── baseball_game_proposal.docx            # 棒球遊戲企劃書 Word 檔案 (ASCII 名稱相容)
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
- `baseball_game.html` 暢玩 8-Bit 棒球遊戲
- `index.html` 暢玩台積電 ADR 守護戰

### 方法二：透過本機 HTTP 伺服器
```bash
# 使用 Python 內建伺服器
python -m http.server 8000

# 或使用 Node.js npx serve
npx serve .
```
開啟瀏覽器前往 `http://localhost:8000/baseball_game.html` 或 `http://localhost:8000` 即可。

---

## 技術棧 (Tech Stack)

* **Core**: Vanilla JavaScript (ES6+), HTML5 Canvas 2D / 3D, HTML5 Video API
* **Styling**: Tailwind CSS CDN, Retro 8-Bit Pixel Art CSS, Cyberpunk Dark UI Design
* **Audio**: Web Audio API (免載入外部音訊套件，原生振盪器合成音頻)
* **Media AI**: Seedance & 8-Bit Pixel Art Video Generation Pipeline
* **Deployment**: GitHub Pages / Netlify
