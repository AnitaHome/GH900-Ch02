#  GitHub Wiki Labs
GitHub Wiki 是 GitHub 為每個儲存庫（Repository）提供的內建文件系統。如果 README.md 是產品的「門面」，那麼 Wiki 就是產品的「完整操作手冊」。
必須是 Public 的 Repository 才可以使用 Wiki
Repository > Settings > Features，勾選 Wikis

<img width="445" height="226" alt="螢幕擷取畫面 2026-02-23 223839" src="https://github.com/user-attachments/assets/7a6d93a3-0b38-48b7-b107-0885c24f9d2c" />

## 實驗目標
- 啟用並設定專案 Wiki。
- 建立多層次的文件頁面。
- 實作「自定義側邊欄」與「頁尾」。
- 進階： 使用 Git 在本地端克隆並編輯 Wiki。

## Lab 1：啟動與第一頁
**目標**： 在專案中開啟 Wiki 功能並建立門面。
1. 開啟功能： 進入 GitHub 儲存庫設定 (Settings)，向下捲動到 Features 區塊，確保 Wikis 已勾選。
2. 建立首頁： 點擊上方選單的 Wiki 標籤，點擊 Create the first page。
3. 編輯內容： * 標題預設為 Home。
> - 在內文輸入專案簡介（例如：這是 GH900-Ch02 的官方文件庫）。
> - 使用 Markdown 語法（例如：# 歡迎來到專案手冊）。
> - 存檔： 點擊 Save Page。

## Lab 2：建立知識庫架構
**目標**： 建立多個分頁並練習內部連結。
1. 新增頁面： 點擊右上角的 New Page。
2. 命名規範： 建立以下三個頁面（注意頁面檔名建議使用英文）：
> - Installation (環境設定)
> - Usage (使用說明)
> - API-Reference (API 參考)
3. 跨頁面連結： 在 Home 頁面中使用 [[頁面標題]] 語法建立連結：
> - 範例：請參考我們的 [[Installation]] 來開始安裝。

## Lab 3：打造專業導覽列 (_Sidebar)
目標： 讓 Wiki 右側顯示一致的目錄，而不是雜亂的頁面清單。
1. 新增側邊欄： 點擊 Add a custom sidebar（在右下角）。
2. 編輯內容： 檔案名稱必須是 _Sidebar。
3. 設計目錄： 請複製以下內容：
```
### 📚 課程大綱
* [[首頁|Home]]
* **開始使用**
  * [[環境設定|Installation]]
  * [[API參考|API‐Reference]] 
* **核心功能**
  * [[Usage]]
---
### 🆘 幫助
* [回專案主頁](https://github.com/AnitaHome/GH900-Ch02)
```
4. 存檔： 現在每一頁的右側都會出現這個精美的導覽列。
## Lab 4：進階 - 本地端 Git 編輯
**目標**： 像改程式碼一樣改文件，支援批次編輯。
1. 取得 Wiki 位址： 在 Wiki 頁面右側找到 Clone URL。
2. Clone 到電腦：
```
# 以你的專案為例
git clone [https://github.com/AnitaHome/GH900-Ch02.wiki.git](https://github.com/AnitaHome/GH900-Ch02.wiki.git)
cd GH900-Ch02.wiki
```
3. 批次編輯： 使用 VS Code 開啟資料夾。你可以直接新增 .md 檔案或修改圖片。推送到雲端：git add .
```
git commit -m "docs: 更新導覽列與課程大綱"
git push origin master
```
## Lab 5：頁尾與視覺優化 (_Footer)
**目標**： 加入版權宣告或頁面結尾資訊。
1. 新增頁尾： 點擊 Wiki 右下角的 Add a custom footer。
2. 內容範例：
```
---
© 2026 AnitaHome GH900-Ch02 | 由 [Gemini](https://google.com) 驅動支援
```
3. 存檔： 所有頁面下方都會自動出現這行字。

### 💡 小撇步 
- 別名連結： 語法為 [[顯示文字|實際頁面名稱]]。
- 權限控制： 在 Settings 中可以勾選 "Restrict editing to collaborators only"，防止一般訪客修改你的 Wiki。
- Emoji： 多使用 Emoji（如 🚀, 📖, ⚠️）能大幅提升手冊的可讀性。
