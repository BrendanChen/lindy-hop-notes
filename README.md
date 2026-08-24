# Lindy Hop 練習筆記

上課後複習筆記，用 [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) 產生靜態網站，透過 GitHub Actions 自動部署到 GitHub Pages。

## 新增一則筆記

在 `docs/` 資料夾新增一個 `.md` 檔案即可，檔名建議用 `YYYY-MM-DD_主題.md`（依日期排序，同時也是側邊欄的排序依據）。push 到 `main` 分支後，GitHub Actions 會自動重新部署網站。

## 本機預覽

```bash
pip install -r requirements.txt
mkdocs serve
```

然後打開 http://127.0.0.1:8000

## 部署

`main` 分支有異動時，`.github/workflows/deploy.yml` 會自動執行 `mkdocs gh-deploy`，把產生的靜態網站推到 `gh-pages` 分支。第一次部署完成後，記得去 repo 的 **Settings → Pages** 確認 Source 設定成 `gh-pages` 分支（通常會自動偵測到並設定好，保險起見還是確認一下）。
