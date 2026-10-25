# CLAUDE.md

## 專案說明

台南海事 AI 航海法規智慧系統。單頁網站，使用者輸入問題，前端呼叫 Gemini 或 Groq，依海事法規題庫回答。

- `index.html`：前端主程式，所有畫面與邏輯都在這裡
- `law.txt`：海事法規題庫，`index.html` 以 `fetch('law.txt')` 讀取
- `law.js`：與 `law.txt` 內容相同，掛成 `window.lawText`；修改題庫時兩份要一起改
- `海事法規精華重點整理 - 台北海洋科技大學航海系.pdf`：題庫原始資料

API key 由使用者在頁面輸入，存在 sessionStorage。`TEACHER_GROQ_KEY`、`TEACHER_GEMINI_KEY` 必須保持空字串，這個 repo 是公開的，不可寫入真實 key。

## 版本與推送規則

- 擁有者：GitHub 帳號 `childalice-dev`
- 改完程式後，直接 commit 並 push，不必再詢問
- 修改一律在工作分支上進行，不直接推到 `main`
- `main` 是正式版（GitHub Pages 發布的分支）；工作分支要合併進 `main` 時，開 PR 交給擁有者決定，擁有者明確說「直接推 main」才可直接推
- commit 訊息用繁體中文，簡述改了什麼

## 新網頁

每個新網頁各自建立一個 repo，放在 `childalice-dev` 底下，不放進這個 repo。
