# Agent Guidelines

## Google Drive — Repository-specific Build Delivery (Required)

**所有 Codex／開發 Agent 必須遵守**：每個 GitHub Repository 有獨立交付資料夾 `Google Drive / AI Project/arethetypeswrong.github.io/`，名稱必須與 Repo 完全相同；AI Project folder ID: `1Yhfro6Ss5TSCXCVIZIHEu5h7V1gL8b27`。

1. **最新完整 Build 直接放專案資料夾根目錄**，包含版本化檔名的 ZIP／EXE 包、SHA-256 及必要的分片、還原腳本／使用說明；多平台最新版本可並存。不要在 AI Project 根目錄放任何 Build，也不要每次 Build 都建立版本資料夾。
2. **僅重要版本差異**（重要功能、架構、相容性、畫面里程碑）才在專案內建立 `vX.Y.Z-說明/` 子資料夾保存；一般舊版本非破壞性移入 `歷史封存/`，不可逕自刪除任何舊檔。
3. **先確認新版本完整，才能更換最新版本**：上傳後讀回 Google Drive 名稱、parent、大小及 checksum；只看到 SHA、缺少 ZIP 或缺一個分割檔的版本屬「不完整」，不得取代前一完整最新版。
4. 尚未實際編譯且驗證成功，不得宣稱已產出、已上傳或可執行。每次新開發推送 GitHub，正式 Build/發布的 GitHub Actions 優先 `workflow_dispatch` 或 `release: published`，避免每次推送 main 觸發高成本 Build。
5. 回報最新版本、Drive **專案資料夾連結**、檔案清單、checksum 和實測／上傳狀態；第一次成功 Build 才需建立專案資料夾。

**Coding agents (English):** Publish only the newest *complete and verified* build directly under `AI Project/arethetypeswrong.github.io/`. Preserve milestone versions in `vX.Y.Z-description/` only for material differences; archive routine older versions under `歷史封存/` without deleting them. Never promote incomplete uploads.
