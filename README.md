使用 Google Colab 可以簡化操作，因為它已經內建了 Google Drive 整合，且方便執行 AWS S3 操作

打開 Google Colab 並登入 Google 帳號，選擇 Runtime -> Change runtime type -> 選擇 Python 3 環境。

將以下程式碼 s3toGoogleDrive.ipynb 複製到 Colab 並執行



使用說明
1.	填寫 AWS 憑證：
	•	將 YOUR_AWS_ACCESS_KEY_ID 替換為你的 AWS Access Key。
	•	將 YOUR_AWS_SECRET_ACCESS_KEY 替換為你的 AWS Secret Key。
	•	將 YOUR_AWS_REGION 替換為你的 AWS 區域（如 us-east-1）。
	修改 S3 bucket 名稱

2.	運行腳本：
	•	複製腳本到 Colab。
	•	按順序執行每個區塊。
    
3.	檢查結果：
	•	執行最後一個區塊，檢查文件是否已成功同步到 Google Drive。
	•	在 Google Drive 中，你會在 MyDrive/s3_backup 文件夾中找到同步的文件。