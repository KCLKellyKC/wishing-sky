# Midnight Wishing Sky v2.2 Email Magic Link

這版移除 Google OAuth，改成 Supabase Email Magic Link。手機與電腦用同一個 Email 點登入連結，就會讀寫同一份 Supabase `wishes` 資料。

## Supabase 必做設定

1. Authentication → Sign In / Providers → Email。
2. 確認 Email provider enabled。Magic Link 與 Email OTP 屬於 Email provider。
3. Authentication → URL Configuration：
   - Site URL: `https://kclkellykc.github.io/wishing-sky/`
   - Redirect URLs: `https://kclkellykc.github.io/wishing-sky/`
4. `wishes` table 和 RLS Policy 沿用原本設定：`auth.uid()::text = user_id`。

## GitHub Pages

把 ZIP 解壓後全部檔案覆蓋到 repo root，Commit changes，等待 Pages 部署完成。

## 使用方式

1. 開啟網站。
2. 點「Email 登入」。
3. 輸入 Email。
4. 到信箱點 Magic Link。
5. 回到網站後即可跨手機與電腦同步。
