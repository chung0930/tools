---
title: "豬皮專業NAS & Baycarchat 專案文檔"
author: "602班 開發者"
date: 2026-08-25
tags: [Termux, FastAPI, Apps Script, RWD]
---

<div align="center">
  <img src="https://img.shields.io/badge/Status-Active-brightgreen.svg" alt="Status">
  <img src="https://img.shields.io/badge/Platform-Termux-black.svg" alt="Termux">
  <img src="https://img.shields.io/badge/Frontend-HTML%2FJS-orange.svg" alt="Frontend">
</div>

# 🚀 豬皮專業NAS & Baycarchat 專案總覽

這是一份整合了**前端自適應網頁**、**後端 Python API** 以及 **Google Apps Script** 的開發與維護文檔。本系統主要依賴舊手機進行本地伺服器託管。

> [!IMPORTANT]
> **前端開發規範：**
> 所有撰寫的前端 HTML 與後端 Apps Script 專案的 HTML 都**必須做到自適應比例 (RWD)**。HTML 檔案將採用嵌入方式，不直接放在主專案目錄中。程式碼在提交前請再三檢查！

---

## 🛠️ 開發與生活待辦事項 (Task Lists)

日常專案維護、3C 設備測試以及個人行程清單：

- [x] **前端 UI 優化**：完成 Baycarchat 的 HTML 嵌入與響應式排版。
- [x] **DIY 藍牙喇叭測試**：使用 _808 Dreams_ 與 _Aqua Drop_ 測試下潛與被動輻射器氣密性。
- [ ] **Minecraft Bedrock 模組**：打包自定義 Behavior Pack 與 Resource Pack，並加入音樂模組。
- [ ] **Project Sekai (日服)**：執行版本更新與裝置效能測試。
- [x] **行程準備**：完成三灣鄉頂三天兩夜露營裝備確認，以及頭份國中新生報到準備。

---

## 💻 程式碼區塊 (Code Blocks & Syntax Highlighting)

### 1. Termux 伺服器啟動指令
*(註：Termux 指令區塊已依規範排除 `#` 註釋)*

```bash
pkg update -y
pkg install python -y
pip install fastapi uvicorn
uvicorn main:app --host 0.0.0.0 --port 8000
