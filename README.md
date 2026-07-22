# Programming Thinking 逐章深度導讀

本篇為 YouTube 頻道 Visual Kernel《Programming Thinking》教學影片的逐章深度導讀。拆解變數、條件、串列、迴圈、函式、範疇、傳址、字典、遞迴等十一個 Python 核心主題，搭配十一張原創資訊圖，並附繁體中文字幕燒錄版影片，協助讀者理解程式設計思維的本質，回應 AI 時代是否還需要學程式設計。

🔗 **線上閱讀**：本 repo 已開啟 GitHub Pages，可直接開啟 `index.html` 對應的網址閱讀。

---

## 素材來源

- **原始影片**：[Programming Thinking](https://www.youtube.com/watch?v=KtBefDeECVU)（YouTube 頻道 Visual Kernel，約 4.41 萬訂閱者，2026-07-14 上線，時長 2:08:06）
- **中文化字幕燒錄版**：[Programming.Thinking_zh-TW_burned.mp4](https://github.com/lushinshang/Programming-Thinking/releases/download/mv/Programming.Thinking_zh-TW_burned.mp4)（本 repo Release 資產，已內嵌於頁面置頂播放器）
- **逐字稿**：透過 YouTube 字幕下載工具取得繁體中文逐字稿，作為導讀撰寫的原始依據

## 製作流程

1. **逐字稿處理**：下載並讀取影片繁體中文逐字稿全文（約 6,900 行 SRT），依原片 13 個章節時間軸（Intro、Variable、If & Else、List、For Loop、Range()、Double Loop、Function、Scope、Value vs. Reference、Dictionary、Recursion、Future）對照消化內容。
2. **深度導讀撰寫**：套用 `deep-guide` skill，以「痛點先行 → 靈魂拷問 → 機制解構 → 深層真相 → 落地價值」的敘事邏輯，逐章重新消化、原創撰寫導讀文字（非逐字稿翻譯或摘錄），並於文章前段加入摘要、結尾加入結論。
3. **資訊圖生成**：透過 Codex CLI 的 `image_gen` 工具，為每一章節各自產出一張原創資訊圖（共 11 張），每張皆包含桌面版（16:9）與手機版（9:16）兩種比例，確保行動裝置閱讀時圖片文字仍清晰可讀。
4. **HTML 排版**：套用 `md_to_html` skill 轉換為單一 standalone HTML 頁面，採用 Notion 風格的長文閱讀排版、淺色護眼底色、響應式圖片切換（`<picture>` + 媒體查詢）、圖片點擊放大燈箱（lightbox）等互動細節。
5. **影片嵌入與起源介紹**：於文章置頂處嵌入 HTML5 `<video>` 播放器，直接串流本 repo Release 中的繁體中文字幕燒錄版影片；並在導讀開頭補充原始 YouTube 影片的頻道、上線時間、觀看次數等背景資訊。
6. **驗證**：以 `python3 -m html.parser` 驗證 HTML 語法正確性；以 Playwright 分別截取桌面（1280px）與手機（390px）版面截圖，確認排版無跑版、無文字重疊、圖片比例正確切換。

## 目錄結構

```
.
├── index.html              # 逐章深度導讀網頁（GitHub Pages 進入點）
├── images/                 # 11 章節資訊圖，各含桌面版 (*.png) 與手機版 (*-mobile.png)
└── README.md                # 本檔案
```

## 章節對照

| 原片章節 | 導讀對應內容 |
|---|---|
| Intro | AI 時代為何仍需要程式設計思維 |
| Variable | 等號是動作而非等於，賦值的心智模型 |
| If & Else | 布林邏輯與 AND/OR 電路閘門類比 |
| List | 串列四大操作與參考本質的伏筆 |
| For Loop | 三種經典迴圈模式（加總／找最大／去重複） |
| Range() | 直接走訪 vs 索引走訪的取捨 |
| Double Loop | 獨立型與依賴型巢狀迴圈 |
| Function | 輸入輸出的沙盒模型 |
| Scope | 區域範疇與全域範疇的查找規則 |
| Value vs. Reference | 傳值與傳參考，堆疊與堆積記憶體 |
| Dictionary | 鍵值對映，讓查詢本身變得有意義 |
| Recursion | 遞迴的信心跳躍與呼叫堆疊 |

---

整理完成日期：2026-07-22
