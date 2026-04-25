# Code Style and Conventions

## TypeScript
- ESM modules: `"type": "module"` in package.json
- TypeScript v6.0.2
- `tsconfig.json` (開発用) と `tsconfig.build.json` (ビルド用) の2ファイル構成
- ts-nodeで直接実行: `--no-warnings --experimental-specifier-resolution=node --loader ts-node/esm`

## Linting / Formatting
- ESLint v10 (`eslint.config.mjs` フラットconfig形式)
- Prettier統合 (`eslint-plugin-prettier`, `.prettierrc`)
- `npm run lint` で実行

## Compact (スマートコントラクト)
- ファイル拡張子: `.compact`
- pragma: `pragma language_version >= 0.20;`
- `CompactStandardLibrary` のimportが標準
- コンパイル出力: `src/managed/<contract-name>/`

## ライセンスヘッダー
全ソースファイルに Apache-2.0 ライセンスヘッダーを付与:
```
// This file is part of midnightntwrk/example-counter.
// Copyright (C) 2025 Midnight Foundation
// SPDX-License-Identifier: Apache-2.0
```

## テスト
- Vitest (`vitest.config.ts`)
- コントラクトテストは `contract/src/test/` に配置
- シミュレーター (`counter-simulator.ts`) を使ったオフチェーンテスト
