# LinguaVideo - 英文句子即時同步語音影片生成器

> 輸入英文句子 ➔ AI 真人擬真發音 ➔ 唸到哪、字詞高亮到哪（即時卡拉OK視覺同步）➔ 轉成影片導出。

## 專案內容
- `index.html`：純前端 Web App，支援輸入句子、AI 語音合成、單字級卡拉OK同步高亮、16:9 / 9:16 短影音切換與直接一鍵錄製導出影片。
- `generator.py`：後端 Python 自動化管線，利用 `edge-tts` 提取逐字時間戳 (WordBoundary)，並透過 FFmpeg 批量生成 1080p MP4 影片。
- `requirements.txt`：Python 依賴套件清單。

## 快速部署至 GitHub Pages（免費線上網站）
1. 在 GitHub 建立一個名為 `lingua-video` 的公開倉庫 (Public Repository)。
2. 將本專案中的 `index.html` 上傳至倉庫根目錄。
3. 進入倉庫的 **Settings** -> **Pages**。
4. 在 **Build and deployment** 下的 Branch 選擇 `main`（或 `master`），資料夾選擇 `/ (root)`，點擊 **Save**。
5. 稍等 1 分鐘，即可透過 `https://<你的 GitHub 帳號>.github.io/lingua-video/` 在任何裝置上直接使用！

## 本機執行 Python 影片生成器
```bash
# 1. 安裝依賴
pip install -r requirements.txt

# 2. 安裝系統工具 FFmpeg (macOS: brew install ffmpeg / Ubuntu: sudo apt install ffmpeg)

# 3. 執行示範影片生成
python generator.py --demo
```
