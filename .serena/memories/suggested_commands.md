# Suggested Commands

## セットアップ
```bash
# 依存インストール (ルート)
npm install

# Compact toolchainインストール (初回のみ)
curl --proto '=https' --tlsv1.2 -LsSf https://github.com/midnightntwrk/compact/releases/latest/download/compact-installer.sh | sh
source $HOME/.local/bin/env
compact update 0.30.0
```

## コントラクトビルド
```bash
cd contract
npm run compact       # Compactコンパイル (src/managed/ に出力)
npm run build         # TypeScriptビルド (dist/ に出力)
npm run test          # Vitestテスト実行
npm run test:compile  # コンパイル + テスト
npm run lint          # ESLintチェック
npm run typecheck     # TypeScript型チェック
```

## CLIアプリ実行
```bash
cd counter-cli
npm run preprod-ps    # Preprod (proof serverも自動起動, 推奨)
npm run preprod       # Preprod (proof serverは別途起動済み前提)
npm run preview-ps    # Preview (proof serverも自動起動)
npm run preview       # Preview
npm run standalone    # ローカルDocker環境フルスタック
npm run test-api      # APIテスト (Docker使用)
npm run lint          # ESLintチェック
npm run typecheck     # TypeScript型チェック
```

## インフラ
```bash
# Proof server (Preprod/Preview用)
cd counter-cli && docker compose -f proof-server.yml up

# フルローカルスタック起動
cd counter-cli && docker compose -f standalone.yml up
```
