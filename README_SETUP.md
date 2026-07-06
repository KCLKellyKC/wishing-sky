# Midnight Wishing Sky v2.0 Supabase Cloud Sync

## 已填入你的 Supabase 設定
- Project URL: https://dqsxliknvtqxqkyuhdag.supabase.co
- Publishable key 已放在 config.js

## 上傳 GitHub Pages
將 ZIP 解壓後所有檔案覆蓋到 GitHub Repository root，Commit changes 等待 1-3 分鐘。

## 必要 Supabase 設定
1. `wishes` table 已建立。
2. Authentication → Sign In / Providers → Anonymous 已啟用。
3. RLS policies 已建立。

## 注意
目前使用 Anonymous 登入。手機與電腦若各自產生不同匿名 user，資料會分開。若要真正跨不同瀏覽器同帳號同步，下一版建議改成 Email Magic Link 或 Google Login。
