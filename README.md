# 株式会社RIGEL ホームページ

1ページ構成の静的サイト。ビルド不要（HTML/CSSのみ）。

## ファイル構成
- `index.html` … 本体（会社概要・RTS事業紹介・お問い合わせ）
- `assets/rigel-logo.png` … 正式ロゴ（規定色 #026881 に補正済み）
- `CNAME` … GitHub Pages用のカスタムドメイン指定（`rigel-works.com`）

## GitHub Pagesへの公開手順

1. GitHubで新規リポジトリを作成（例: `rigel-homepage`）
2. このフォルダの中身をリポジトリにpush
   ```bash
   git init
   git add .
   git commit -m "Initial homepage"
   git branch -M main
   git remote add origin https://github.com/<ユーザー名>/rigel-homepage.git
   git push -u origin main
   ```
3. GitHubリポジトリの Settings → Pages で、Source を `main` ブランチ / `/ (root)` に設定
4. ドメインレジストラ側のDNS設定で、`rigel-works.com` に以下のいずれかを設定
   - Aレコード: GitHub Pagesの4つのIPアドレス（185.199.108.153 等、GitHub公式ドキュメント参照）
   - もしくは `www` サブドメインを使う場合はCNAMEレコードで `<ユーザー名>.github.io` を指定
5. `rigel-works.jp` は、ドメインレジストラの「転送設定（フォワーディング）」機能で `https://rigel-works.com` へ301リダイレクトするよう設定（GitHub Pages側では二重ドメインを持てないため）

## 今後の更新候補
- 所在地の詳細（丁目番地）は、法人登記完了後に追記するか検討
- 事業内容を増やす場合は、②FA設備設計事業などのセクションを追加
