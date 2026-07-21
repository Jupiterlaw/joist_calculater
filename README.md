# Joist Layout Calculator (龍骨佈局計算器)

[![Calculator Suite](https://img.shields.io/badge/Calculator%20Suite-Joist%20Layout-38BDF8?style=flat-square)](https://github.com/Jupiterlaw/calculator-suite)

龍骨（Joist）佈局計算器 — 根據地板長度、最大間距與邊距，自動計算每條龍骨的準確位置。

> **現場第一線工具**：專為工地環境設計，大按鈕、大字體、高對比度，即使在陽光直射下也能清晰閱讀。

---

## 功能特色

- **龍骨位置計算** — 按等分規則自動計算每條龍骨的中心點、左邊緣與右邊緣位置
- **板接點標記** — 自動標記靠近板端接縫的龍骨（★ 標示），方便施工時注意
- **互動式表格** — 清晰顯示龍骨編號、所屬板號、分段號與位置數據
- **分段統計** — 即時顯示分段長度、最大間距、龍骨總數與板數
- **CSV 匯出** — 一鍵複製 CSV 格式數據，方便匯入 Excel 或其他工具
- **即時計算** — 開啟頁面即自動計算，修改參數後按 Calculate 更新結果

---

## 快速開始

### 直接在瀏覽器使用

1. 打開 [GitHub Pages 連結](https://jupiterlaw.github.io/joist_calculater/)（如有啟用）
2. 或直接下載 `index.html` 在瀏覽器開啟

### 本地使用

```bash
# 克隆倉庫
git clone https://github.com/Jupiterlaw/joist_calculater.git

# 直接在瀏覽器打開 index.html
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

**無需任何依賴、無需構建、無需後端。** 一個 HTML 檔案，打開即用。

---

## 使用說明

### 輸入參數

| 參數 | 說明 | 範例 |
|------|------|------|
| **Site Length (L)** | 施工場地總長度 (mm) | 9005 |
| **Board Length (B)** | 每塊地板長度 (mm) | 3000 |
| **Joist Width (W)** | 龍骨闊度 (mm) | 45 |
| **Max Spacing** | 最大允許間距 (mm) | 400 |
| **Edge Offset** | 龍骨離板端邊距 (mm) | 5 |
| **Board Gap** | 板與板之間隙 (mm) | 5 |

### 操作步驟

1. 在左側面板輸入所有參數
2. 按 **「▶ Calculate」** 按鈕
3. 右側表格顯示所有龍骨位置
4. 按 **「📋 Copy CSV」** 匯出數據

### 計算公式

| 項目 | 公式 |
|------|------|
| 分段數 | `ceil(地板長度 / 最大間距)` |
| 分段長度 | `地板長度 / 分段數` |
| 龍骨中心點 | `(分段長度 × k + 邊距) + m × (地板長度 + 板隙)` |
| 龍骨左邊緣 | `中心點 - 龍骨闊度 / 2` |
| 龍骨右邊緣 | `中心點 + 龍骨闊度 / 2` |

---

## 截圖

| 桌面版 | 手機版 |
|--------|--------|
| *(待添加)* | *(待添加)* |

---

## 瀏覽器支援

| Chrome | Firefox | Safari | Edge | Opera |
|--------|---------|--------|------|-------|
| ✅ 最新 | ✅ 最新 | ✅ 最新 | ✅ 最新 | ✅ 最新 |

亦支援 iOS Safari 及 Android Chrome 等行動瀏覽器。

---

## 開發資訊

### 專案結構

```
joist_calculater/
├── index.html    # 完整計算器（HTML + CSS + JS 單一檔案）
└── README.md     # 本文件
```

### 技術棧

- 純 HTML5 / CSS3 / JavaScript（ES6）
- CSS Custom Properties 設計系統
- 無外部執行時期依賴
- 響應式設計（375px 手機到寬螢幕桌面）

### 設計系統

本計算器是 **Calculator Suite** 的一部分，共享設計語言規範於 [UI-SYSTEM.md](https://github.com/Jupiterlaw/calculator-suite/blob/main/UI-SYSTEM.md)（跨專案文件）。

---

## 相關專案

| 計算器 | 說明 |
|--------|------|
| [Outdoor Flooring Calculator](https://github.com/Jupiterlaw/ourdoor_flooring_material_calculator) | 戶外木地板及面通材料計算（地板分段、等分規則、面通/底通/鋁角） |
| [Flooring Calculator](https://github.com/Jupiterlaw/flooring-calculator) | 地板材料面積計算器（多區域、損耗率、包裝計算） |

---

## 授權

本專案採用 MIT 授權條款 — 詳見 LICENSE 檔案（如適用）。

---

## 貢獻

歡迎提交 Issue 或 Pull Request。請參閱 [PR-GUIDELINES.md](https://github.com/Jupiterlaw/calculator-suite/blob/main/PR-GUIDELINES.md) 了解分支命名、提交規範與 PR 流程。