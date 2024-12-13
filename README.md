# S3 to Google Drive with Google Colab

使用 Google Colab，可以簡化從 AWS S3 同步文件到 Google Drive 的操作。這個方法利用了 Colab 內建的 Google Drive 整合功能，並且方便執行 AWS S3 的操作。

---

## 環境準備

1. 打開 [Google Colab](https://colab.research.google.com/) 並登入 Google 帳號。
2. 選擇 `Runtime -> Change runtime type`，將運行環境設置為 **Python 3**。

---

## 使用說明

### 1. 填寫 AWS 憑證

在腳本中找到以下變數，並替換為你的 AWS 資訊：
- `YOUR_AWS_ACCESS_KEY_ID`：替換為你的 AWS Access Key。
- `YOUR_AWS_SECRET_ACCESS_KEY`：替換為你的 AWS Secret Key。
- `YOUR_AWS_REGION`：替換為你的 AWS 區域（例如 `us-east-1`）。

此外，確認你的 **S3 bucket 名稱** 是否正確。

---

### 2. 運行腳本

1. 複製以下程式碼到 Colab。
2. 按順序執行每個代碼區塊，等待同步完成。

---

### 3. 檢查結果

1. 執行腳本的最後一個區塊。
2. 在 Google Drive 中，檢查 `MyDrive/s3_backup` 資料夾，確認文件是否成功同步。

---



注意事項

1.	安全性：
不要將 AWS 憑證直接暴露在公開的 GitHub 存儲庫中。如果需要共享 Notebook，可以考慮通過環境變數或輸入框的方式獲取憑證。

2.	Bucket 名稱：
確保在腳本中將 YOUR_BUCKET_NAME 替換為你的 S3 Bucket 名稱。

3.	檔案同步：
使用 aws s3 sync 命令時，只有新增或修改的文件會被下載，已存在的文件不會被重複下載。



