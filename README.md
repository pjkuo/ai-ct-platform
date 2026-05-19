# 🧠 AI 賦能運算思維教學平台
### Think-Then-Verify · AI-Empowered Computational Thinking Platform

> 基於郭博仁（2026）大樣本準實驗研究（N = 200）的整合式教學工具
> Implementation of Kuo, P.-J. (2026) — *Performance Evaluation of Human–Machine Collaboration in Smart Agriculture / MDPI Engineering Proceedings*

---

## 📖 一、平台簡介

本平台將論文所驗證之「先思考、後驗證」（Think-Then-Verify）四階段教學模式，整合為**單一網頁應用**，無須後端、無須安裝、可直接部署於 GitHub Pages。

| 階段 | 模組名稱 | 對應論文章節 | 教學目標 |
|:---:|:---|:---|:---|
| **01** | 心智圖 → IPO 結構分解 | §3.3 第一階段 | 問題分解、模式辨識 |
| **02** | AI 賦能驗證與程式生成 | §3.3 第二階段 | 演算法理解、除錯能力 |
| **03** | 影音教學腳本創作 | §3.3 第三階段 | 4C 素養：溝通與創造力 |
| **04** | CT + 4C 雙量表自評 | §3.4 研究工具 | 反思評量、學習遷移 |
| ★ | 教師評量後臺 | §4 研究結果分析 | 群體統計、CSV 匯出 |

---

## ✨ 二、核心特色

- ✅ **單檔部署**：整個平台僅一個 `index.html`，無需建置流程
- ✅ **完整量表**：CT 16 題 + 4C 12 題，與論文工具 1 : 1 對應（α = .892–.901）
- ✅ **學生 / 教師雙模式**：右上角一鍵切換
- ✅ **本機資料儲存**：使用 `localStorage`，學生資料完全留在使用者端
- ✅ **資料匯出**：教師可一鍵匯出 **CSV**（Excel/SPSS 可直接讀取）或 **JSON** 備份
- ✅ **示範資料**：教師可載入 20 筆模擬資料（前/後測各 10 筆）展示後臺功能
- ✅ **個人化儀表板**：學生提交評量後產生雷達圖與分數報告
- ✅ **離線 AI 模擬**：AI 程式碼生成模組為論文 Grok + DeepSeek 雙核心架構之離線示範
- ✅ **編輯式學術美感**：Noto Serif TC 標題、編輯版面設計，符合學術發表氣質
- ✅ **可列印**：所有區塊已加上 `@media print` 樣式，方便老師備課列印
- ✅ **行動裝置適配**：響應式設計，平板手機皆可順暢操作

---

## 🚀 三、快速部署到 GitHub

### 方法 A：GitHub Pages（推薦，可線上分享）

```bash
# 1. 建立新的 GitHub repository（例如：ai-ct-platform）
# 2. 將 index.html 與 README.md 上傳至 main 分支
# 3. 進入 Settings → Pages → Source 選擇 "main / root"
# 4. 等待約 1 分鐘，網址 https://你的帳號.github.io/ai-ct-platform 即可使用
```

### 方法 B：直接開啟本機檔案

```
雙擊 index.html 即可在瀏覽器中執行
（無需任何伺服器或建置步驟）
```

### 方法 C：嵌入學校 LMS（Moodle / Canvas / Tronclass）

```html
<!-- 於 LMS 中新增 HTML 區塊，貼上以下 iframe -->
<iframe src="https://你的網址/index.html"
        width="100%" height="900px"
        style="border:none;border-radius:8px"></iframe>
```

---

## 📊 四、論文資料對應對照表

| 平台元件 | 論文出處 | 對應數據 |
|:---|:---|:---|
| 首頁理論框架 | §1.2 圖 1 | 建構主義 × 認知負荷 × 自我效能 |
| 四階段流程 | §3.3 | 70% 學生推理 + 30% AI 驗證 |
| IPO 分解模組 | §3.3 第一階段 | 對應演算法理解 d = 0.95 |
| CT 量表（16 題） | §3.4 (一) / 附錄 A 表 3 | α = .892–.901 |
| 4C 量表（12 題） | §3.4 (二) | α = .876 |
| 元認知反思題 | §3.4 (三) | 主題分析法 91.5% 回應 |
| 教師後台統計 | §4 結果分析 | 配對 t 檢定 / ANCOVA |

---

## 👨‍🏫 五、教師使用指南

### 5.1 課前準備

1. 將平台部署至 GitHub Pages 或學校伺服器
2. 將網址公告給學生（建議使用 QR code 投影）
3. 在第一堂課示範「心智圖 → IPO → AI 驗證」完整流程

### 5.2 課堂操作（建議節奏，對應論文 12 週設計）

| 週次 | 階段 | 平台模組 | 預期時數 |
|:---:|:---:|:---|:---:|
| W1 | 前測 | 04 能力評量（前測模式） | 30 min |
| W2-3 | 01 | 心智圖 → IPO 練習 | 4 hr |
| W4-7 | 02 | AI 驗證、程式除錯 | 8 hr |
| W8-10 | 03 | 影音腳本與專案 | 6 hr |
| W11-12 | 04 | 後測 + 反思 | 30 min |

### 5.3 資料蒐集流程

```
學生提交評量 → 資料存於該學生瀏覽器之 localStorage
              → 切換為教師模式 → 查看「所有提交紀錄」
              → 點擊「匯出 CSV」→ 用 Excel / SPSS / R 分析
```

> ⚠️ 重要：因採 `localStorage`，**每台機器資料獨立**。若要收集全班資料，建議：
> - 學生個別匯出後上傳至雲端（Google Drive / Classroom）
> - 或請學生使用同一台教室電腦輪流作答
> - 或將平台改為連接後端（請見「進階擴充」）

### 5.4 CSV 欄位說明（與 SPSS / R 對接）

| 欄位 | 說明 | 統計用途 |
|:---|:---|:---|
| `學號`、`姓名`、`階段` | 配對識別 | 配對樣本 t 檢定 |
| `CT_整體` | 16 題平均 | 主要應變項 |
| `CT_問題分解 / 流程邏輯 / 演算法 / 除錯` | 4 子向度 | 子向度分析 |
| `4C_整體` 與 4 子向度 | 4C 各向度 | 多變量分析 |
| `提交時間` | ISO 8601 | 時序分析 |

---

## 🎓 六、學生使用指南

1. **首頁**：閱讀「先思考、後驗證」教學理念
2. **模組 01**：先**獨立思考**，將你的問題拆解為 INPUT / PROCESS / OUTPUT，再點「轉換」
3. **模組 02**：把 IPO 帶入 → 觀察 AI 生成程式碼框架 → **逐項驗證、找錯、優化**
4. **模組 03**：把專案轉換為三幕式影音腳本
5. **模組 04**：誠實作答 28 題自評量表，獲得能力雷達圖

> 💡 **關鍵原則**：AI 是你的「驗證夥伴」而非「答案機器」。你要做的不是抄寫 AI 的答案，而是**判斷它對不對**。

---

## 🔧 七、進階擴充建議

### 7.1 串接真實 AI（Grok / DeepSeek / Gemini / Claude）

目前平台的「AI 生成」為離線模擬。如需串接真實 API：

```javascript
// 於 index.html 內找到 generateCode() 函式，替換為：
async function generateCode() {
  const response = await fetch('https://api.x.ai/v1/chat/completions', {
    method: 'POST',
    headers: {
      'Authorization': 'Bearer YOUR_API_KEY',
      'Content-Type': 'application/json'
    },
    body: JSON.stringify({
      model: 'grok-2-latest',
      messages: [{ role: 'user', content: buildPrompt() }]
    })
  });
  const data = await response.json();
  // 顯示結果
}
```

⚠️ 安全性提醒：API 金鑰**不可**直接寫入前端原始碼。建議：
- 改用 Cloudflare Workers / Vercel Functions 作為 API proxy
- 或讓學生於 Step 1 介面自行輸入個人金鑰（暫存於 sessionStorage）

### 7.2 後端整合（蒐集全班資料）

若需集中蒐集多位學生資料，可後端化：

- **Firebase Firestore**（最快，免費額度足夠 200 人課程）
- **Supabase**（含表格化資料庫，類 PostgreSQL）
- **Google Sheets API**（學校環境最易接受）

---

## 📜 八、引用與授權

### 8.1 學術引用（APA 7th）

```
郭博仁（2026）。整合「先思考、後驗證」教學模式之 AI 賦能運算思維教學成效：
   大樣本準實驗研究。MDPI Engineering Proceedings。

Kuo, P.-J. (2026). The Effectiveness of AI-Empowered Computational Thinking
   Instruction Integrated with a Think-Then-Verify Pedagogical Model:
   A Large-Sample Quasi-Experimental Study. MDPI Engineering Proceedings.
```

### 8.2 平台引用

```
郭博仁（2026）。AI 賦能運算思維教學平台（Think-Then-Verify Edition）
   [Computer software]. https://github.com/你的帳號/ai-ct-platform
```

### 8.3 授權條款

- 程式碼：MIT License（自由修改、教學使用）
- 量表內容：依論文授權，學術與教學使用免費，商業使用請聯繫作者
- 字型：Noto Serif TC / Noto Sans TC 採 SIL Open Font License

---

## 📮 九、作者資訊

**郭博仁 Kuo, Po-Jen**
- 中華電信數據分公司 資深工程師
- 國立屏東科技大學 資訊管理系 兼任講師
- 📧 pjkuo@npust.edu.tw

研究專長：網際網路與企業網路、雲端運算、IoT、巨量資料分析、AI 賦能教學設計

---

## 📝 十、更新日誌

### v1.0 (2026-05)
- 🎉 首次發布
- 整合心智圖→IPO、IPO 程式分析器、學生實作平台三大原型
- 完整實作論文之 CT（16 題）與 4C（12 題）量表
- 教師後台含群體統計、CSV / JSON 匯出、前後測比較圖
- 編輯式學術風格設計，列印友善

---

<div align="center">

**「先思考、後驗證」**
Think first, then verify with AI.

不是 AI 取代人類，而是 AI 增強人類認知。

</div>
