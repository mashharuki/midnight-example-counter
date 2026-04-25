# Project Structure

npm workspaces構成 (ルートpackage.json):

```
midnight-example-counter/
├── contract/                          # スマートコントラクト (Compact言語)
│   ├── src/
│   │   ├── counter.compact            # Compactコントラクト本体
│   │   ├── index.ts                   # TypeScriptエクスポート
│   │   ├── witnesses.ts               # Witnessデータ
│   │   └── test/
│   │       ├── counter.test.ts        # ViTestテスト
│   │       └── counter-simulator.ts  # テスト用シミュレーター
│   ├── package.json                   # npm scripts: compact/build/test/lint
│   ├── tsconfig.json / tsconfig.build.json
│   ├── vitest.config.ts
│   └── eslint.config.mjs
│
├── counter-cli/                       # CLIアプリケーション
│   ├── src/
│   │   ├── standalone.ts              # Standalone起動エントリーポイント
│   │   ├── preprod.ts                 # Preprod接続エントリーポイント
│   │   ├── preprod-start-proof-server.ts
│   │   ├── preview.ts                 # Preview接続エントリーポイント
│   │   └── preview-start-proof-server.ts
│   ├── proof-server.yml               # Proof server Docker設定
│   ├── standalone.yml                 # フルローカルスタックDocker設定
│   ├── standalone.env.example         # Standalone環境変数サンプル
│   ├── package.json
│   ├── tsconfig.json / tsconfig.build.json
│   └── vitest.config.ts
│
├── package.json                       # ルート (workspaces定義 + 共通依存)
├── package-lock.json
├── README.md
├── MIGRATION_GUIDE.md
└── CHANGELOG.md
```

## Compact Contract Summary
```compact
pragma language_version >= 0.20;
import CompactStandardLibrary;

export ledger round: Counter;      // パブリックな状態

export circuit increment(): [] {   // トランジション関数
  round.increment(1);
}
```
