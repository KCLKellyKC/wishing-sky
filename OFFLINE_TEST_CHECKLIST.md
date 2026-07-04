# 深夜許願星空 PWA 離線安裝測試 Checklist

> 測試前請用 HTTPS 或 localhost 開啟。Service Worker 不能只靠雙擊檔案啟用。

## 共通檢查

- [ ] 第一次載入後，DevTools Application/應用程式面板可看到 `manifest.webmanifest`。
- [ ] Service Worker 狀態為 activated/running。
- [ ] Cache Storage 內有 `wishing-sky-pwa-v3`。
- [ ] IndexedDB 內有 `WishingSkyDB`，包含 `wishes` 與 `meta`。
- [ ] 新增願望後重新整理，星星仍存在。
- [ ] 關閉網路後重新整理，頁面仍可開啟。
- [ ] 匯出 JSON 成功，匯入 JSON 後星星數量正確。
- [ ] 切換主題後重新整理，主題仍保留。
- [ ] 成就解鎖後重新整理，成就仍保留。

## Chrome Desktop / Edge Desktop

- [ ] URL bar 或頁面按鈕出現安裝提示。
- [ ] 點擊「安裝 App」後可用獨立視窗開啟。
- [ ] DevTools > Network 勾選 Offline 後重新整理仍可使用。
- [ ] Application > Manifest 無重大錯誤，192/512 icons 可讀取。

## Android Chrome

- [ ] 開啟頁面後可看到「安裝 App」或瀏覽器選單的「安裝應用程式」。
- [ ] 安裝後主畫面出現 App icon。
- [ ] 從主畫面開啟時為 standalone 體驗。
- [ ] 飛航模式下仍可開啟、查看歷史星星與月曆。
- [ ] Web Audio 需使用者點擊後才播放，符合瀏覽器限制。

## iOS / iPadOS Safari

- [ ] 使用 Safari 分享選單 > 加入主畫面。
- [ ] 主畫面 icon 可開啟 App。
- [ ] 離線後可開啟已快取版本。
- [ ] iOS 不一定支援 `beforeinstallprompt`，所以頁面上的「安裝 App」按鈕可能不出現，屬正常。
- [ ] 檢查安全區域 safe-area-inset 顯示正常，按鈕未被瀏海或 Home indicator 擋住。

## Safari macOS

- [ ] 測試基本離線快取與 IndexedDB 保存。
- [ ] 若沒有瀏覽器提供的安裝提示，屬平台支援差異。
- [ ] 仍可透過書籤/加入 Dock 等方式手動存取。

## 回歸測試情境

- [ ] 第一天新增一顆「感謝」：解鎖「第一次感謝」。
- [ ] 新增一顆「放下」：解鎖「第一次放下」。
- [ ] 累積 10 顆：解鎖「小小銀河」。
- [ ] 連續 7 天資料：解鎖「連續 7 天許願」。可用匯入 JSON 模擬不同日期。
- [ ] 點擊歷史星星，星座故事顯示正常。
- [ ] 切換四種主題：深夜藍、晨霧白、森林綠、玫瑰夜空，重整後保留。
