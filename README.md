# 龍骨佈局計算器 · Joist Layout Calculator

戶外地板龍骨（joist）位置計算工具：依場地長度、地板長度、龍骨闊度與最大間距，計算每條龍骨的中心 / 左 / 右位置，並標示靠近板端接縫的龍骨；可匯出 CSV。

A joist-layout calculator for outdoor flooring: given site length, board length, joist width, and max spacing, it computes each joist's center / left / right position, highlights joints near board ends, and exports CSV.

## 使用方法 · How to use
1. 輸入參數（毫米）：場地長度、地板長度、龍骨闊度、最大間距、邊緣偏移、板間隙。
2. 按「Calculate」生成龍骨位置表。
3. 按「Copy CSV」複製結果，便於匯入試算表或工地紀錄。

1. Enter parameters (mm): site length, board length, joist width, max spacing, edge offset, board gap.
2. Press Calculate to generate the joist position table.
3. Press Copy CSV to export results.

## 計算公式 · Formula
- 每段長度 = 地板長度 ÷ ⌈地板長度 ÷ 最大間距⌉
- 龍骨中心 = 每段長度 × k + 邊緣偏移 + m × (地板長度 + 板間隙)
- 龍骨左緣 = 中心 − 龍骨闊度 ÷ 2；右緣 = 中心 + 龍骨闊度 ÷ 2
- 靠近板端（board end）的龍骨以 ★ 標示

## 特性 · Notes
- 手機優先（375px），系統字型，高對比，戶外強光可讀。
- 純單一 `index.html`，無外部依賴、無建置步驟。
- CSV 匯出便於工地紀錄與試算表整合。

## 本套件成員 · Part of the Jupiterlaw calculator suite
- [flooring-calculator](https://github.com/Jupiterlaw/flooring-calculator) — 地板材料
- [ourdoor_flooring_material_calculator](https://github.com/Jupiterlaw/ourdoor_flooring_material_calculator) — 戶外木地板 + 面通/底通/鋁角
- [joist_calculater](https://github.com/Jupiterlaw/joist_calculater) — 本工具（龍骨佈局）

© Jupiter's Design Limited
