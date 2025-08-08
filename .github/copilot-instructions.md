# GitHub Copilot設定管理プロジェクト

このリポジトリはGitHub Copilotの設定ファイルとカスタマイゼーションを管理するためのものです。

## プロジェクト構造

- `.github/copilot-instructions.md` - AI エージェント向けの指示ファイル（このファイル）
- `settings/` - VS Code設定とCopilot関連の設定ファイル
- `templates/` - プロジェクトテンプレートとボイラープレート
- `prompts/` - カスタムプロンプトとテンプレート集
- `docs/` - 設定方法と使用ガイド

## 開発パターン

### 設定ファイルの管理`
- JSON設定ファイルは適切にフォーマットし、コメントを含める
- 設定変更時は必ず`settings/backup/`に既存設定をバックアップ
- 環境固有の設定は`settings/environments/`で分離管理

### プロンプトテンプレート
- `prompts/`下のMarkdownファイルで構造化されたプロンプトを管理
- プロンプトには明確な使用例とパラメータ説明を含める
- 言語固有のプロンプトは`prompts/languages/`で分類

### ドキュメント規則
- すべての設定変更は`docs/changelog.md`に記録
- スクリーンショットは`docs/images/`に配置
- 設定手順は段階的で再現可能な形式で記述

## ワークフロー

### 新しい設定の追加
1. `settings/templates/`から適切なテンプレートをコピー
2. 環境に応じてカスタマイズ
3. `docs/`に設定手順を文書化
4. テスト環境で動作確認

### Copilot最適化
- `.github/copilot-instructions.md`の更新時は具体的な例を含める
- プロジェクト固有のパターンを明確に記述
- 汎用的なアドバイスではなく、このプロジェクトの特有性に焦点

## 重要ファイル

- `settings/vscode/settings.json` - VS CodeのCopilot設定
- `prompts/development/` - 開発用プロンプトコレクション
- `docs/setup-guide.md` - 初期セットアップガイド

## 外部連携

このプロジェクトは個人の開発環境設定を管理するため、外部APIやサービスとの連携は最小限に抑える。設定の同期にはGitリポジトリを使用し、機密情報は環境変数で管理する。
