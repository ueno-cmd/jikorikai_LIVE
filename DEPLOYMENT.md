# ジコリカイLIVE デプロイメント引継ぎ資料

## プロジェクト概要
- **プロジェクト名**: ジコリカイLIVE
- **プロジェクトタイプ**: Vite静的サイト
- **デプロイ先**: Cloudflare Pages
- **ビルドコマンド**: `npm run build`
- **出力ディレクトリ**: `dist`

## 現在の状態
### ✅ 完了済み
- SEO対策実装（meta tags, OGP, 構造化データ）
- .gitignore設定済み
- wrangler.toml作成済み
- 日本語対応（lang="ja"）
- レスポンシブデザイン
- 現実的な会場設定（都内ライブハウス調整中）

### 🔄 未定・準備中の要素
- 開催日時：2026年6月（詳細未定）
- 会場：都内ライブハウス（調整中）
- 出演アーティスト（Coming Soon表示中）
- チケット販売（準備中表示）
- SNSアカウント（準備中表示）
- 応募フォーム（準備中表示）

## デプロイ手順

### 1. GitHub連携準備
```bash
# 現在のディレクトリ構造確認
# jikorikai_LIVE/
# ├── index.html
# ├── package.json
# ├── wrangler.toml
# ├── .gitignore
# ├── src/
# │   ├── js/main.js
# │   └── styles/main.css
# └── public/
```

### 2. Cloudflare Pages設定
- **ビルドコマンド**: `npm run build`
- **ビルド出力ディレクトリ**: `dist`
- **Node.jsバージョン**: 18.x以上推奨
- **環境変数**: 特になし

### 3. wrangler.toml設定内容
```toml
name = "jikorikai-live"
compatibility_date = "2024-07-01"

[env.production]
name = "jikorikai-live"

[build]
command = "npm run build"
cwd = ""
watch_dir = "src"

[[pages_build_output_dir]]
value = "dist"
```

## SEO設定詳細

### Meta Tags
- **Title**: ジコリカイLIVE - 最高の音楽体験があなたを待っている
- **Description**: 自己理解プログラム修了生によるアーティストが一堂に会する特別な音楽イベント。2026年6月開催予定。
- **Keywords**: ジコリカイLIVE,音楽イベント,ライブ,アーティスト,東京,2026,自己理解,コンサート

### Open Graph設定
- **og:type**: event
- **og:url**: https://jikorikai-live.pages.dev
- **og:locale**: ja_JP

### 構造化データ（JSON-LD）
- イベントタイプでschema.org準拠
- 会場：都内ライブハウス（調整中）
- 日時：2026年6月

## 今後の更新ポイント

### 1. 詳細決定時の更新箇所
- **index.html line 24**: 開催日時の具体的な日付
- **index.html line 36-37**: 構造化データの開催日時
- **index.html line 42**: 会場名

### 2. 機能追加時の対応
- **SNS設定**: Twitter Cardにimage追加
- **チケット販売**: Peatix統合
- **アーティスト発表**: lineup-sectionの更新
- **応募フォーム**: Google Forms統合

## 技術スタック
- **フレームワーク**: Vite
- **言語**: Vanilla JavaScript, CSS
- **ビルドツール**: Vite
- **デプロイ**: Cloudflare Pages
- **ドメイン**: jikorikai-live.pages.dev（予定）

## 注意事項
1. **画像最適化**: 必要に応じてWebP形式を使用
2. **パフォーマンス**: Lighthouseスコア確認推奨
3. **アクセシビリティ**: 色彩コントラスト、フォーカス管理
4. **モバイル対応**: レスポンシブデザイン確認

## 緊急時の連絡先
- プロジェクト管理者: [未設定]
- 技術担当: [未設定]

## 関連ファイル
- `CLAUDE.md`: プロジェクト詳細とClaude Code向けガイダンス
- `package.json`: 依存関係とスクリプト
- `wrangler.toml`: Cloudflare設定
- `.gitignore`: Git除外設定

---
**最終更新**: 2024-07-20
**作成者**: Claude Code AI Assistant