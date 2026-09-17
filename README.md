# MiTALK AI Forum｜純靜態網頁版

此版本以 `index.html` 為主網頁，可直接放在 GitHub Pages、一般網頁主機或 FTP 空間，並可綁定自訂網域。

網站僅呈現活動內容，不包含出席表單、管理後台、資料庫或 Excel 匯出功能。「回覆出席」按鈕會直接開啟 Email 軟體，收件人為 `hello@ysed.org.tw`。

## 檔案結構

- `index.html`：活動主頁
- `assets/styles.css`：網站樣式
- `assets/`：講師照片、Logo 與圖示
- `.nojekyll`：讓 GitHub Pages 直接發布靜態檔案

## 上傳 GitHub Pages

1. 在 GitHub 建立新的 repository。
2. 將本資料夾內所有檔案上傳到 repository 根目錄，確認 `index.html` 位於最上層。
3. 到 Settings → Pages。
4. Source 選擇 Deploy from a branch。
5. Branch 選擇 `main`，資料夾選擇 `/ (root)`，再儲存。

## 綁定外部 DNS／自訂網域

1. 在 GitHub Settings → Pages → Custom domain 填入正式網域。
2. 依 GitHub 顯示的指示，在 DNS 管理平台設定 CNAME 或 A 記錄。
3. 等待 DNS 生效後，勾選 Enforce HTTPS。

若使用子網域（例如 `mitalk.example.org`），通常建立：

```text
Type: CNAME
Name: mitalk
Value: 您的GitHub帳號.github.io
```

請以 GitHub Pages 畫面顯示的值為準。
