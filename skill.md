# BitMart PM Workflow Skill

## 適用場景
當任務涉及以下任一情境時觸發本 Skill：
- 撰寫或更新 PRD / Feature Spec
- 競品分析（OKX / Bybit / Bitget / Binance / Gate.io）
- Sprint OKR 規劃或 Roadmap 排序
- Figma 原型 + HTML Prototype 產出
- Stakeholder 溝通文件

---

## 產品線上下文

**負責產品線：** Copy Trading｜Futures Grid｜Futures DCA｜Spot DCA｜｜Spot Grid ｜AI Hub ｜ Signal Trading

**競品追蹤維度：**
| 維度 | 關注點 |
|---|---|
| 網格交易 | 參數設計、安全係數、保證金公式 |
| 跟單交易 | 策略展示、分享海報、帶單員機制 |
| AI Skill | 入口設計、策略推薦邏輯、Hub 架構 |
| DCA交易 | 參數設計、安全係數、保證金公式 |
**當前 Sprint（Q2 2026）：**
1. Futures Martingale — P0 must-ship，4/30 deadline / dev-complete，web-only
2. Futures DCA —
3. Spot Grid
4. AI Strategy
5. Spot DCA


---

## 工作流程定義

### Step 0：任務分類
收到需求後，先判斷類型：
- `PRD` → 走 SDD 前置流程
- `競品分析` → 走競品框架
- `OKR/Roadmap` → 走優先級框架
- `原型/UI` → 先 fetch BMDS SKILL.md

### Step 1：SDD 前置（PRD 類必須）
輸出 PRD 正文前，強制先完成三步：
1. **Requirements**：What（要做什麼）+ Why（為什麼做，對應哪個用戶痛點）
2. **Spec**：欄位定義 / 條件邊界 / 輸入輸出 / 錯誤處理
3. **Tasks**：拆解到可排入 Sprint 的粒度

### Step 2：PRD 正文結構
```
# [功能名稱] PRD

## 1. 背景與目標
用戶 + 場景 + 痛點（1 段話）

## 2. 成功指標
可量化指標（例：首周啟動率 > 15%）

## 3. 功能描述
### 3.1 核心流程
### 3.2 欄位 / 狀態定義
### 3.3 邊界條件 / 錯誤處理

## 4. 風險與機會成本
- 風險：[技術/業務/合規]
- 機會成本：不做這個 = 損失什麼

## 5. 依賴項
- 前端 / 後端 / 設計 / 合規
- 外部依賴（第三方 API、其他產品線）

## 6. 版本記錄
| 版本 | 日期 | 變更說明 |
```

### Step 3：輸出格式規範
- Lark 相容：Markdown 表格 + 清單，避免複雜嵌套
- 數字先行：指標直接寫數值，不用「顯著提升」這類詞
- 繁體中文正文，技術術語保留英文

---

## 原型工作流（UI/Prototype 類）

```
1. fetch BMDS SKILL.md
   → https://github.com/ma-ching-tse/BMDS/blob/main/bmds-skill-v2/SKILL.md

2. fetch Agile PM Workflow SKILL.md
   → https://github.com/chyxin071-sys/Agile-PM-Workflow/blob/main/agile-pm-workflow_skill/SKILL.md

3. 產出 HTML prototype（desktop-first，≥1024px）

4. 轉 Figma frame（透過 Figma MCP）
   → 讀取現有 frame 位置（get_metadata）
   → offset 新 frame 430–460px
   → 載入 Inter 字體四個 style 後再建文字
```

---

## 競品分析框架

```
維度：功能完整度 / UX 流程 / 參數設計 / 數據展示 / 分享/社交機制
輸出：Gap Analysis 表格（我方現狀 vs 競品最佳實踐 vs 建議方向）
```

---

## 常用參照

| 資源 | 用途 |
|---|---|
| BMDS SKILL.md | UI/原型設計規範 |
| Agile PM Workflow | PRD+原型迭代流程 |
| BitMart Figma（KHfhEaTw6XRufePiXXeopv） | Futures DCA v1 主文件 |
| Lark CSV Pipeline | 最低摩擦數據基礎設施 |
| Make.com | 自動化優先工具 |

