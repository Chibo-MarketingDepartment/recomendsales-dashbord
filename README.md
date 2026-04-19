# 千房グループ 春メニュー販売数ダッシュボード

## セットアップ手順（初回のみ・約15分）

### STEP 1: GitHubリポジトリを作成

1. https://github.com にログイン
2. 右上「＋」→「New repository」
3. 設定：
   - Repository name: `chibo-dashboard`（任意）
   - Public を選択（GitHub Pagesに必要）
   - 「Create repository」をクリック

### STEP 2: ファイルをアップロード

1. 作成したリポジトリを開く
2. 「uploading an existing file」をクリック
3. 以下のファイルをドラッグ＆ドロップ：
   - `index.html`
   - `data/index.json`
4. 「Commit changes」をクリック

### STEP 3: GitHub Pagesを有効化

1. リポジトリの「Settings」タブ
2. 左メニュー「Pages」
3. Source：「Deploy from a branch」
4. Branch：「main」/ 「/ (root)」を選択して「Save」
5. 1〜2分後に `https://【ユーザー名】.github.io/chibo-dashboard/` でアクセス可能

---

## 毎週の更新手順（約3分）

### 方法A: GitHub画面から（推奨・PCブラウザのみ）

1. GitHubのリポジトリを開く
2. `data` フォルダをクリック
3. 「Add file」→「Upload files」
4. 新しいCSVをアップロード（例：`week4.csv`）
5. 「Commit changes」
6. `data/index.json` を開いて「鉛筆アイコン（Edit）」をクリック
7. ファイル名を追記して「Commit changes」

```json
[
  "week1.csv",
  "week2.csv",
  "week3.csv",
  "week4.csv"
]
```

### 方法B: GitHub Desktop（PC アプリ）

1. GitHub Desktopでリポジトリをクローン
2. `data/` フォルダにCSVをコピー
3. `data/index.json` を編集してファイル名を追記
4. GitHub Desktopで「Commit」→「Push」

---

## ファイル構成

```
chibo-dashboard/
├── index.html          ← ダッシュボード本体（更新不要）
├── README.md           ← この手順書
└── data/
    ├── index.json      ← CSVファイル一覧（毎週更新）
    ├── week1.csv       ← 第1週データ
    ├── week2.csv       ← 第2週データ
    └── week3.csv       ← 第3週データ...
```

## ダッシュボードURL

```
https://【GitHubユーザー名】.github.io/chibo-dashboard/
```

## GA4計測ID

`G-XPZJL7GN67`（index.htmlに埋め込み済み）

---

## よくある質問

**Q: CSVを追加したのに反映されない**  
A: `data/index.json` の更新を忘れていないか確認。更新後1〜2分待ってください。

**Q: GitHub Pagesのページが404になる**  
A: Settings → Pages でブランチが「main」になっているか確認。

**Q: データが文字化けする**  
A: CSVをShift-JIS形式で保存されているか確認（自動変換対応済みですが稀に失敗することがあります）。
