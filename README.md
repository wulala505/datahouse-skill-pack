# 🏢 Data House AI 顧問團隊 Skill Pack

> 專為 Data House 數據顧問服務設計的多角色 Claude Code Skill Pack（Cowork Plugin 格式），
> 涵蓋從業務開發、數據策略、技術建置到客戶維護的完整顧問工作流程。

---

## 📖 這是什麼？

這套 Skill Pack 把 Claude Code 變成 Data House 的**虛擬顧問團隊**。
每個 Skill 就是一個有明確專業定位、工作流程和輸出格式的 AI 成員。
根據當前任務階段，自動切換到最合適的角色。

採用 **Cowork Plugin** 格式，放在 `.claude/skills/` 目錄下，
可直接作為 Claude Code 專案外掛使用。

---

## 👥 10 個角色

| 角色 | Skill 名稱 | 核心職責 | 何時使用 |
|------|-----------|---------|---------|
| 🎯 專案總監 | `project-director` | 任務分派、流程統籌 | 不知從何開始 / 多工統籌 |
| 📋 提案分析師 | `proposal-analyst` | 解析客戶需求、評估可行性 | 收到新詢問 / 業務開發 |
| 📊 數據策略師 | `data-strategist` | KPI 定義、追蹤策略規劃 | 專案啟動規劃階段 |
| 📣 MarTech 企劃 | `martech-planner` | 工具選型、整合方案設計 | 技術方案規劃 |
| 🖥️ 儀表板工程師 | `dashboard-builder` | Looker Studio 設計規格 | 儀表板建置 / 改版 |
| 🏷️ 追蹤工程師 | `tracking-engineer` | GA4 / GTM 設定規格 | 追蹤設定 / Debug |
| 📡 廣告整合師 | `ads-integrator` | 跨平台廣告數據整合 | 廣告數據彙整 |
| 📝 洞察報告師 | `insight-reporter` | 月報 / 數據洞察撰寫 | 報告交付 |
| 🔍 SEO/AEO 專員 | `seo-aeo-specialist` | 搜尋可見度優化 | 網站自然流量提升 |
| 🤝 客戶成功經理 | `client-success` | 客戶維護 / 升級銷售 | 定期 Review / 續約 |

---

## 🔄 常見工作流程

### 新客戶業務開發
```
① proposal-analyst  → 解析詢問需求、評估可行性
② data-strategist   → 規劃數據架構與 KPI 框架
③ martech-planner   → 設計工具整合方案
④ project-director  → 統整提案、規劃交付時程
```

### GA4 + 儀表板建置專案
```
① data-strategist    → 定義 KPI 與事件清單
② tracking-engineer  → GA4 事件規格 + GTM 設定
③ dashboard-builder  → Looker Studio 儀表板設計
④ insight-reporter   → 第一份報告交付
```

### 廣告數據整合專案
```
① ads-integrator     → 跨平台整合架構規劃
② dashboard-builder  → 整合儀表板設計
③ insight-reporter   → 廣告成效報告
```

### 月度維護服務
```
① insight-reporter   → 月報撰寫
② client-success     → 客戶溝通 + Review 規劃
③ project-director   → 下月優先項目統籌
```

### 網站搜尋優化
```
① seo-aeo-specialist → SEO + AEO 策略規劃
② tracking-engineer  → GSC + GA4 追蹤確認
③ insight-reporter   → 成效追蹤報告
```

---

## 🔌 MCP 整合建議

| MCP 服務 | 連結後可做什麼 | 相關 Skill |
|---------|-------------|-----------|
| Gmail | 直接讀取客戶詢問信件 | `proposal-analyst` |
| Google Calendar | 建立專案里程碑提醒 | `project-director` |
| Notion | 建立案件追蹤資料庫 | `project-director`, `client-success` |
| Google Drive | 讀取既有報告 / 規格文件 | `insight-reporter`, `dashboard-builder` |
| Slack | 推送報告摘要到頻道 | `insight-reporter`, `client-success` |

---

## 📁 檔案結構

```
.claude/
└── skills/
    ├── datahouse-consulting-team/
    │   └── SKILL.md          ← 主 Skill（團隊總覽與觸發規則）
    ├── project-director/SKILL.md
    ├── proposal-analyst/SKILL.md
    ├── data-strategist/SKILL.md
    ├── martech-planner/SKILL.md
    ├── dashboard-builder/SKILL.md
    ├── tracking-engineer/SKILL.md
    ├── ads-integrator/SKILL.md
    ├── insight-reporter/SKILL.md
    ├── seo-aeo-specialist/SKILL.md
    └── client-success/SKILL.md
```

---

## ⚙️ 安裝方式

### 方式一：Cowork Plugin（推薦）

將整個 `.claude/` 目錄複製到你的 Claude Code 專案根目錄：

```bash
cp -r .claude/ /your-project/
```

開啟 Claude Code，Skills 會自動載入。輸入任何 Data House 相關任務，Claude 會自動切換角色。

### 方式二：手動指定角色

```
請用 proposal-analyst 幫我分析這封客戶詢問信
用 insight-reporter 幫我寫本月報告，數據如下：...
```

---

## 🎯 設計原則

- **角色分工明確**：每個 Skill 只做自己的事
- **上下游銜接**：每個角色的輸出格式是下一個角色需要的輸入
- **可直接執行**：所有輸出都是「可以直接用」的格式，不是模糊建議
- **台灣語境優先**：針對台灣電商/中小企業生態優化
- **Cowork 原生格式**：符合 Claude Code Cowork Plugin 規範，即插即用

---

*Data House 疊塔好思股份有限公司 — datahouse.solutions*
