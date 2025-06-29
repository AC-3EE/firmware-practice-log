# 📚 Git 使用指南

## 🎯 目的
此指南用於 STM32 / 一般軟體專案版本控制：

- **備份**：將程式碼安全儲存到遠端 (如 GitHub)
- **版本管理**：隨時回到舊版或比較歷史差異
- **多人協作**：未來如有需要可與他人協作

---

## ✅ 常用 Git 指令

### 1️⃣ 檢查專案狀態
查看哪些檔案被修改、尚未提交：

```bash
git status
```


### 2️⃣ 將檔案加入暫存區
將新檔或修改檔案納入版本控制：

```bash
git add .
```

或加入單一檔案：

```bash
git add <檔案名稱>
```


### 3️⃣ 提交到本地倉庫
將暫存區的變更提交：

```bash
git commit -m "本次修改說明"
```


### 4️⃣ 推送到遠端倉庫 (GitHub)
將本地提交同步到 GitHub：

```bash
git push
```


### 5️⃣ 拉取遠端更新
取得並合併 GitHub 上的新提交：

```bash
git pull
```


### ⭐ 進階常用
查看簡易提交紀錄：

```bash
git log --oneline
```

建立並切換到新分支：

```bash
git checkout -b 新分支名稱
```

切換分支：

```bash
git checkout 分支名稱
```

### ❗ 常見狀況 & 解法
推送時出現錯誤：遠端有更新

執行：

```bash
git pull
git push
```

想忽略某些檔案 (如 IDE 設定、編譯產物)

在 .gitignore 加入對應規則後執行：

```bash
git add .gitignore
git commit -m "更新 .gitignore"
git push
```

### 📌 小建議
提交訊息盡量清楚說明這次改了什麼

先拉取遠端更新再推送，避免衝突

多使用 git status 確保自己知道目前專案狀態

若有重要改動，提交前可以先用 git diff 看差異
