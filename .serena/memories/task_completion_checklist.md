# Task Completion Checklist

タスク完了時に以下を実行すること:

## コントラクト変更時
1. `cd contract && npm run compact` - Compactコンパイル
2. `cd contract && npm run build` - TypeScriptビルド
3. `cd contract && npm run test` - テスト実行
4. `cd contract && npm run lint` - ESLintチェック
5. `cd contract && npm run typecheck` - 型チェック

## CLI変更時
1. `cd counter-cli && npm run lint` - ESLintチェック
2. `cd counter-cli && npm run typecheck` - 型チェック

## 共通
- Apache-2.0ライセンスヘッダーが新規ファイルに付与されているか確認
- `package-lock.json` の変更は `npm install` 後に正常
