# **🧪 GitHub Gists 實戰**

**目標：** 學習如何使用 Gists 快速分享程式碼片段，並了解其與一般儲存庫（Repository）的差異。

### **1\. 建立你的第一個 Gist**

* 前往 [gist.github.com](https://gist.github.com/)。  
* 在描述欄位輸入：My Git Tips。  
* 檔名輸入：git-cheatsheet.md。  
* 內容輸入一些常用的指令：
  ```
  # Git 常用指令  
  - `git status`: 查看狀態  
  - `git commit -m "msg"`: 提交紀錄
  ```

* 點擊 **Create secret gist** (秘密) 或 **Create public gist** (公開)。

### **2\. 練習嵌入 (Embed)**

* 在你的 Gist 頁面右上角，點擊 **Embed** 下拉選單。  
* 複製出現的 <script\> 標籤。  
* **練習：** 試著將它貼到你的 index.html 中，重新發佈後，你會發現程式碼會帶有精美的語法高亮直接顯示在網頁上。

### **3\. 進階：使用 Git 指令管理 Gist**

每個 Gist 在底層其實都是一個獨立的 Git Repo，這意味著你可以使用熟悉的指令來更新它：

* 複製 Gist 頁面上的 **Clone URL**。  
* 在終端機執行：  
  git clone [https://gist.github.com/\](https://gist.github.com/)<你的 Gist ID\>.git

* 在本地修改檔案、Commit 並 git push。  
* 重新整理 Gist 網頁，查看 **Revisions** (修訂紀錄)，你會看到完整的版本歷史。

### **💡 Gist 與 Repo 的差異**

* **Repo**：適合多檔案、複雜架構、完整專案。  
* **Gist**：適合單一檔案、快速分享、跨網站嵌入。

<!-- 返回按鈕 -->
<div style="margin-top: 50px; text-align: center; display: flex; justify-content: center; gap: 20px;"\>
<a href="index.html" class="btn" style="padding: 10px 25px; color: \#157878; border: 1px solid \#157878; text-decoration: none; border-radius: 5px;"\>🏠 回到首頁\</a\>
</div\>

© 2026 AnitaHome | GH900-Ch02
