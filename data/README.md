# data フォルダ

## 毎週の更新手順

1. POSからRAWデータCSVを出力
2. このフォルダに `week4.csv`（連番）でアップロード
3. `index.json` に追記する

```json
[
  "week1.csv",
  "week2.csv",
  "week3.csv",
  "week4.csv"
]
```

4. GitHubにコミット → GitHub Pagesに自動反映（約1〜2分）

## ファイル命名規則

| ファイル名 | 内容 |
|---|---|
| week1.csv | 第1週（例：2026/03/01〜03/08） |
| week2.csv | 第2週（例：2026/03/09〜03/14） |
| index.json | CSVファイル一覧（必ず更新） |

## 注意事項
- CSVはShift-JIS形式でOK（自動変換）
- `index.json` を更新しないと新しいCSVが反映されません
