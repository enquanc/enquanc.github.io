# En-Chuan Chen — Personal Site

根據履歷內容建立的靜態個人網站，純 HTML / CSS / JS，無需建置工具，可直接部署到 GitHub Pages。

## 檔案結構

```
self/
├── index.html              # 網站主頁面
├── Resume_Enquanc.pdf       # 履歷 PDF（「View Résumé」按鈕連結）
└── assets/
    ├── css/style.css        # 樣式（含亮 / 暗色主題）
    └── js/main.js            # 互動邏輯（主題切換、捲動進度條、滾動動畫）
```

## 內容區塊

- **About** — 簡介、Traits／Core Strengths／Focus Areas／Languages & Frameworks
- **Education** — 學歷（中央大學碩士在讀、中興大學應數系）
- **Experience** — 研究經歷（中央大學多媒體訊號處理實驗室、中研院資訊所研究助理／實習）
- **Research & Projects** — 重點研究 TAFI（2026 ICME）、其他研究與課程專案
- **Awards** — 榮譽獎項
- **Contact** — Email、GitHub 連結

## 本機預覽

直接用瀏覽器開啟 `index.html` 即可，或用簡單的本機伺服器：

```bash
python -m http.server 8000
# 瀏覽 http://localhost:8000
```

## 部署到 GitHub Pages

1. 建立一個名為 `enquanc.github.io` 的 GitHub repository（repo 名稱需與你的 GitHub 帳號一致，才能用根網域）。
2. 把 `self/` 資料夾內的內容（`index.html`、`assets/`、`Resume_Enquanc.pdf`）放到該 repo 的根目錄。
3. Push 到 `main` 分支：

   ```bash
   git init
   git add .
   git commit -m "Initial personal site"
   git branch -M main
   git remote add origin https://github.com/enquanc/enquanc.github.io.git
   git push -u origin main
   ```

4. 到 repo 的 **Settings → Pages**，Source 選擇 `main` 分支 `/ (root)`，儲存即可。
5. 幾分鐘後即可透過 `https://enquanc.github.io` 造訪網站。

## 後續可自訂

- 可替換 `assets/img/` 加入大頭照或研究成果圖。
- 若要加入 Publications／Projects 區塊，可仿照 `.research-feature` 的結構新增卡片。
- 履歷公開頁面預設不放電話號碼，僅保留 Email 與 GitHub，若要顯示可自行加入 `#contact` 區塊。
