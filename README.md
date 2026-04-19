# 千房グループ 春メニュー販売数ダッシュボード

## ファイル構成

```
chibo-dashboard/
├── index.html               ← ダッシュボード本体
├── data/
│   ├── index.json           ← ファイル一覧（毎月更新）
│   ├── sales/               ← 日別販売実績表CSV
│   │   ├── 202603.csv
│   │   └── 20260412.csv
│   └── customers/           ← 日別売上実績表CSV（客数）
│       ├── 202603.csv
│       └── 20260418.csv
```

## 毎週の更新手順

1. `data/sales/` に日別販売実績表CSVをアップロード（例: `20260419.csv`）
2. `data/customers/` に日別売上実績表CSVをアップロード（例: `20260419.csv`）
3. `data/index.json` を編集してファイル名を追記：

```json
{
  "sales": ["202603.csv", "20260412.csv", "20260419.csv"],
  "customers": ["202603.csv", "20260418.csv", "20260419.csv"]
}
```

4. GitHub Pagesに自動反映（約1〜2分）

## GitHub Pages URL

```
https://chibokawata.github.io/recomendsales-dashbord/
```

## 新機能（今回追加）

- **前週比**：店舗別ランキングに前週との販売数差を表示
- **曜日別販売数**：平日/土曜/日祝の販売内訳グラフ
- **店舗平均販売数**：KPIカードに追加
- **注文率**：販売実績表＋売上実績表（客数）を自動結合して計算
