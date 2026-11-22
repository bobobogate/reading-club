# 心理學好書讀書會｜Read the Mind

心理學好書讀書會的一頁式介紹網站。純 HTML 單檔，不需要安裝或編譯，直接用 GitHub Pages 免費上線。

## 檔案說明

| 檔案 | 用途 |
|---|---|
| `index.html` | 網站本體（樣式、LINE QR Code 都已內嵌在這個檔案裡） |
| `.nojekyll` | 告訴 GitHub Pages 直接發布檔案、不要另外處理（請保留） |
| `docs/website-style-tokens.json` | 網站視覺風格 tokens（顏色、字級、間距等設計規範） |
| `docs/visual-style-analysis.md` | 簡報視覺風格分析（米白＋朱橘紅＋淡藍點綴、Bodoni＋思源宋體） |

字型（Bodoni Moda、Playfair Display、Noto Serif TC）由 Google Fonts 線上載入，不需要額外上傳。

## 上架到 GitHub Pages（網頁操作，不用寫程式）

1. 登入 GitHub，右上角「＋」→ **New repository**。
2. Repository name 填英文，例如 `reading-club`；選 **Public**（免費帳號的 GitHub Pages 需要公開 repo）；按 **Create repository**。
3. 在新 repo 頁面點 **uploading an existing file**（或 Add file → Upload files）。
4. 把這個壓縮檔**解壓縮後**資料夾裡的所有內容（`index.html`、`README.md`、`docs` 資料夾、`.nojekyll`）拖進上傳區，按 **Commit changes**。
   - `.nojekyll` 是隱藏檔，Mac 可在 Finder 按 `Cmd + Shift + .` 顯示；就算漏傳，網站一樣能正常顯示。
5. 進入 repo 的 **Settings → Pages**。
6. 「Build and deployment」的 Source 選 **Deploy from a branch**，Branch 選 **main**、資料夾選 **/ (root)**，按 **Save**。
7. 等 1～3 分鐘，重新整理該頁，上方會出現網址：
   `https://你的帳號.github.io/reading-club/`

## 之後要更新內容

在 repo 裡點 `index.html` → 右上角鉛筆圖示（Edit）→ 修改文字 → **Commit changes**，約 1 分鐘後網站自動更新。

目前標示「籌備中」的項目（FAQ、心理資源／Notion 書單、Accupass 活動報名），之後拿到連結再替換即可：在 `index.html` 搜尋「籌備中」就能找到位置。

## 自訂網域（選用）

已有自己的網域時：Settings → Pages → Custom domain 填入網域，並依 GitHub 指示在網域商設定 DNS。沒有網域就直接用 `github.io` 網址，完全免費。

## 讓 Google 搜得到（SEO）

- `index.html` 的 `<head>` 已加上標題、描述、canonical 網址、社群分享預覽（Open Graph）。
- `robots.txt`、`sitemap.xml` 放在根目錄，部署後網址為 `/robots.txt`、`/sitemap.xml`。
- `og-image.png` 是貼到 LINE／Facebook 時顯示的預覽圖（1200×630）。
- Google Search Console 驗證：在 `index.html` 搜尋 `google-site-verification`，把驗證碼貼進 content，並刪掉那行前後的 `<!--` `-->`。
- 之後若換網址（自訂網域），要一起改：`index.html` 的 canonical 與 og 網址、`robots.txt`、`sitemap.xml`。
