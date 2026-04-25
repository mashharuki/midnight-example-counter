# Counter DApp - Project Overview

## Purpose
Midnight Network上に構築されたシンプルなオンチェーンカウンターのDAppサンプル。
Compact言語でスマートコントラクトを記述し、TypeScript CLIから操作する。
テンプレートリポジトリとして提供され、Midnight DApp開発の出発点となる。

## Tech Stack
- **Smart Contract**: Compact言語 (Midnight専用ZKスマートコントラクト言語), toolchain 0.30.0
- **TypeScript**: v6.0.2, ESM modules (type: "module")
- **Runtime**: Node.js v22.15+
- **Testing**: Vitest
- **Linting/Formatting**: ESLint + Prettier
- **Infrastructure**: Docker / Docker Compose (proof server, standalone node)
- **SDK**: @midnight-ntwrk/* packages (midnight-js v4+, wallet-sdk v3+)

## Supported Networks
| Network | Description | Command |
|---------|-------------|---------|
| Preprod | 公開テストネット（推奨） | `npm run preprod-ps` (counter-cli内) |
| Preview | プレビューテストネット | `npm run preview-ps` (counter-cli内) |
| Standalone | ローカルDocker環境 | `npm run standalone` (counter-cli内) |
