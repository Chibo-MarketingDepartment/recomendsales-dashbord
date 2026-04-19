# 千房グループ 春メニューダッシュボード v3

## ファイル構成
```
chibo-dashboard/
├── index.html               ← ダッシュボード本体（更新不要）
└── data/
    ├── index.json           ← ファイル一覧（毎月更新）
    ├── sales/               ← 日別販売実績表CSV
    │   ├── 202603.csv
    │   └── 20260412.csv
    └── customers/           ← 日別売上実績表CSV（客数）
        ├── 202603.csv
        └── 20260418.csv
```

## GitHub Pages URL
```
https://chibokawata.github.io/recomendsales-dashbord/
```

## 毎週の更新（3分）
1. `data/sales/` に日別販売実績表CSVをアップロード
2. `data/customers/` に日別売上実績表CSVをアップロード
3. `data/index.json` を編集してファイル名を追記：

```json
{
  "sales": ["202603.csv", "20260412.csv", "20260419.csv"],
  "customers": ["202603.csv", "20260418.csv", "20260419.csv"]
}
```

## 機能一覧
- 注文率・販売数 KPI（前週比付き）
- 週次折れ線グラフ（注文率・販売数）
- 曜日別販売数（平日/土曜/日祝）
- 店舗別注文率ランキング（前週比・達成判定・アラート）
- メニュー別販売数ランキング
- 業態別・立地別・地域別 集計バー
- ドリルダウン（店舗→メニュー別 / メニュー→店舗別）
- 月別タブ（3月・4月比較）
- MO比較タブ（MobileOrder vs POP）
- 累積表示モード
- フィルタ：事業部 / メニュー / 地域 / 導線
