# Zenn 自動取引ログ

stock-app から自動生成される日次取引記事を蓄積する Zenn リポジトリです。

## セットアップ

1. このリポジトリを GitHub に push
2. [Zenn ダッシュボード](https://zenn.dev/dashboard) → GitHub 連携
3. stock-app の `.env` に以下を設定:

```env
ZENN_REPO_PATH=/path/to/this/repo
ZENN_AUTO_PUSH=true
ZENN_PUBLISHED=false   # デモ期間は下書き推奨
```

## ディレクトリ構成

```
articles/          # 日次ログ（自動生成）
books/             # 月次まとめ（有料本用チャプター）
images/            # 画像（任意）
```

## ローカルプレビュー

```bash
npm install
npm run preview
# http://localhost:8000
```

## 有料本（Zenn Books）

月次チャプターは stock-app から生成:

```bash
python publish_zenn.py monthly --year 2026 --month 6
```

Zenn ダッシュボードで本を公開し、価格（200円〜5,000円）を設定してください。
