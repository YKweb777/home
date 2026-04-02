# 世界の株価一覧サイト

GitHub Pages で公開できる、世界の主要市場に連動する ETF の価格一覧ページです。

## 構成

- `index.html` : 公開ページ本体
- `config/markets.json` : 表示したい市場の設定
- `data/markets.json` : GitHub Actions が更新するデータファイル
- `.github/workflows/update-markets.yml` : 株価更新ワークフロー

## セットアップ

1. このファイル一式をリポジトリのルートに置く
2. GitHub で `Settings -> Secrets and variables -> Actions` を開く
3. `ALPHAVANTAGE_API_KEY` という Repository secret を追加する
4. GitHub Pages を `main` ブランチの `/ (root)` で有効化する
5. `Actions` タブから `Update market data` を手動実行する

## カスタマイズ

- 表示銘柄は `config/markets.json` で編集できます
- 初期設定は各地域を代表する ETF です
- 個別株に変えたい場合は `symbol` と `name` を差し替えてください
