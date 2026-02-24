# GH900-Ch02
這是 README.md 可以顯示 較短 的訊息，單一檔


# 📊 GitHub 研發文件生態系技術決策分析表

針對專案生命週期的不同階段與受眾需求，以下為 GitHub 四大核心文件工具的技術特性比對，供架構設計參考。

| 技術維度 | README.md | GitHub Wiki | GitHub Pages | GitHub Gists | 
| :--- | :--- | :--- | :--- | :--- | 
| **技術定位** | **專案索引 (Project Entry)** | **知識庫 (Knowledge Base)** | **部署平台 (Deployment Platform)** | **片段管理 (Snippet Management)** | 
| **主要場景** | 快速上手指南 (Getting Started) | 技術架構、API 詳細規範 | 形象官網、互動式 Demo | 報錯日誌分享、跨平台嵌入 | 
| **內容複雜度** | 扁平式 (Flat) | 分層導覽 (Hierarchical) | 網狀架構 (Site Structure) | 無結構化 (Unstructured) | 
| **擴充性** | 受限於 GitHub 渲染器 | 支援自定義側邊欄 | **極高** (支援自訂 CSS/JS/框架) | 極低 (固定樣式) | 
| **安全性控管** | 繼承儲存庫權限 | 支援協作者權限限制 | 公開部署 (除非使用 Enterprise) | 支援隱藏連結 (Secret Gists) | 
| **CI/CD 整合** | 無 | 支援 Git 同步 (但無 Actions) | **深度整合 (GitHub Actions)** | 可透過 API/CLI 操作 | 

### 🎯 決策建議

1. **內部開發流程紀錄**：優先選擇 **GitHub Wiki**，以維持文件與代碼的緊密關聯。

2. **對外品牌與產品展示**：建議部署 **GitHub Pages**，以獲得完整的 UI 控制權與優化的使用者體驗。

3. **臨時技術溝通**：使用 **GitHub Gists**，避免對核心儲存庫造成內容污染。

### 總結
* **README** 是書的封面。
* **Wiki** 是書的詳細章節。
* **Pages** 是專為這本書架設的專題官網。
* **Gist** 則是書中夾著的一張便利貼。

你目前在整理 Git 課程教材時，如果有某些**常用的設定檔片段**（例如特定的 `.gitignore` 模板），就很適合用 **Gist** 來存放並分享給學生！
