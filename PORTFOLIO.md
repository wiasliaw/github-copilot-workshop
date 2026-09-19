# 待辦清單 Web App

這是一個在 GitHub Copilot 實戰工作坊中完成的待辦清單 Web App。專案從基本的待辦事項管理開始，逐步加入主題切換、篩選、批次清除與使用者偏好保存，並透過 GitHub issue 與 Pull Request 流程處理實際需求與問題。

## 線上展示

[開啟 GitHub Pages](https://wiasliaw.github.io/github-copilot-workshop/)

> 請將上方網址中的帳號與 repo 名稱替換成實際的 GitHub Pages 網址。

## 功能

- 新增待辦事項，會忽略空白或只有空格的輸入。
- 使用核取方塊標記完成，完成項目會顯示刪除線並淡化。
- 刪除單筆待辦事項。
- 顯示整體清單中的未完成項目數量。
- 清單為空或目前篩選結果為空時，顯示對應的提示文字。
- 使用 `localStorage` 保存待辦資料，重新整理後仍可保留。
- 在淺色模式與深色模式之間切換。
- 記住使用者選擇的主題；從未手動選擇時，跟隨作業系統的 `prefers-color-scheme` 設定。
- 依「全部」、「未完成」或「已完成」篩選待辦事項。
- 保存篩選條件，重新整理後維持上次選擇；無效值會安全回退到「全部」。
- 在有已完成項目時批次清除所有已完成事項，並在刪除前顯示確認對話框。
- 支援響應式版面，可在手機螢幕上使用。

## 技術

- 使用純 HTML、CSS 與原生 JavaScript。
- 不使用任何框架、套件或外部 CDN。
- 使用 CSS 變數管理介面配色與淺色／深色主題。
- 使用瀏覽器原生 `localStorage` 保存待辦資料、主題偏好與篩選條件。
- 使用語意化 HTML、原生表單控制項與 ARIA 標籤支援基本的可及性需求。

## 開發方式

- 使用 GitHub Copilot Agent Mode，從需求開始建立待辦清單的 HTML、CSS 與 JavaScript，並透過瀏覽器互動測試驗證功能。
- 使用 MCP 連接 Microsoft Learn，查詢 `prefers-color-scheme` 與深色模式色彩對比的官方文件，作為主題與無障礙檢查的參考。
- 使用 `.github/prompts/fix-issue.prompt.md` 定義 issue 處理流程，依序完成 issue 摘要、提出計畫並等待確認、建立修復分支、修改、驗證、提交、推送與建立 Pull Request。
- 透過 GitHub issues 與 Pull Requests 追蹤篩選持久化、空篩選提示與批次清除等需求，並在合併前完成瀏覽器驗證。

## 我學到什麼

- Agent Mode 適合處理有明確需求、需要同時讀取與修改多個檔案的開發任務。
- 先建立清楚的專案規範與 prompt，可以讓後續修改更一致，也能降低不必要的重構。
- 使用 MCP 查詢官方文件，可以在實作功能時同步確認平台 API 與無障礙建議。
- GitHub issue、分支、commit 與 Pull Request 能把需求、修改內容和驗證結果串成可追蹤的工作流程。
- 瀏覽器實際操作測試能補足語法檢查，及早發現重新整理、篩選與 `localStorage` 相關的行為問題。