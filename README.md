# Midnight Wishing Sky 雲端正式版

這版有 Email Magic Link 登入與 Supabase 儲存。

## 使用步驟
1. 到 Supabase SQL Editor 執行 `supabase_setup.sql`。
2. 複製 `config.example.js` 內容到 `config.js`，填入 `SUPABASE_URL` 和 `SUPABASE_ANON_KEY`。
3. 到 Supabase Authentication 設定 Email Provider，並加入你的部署網址到 Redirect URLs。
4. 部署整個資料夾。

未填 config.js 時會以本機模式運作；填好後，按右上角「Email 登入」。
