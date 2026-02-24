
# 🌐 GitHub Pages 實作工作坊：從零打造專業網站

本指南將帶領你透過 6 個實作實驗（Labs），掌握 GitHub Pages 從基礎發佈到深度自定義的核心技術。無論是建立課程官網、個人作品集或技術文件，都能輕鬆上手。

---

## 🎯 課程目標
- 掌握 GitHub Pages 的靜態發佈流程。
- 學習 Jekyll 引擎與主題（Theme）的連動機制。
- 實作「內容與樣式分離」的網站管理（_config.yml）。
- 運用 HTML/CSS 強化網頁視覺排版。

---

## 🧪 Lab 1：Hello World - 啟動你的網站
**目標：** 了解 GitHub Pages 的基本發佈機制與網址結構。

1. **建立檔案：** 在儲存庫根目錄建立 `index.html`。
2. **編寫內容：**
   ```html
   <h1>歡迎來到我的 GitHub Pages！</h1>
   <p>這是我的第一個自動發佈網站。</p>
   ```
. **啟用服務：**  
   * 進入 **Settings** \-\> **Pages**。  
   * 在 **Build and deployment** \> **Branch** 選擇 main (或 master)。  
   * 點擊 **Save**。  
4. **驗證：** 等待約 1 分鐘，瀏覽 https://\<你的帳號\>.github.io/\<專案名\>/。

## **🧪 Lab 2：穿上新衣 \- 套用 Jekyll 主題**

**目標：** 啟動 Jekyll 引擎並套用專業的主題樣式。

1. **設定大腦：** 在根目錄建立 \_config.yml，輸入以下內容（注意冒號後要有空格）：
   ```
   theme: jekyll-theme-cayman  
   title: 我的課程網站  
   description: 歡迎來到實作頁面
   ```

3. **關鍵啟動步驟 (Front Matter)：** Jekyll 只會處理包含「開頭配置」的檔案。請將 index.html 修改為：
   ```
   ---  
   layout: default  
   ---  
   <h1>測試主題成功！</h1>  
   <p>現在你應該能看到深綠色的漸層橫幅了。</p>
   ```
 **原理：** layout: default 會呼叫主題的外殼，你不需要寫 \<html\> 或 \<body\> 標籤，它們會被自動注入。

## **🧪 Lab 3：自定義控制 \- 調整標題與按鈕**

**目標：** 透過設定檔控制網頁橫幅（Header）的內容。

1. **修改內容：** 編輯 \_config.yml，讓網站更有個性：
   ```
   theme: jekyll-theme-cayman  
   title: 🎓 Git 版本控新手村  
   description: 跟著 Anita 一起踏入 Git 的神奇世界吧！  
   github:  
     is\_project\_page: false \# 設為 false 可自訂或隱藏預設按鈕
   ```

3. **驗證：** 檢查網頁標題與瀏覽器標籤頁文字是否同步更新。

## **🧪 Lab 4：整潔管理 \- 使用 /docs 資料夾**

**目標：** 分離程式碼與文件，讓專案目錄井然有序。

1. **移動檔案：** 在儲存庫建立 docs/ 資料夾，將 index.html 與 \_config.yml 移入。  
2. **更改設定：**  
   * 進入 **Settings** \-\> **Pages**。  
   * 將 **Branch** 下方的資料夾選單從 /(root) 改為 /docs。  
   * 點擊 **Save**。  
3. **優點：** 根目錄現在可以乾淨地存放程式碼，而網站相關檔案則收納在 docs/ 內。

## **🧪 Lab 5：視覺強化 \- 個人簡介排版 (Flexbox)**

**目標：** 學習使用簡單的 CSS 讓圖片與文字並排，打造專業的 Bio 區塊。

1. **準備圖片：** 在 docs/ 下建立 images/ 資料夾，上傳一張大頭照並命名為 profile.png。  
2. **進階排版實作：** 修改 docs/index.html，將內容替換為以下具備 Flexbox 佈局的結構：
   ```
   --- 
   layout: default  
   ---

   <!-- 個人簡介區塊 -->  
   <div style="display: flex; align-items: center; gap: 20px; margin-bottom: 30px; background: \#f4f4f4; padding: 25px; border-radius: 15px; border-left: 5px solid #157878;">

     <!-- 左側：圓形頭像 -->  
     <img src="images/profile.png" style="width: 120px; height: 120px; border-radius: 50%; border: 3px solid \#157878; object-fit: cover; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">

     <!-- 右側：文字介紹 -->  
     <div>  
       <h2 style="margin-top: 0; color: \#157878;"\>Anita 的 Git 教室</h2>  
       <p style="margin-bottom: 0; line-height: 1.6;"\>哈囉！我是 Anita。這是我專為 Git 初學者設計的實作空間。在這裡，我們不只學指令，更學會如何與程式碼的過去對話！</p>  
     </div>
   </div>
   <hr>
   ```

## **🧪 Lab 6：進階部署 \- GitHub Actions**

**目標：** 模擬專業開發流程，使用自動化工作流部署網站。

1. **切換來源：** 進入 **Settings** \-\> **Pages**。  
2. **選擇來源：** 在 **Source** 下拉選單選擇 **GitHub Actions**。  
3. **套用模板：** 選擇 **Static HTML** 並點擊 **Configure**，直接點擊 **Commit changes**。  
4. **觀察：** 到 **Actions** 標籤查看部署過程。這能讓你在未來結合更複雜的前端建置工具（如 React）。

## **⚠️ 避坑指南 (Troubleshooting)**

1. **畫面沒變色？** \- 檢查 index.html 最上方是否有那兩行 \---。  
   * 檢查 \_config.yml 檔名開頭是否有底線 \_。  
2. **出現 404 錯誤？**  
   * 確認你的主頁檔名是 index.html 或 index.md。  
   * 確認 Settings 中的路徑（root 或 /docs）與檔案實際位置相符。  
3. **YAML 語法報照？**  
   * YAML 格式非常嚴謹，冒號後方**必須有一個半形空格**。  
4. **圖片顯示不出來？**  
   * 檢查路徑是否正確（例如 images/profile.png 是否真的在 HTML 檔案的同層資料夾下）。  
   * 注意檔案大小寫（profile.png 在網路上是區分大小寫的）。

© 2026 GitHub Pages 實作教學 | 由 AnitaHome 製作
