# 全てのプロンプトでこのファイル内容を参照して下さい

# CRITICAL RULE: One Task, One Review Principle

このルールは特に厳格に順守してください
**1ファイルの追加・変更毎に**、以下の1-3のサイクルを厳守して開発を進めます
1ファイルの追加・変更の中に複数の機能が含まれる場合、**1機能の追加・変更毎に**以下の1-3のサイクルを順守してください

1. 1つのファイル、又は機能を追加・変更した場合、その実装の概要を詳細に説明します
2. 実装の意図と概要を説明したら、**必ず開発者に「レビューをお願いします」の文言を添えて、レビューを依頼します**。レビューの承認を受けるまで、決して実装を進めてはなりません。
3. 開発者が実装内容をレビューし、その承認を受けたら、**次に行う実装の概要を詳細に説明し、開発者に実装概要のレビューを依頼してください**。開発者が次の実装に対して承認するまで、決して実装を進めてはなりません。

# Prohibited actions
- `rm`コマンドの提案禁止

## Basic Rules

順守すべき基本的な規約を以下に示します

- 英語で思考し、日本語で回答します
- 破壊的な変更を行うときは必ず確認をとって下さい
- タスクは細分化します
  - コーディングする時は細分化されたタスクに対して、更に細かな粒度で実装します
  - 一度のプロンプトから一度に大量のコードを生成しないでください
- ファイルの先頭にあるimport文を必ず確認して下さい
- ライブラリの導入はコマンドによる導入を優先してください

## Coding Standards

コーディングする時には以下の規約を遵守して下さい

- **YAGNI (You Aren't Gonna Need It): 将来使うかもしれない機能は実装しない**
  - 現在の要件に集中し、推測による実装は避ける
- **DRY (Don't Repeat Yourself): 重複コードは必ず関数化・モジュール化する**
  - 同じロジックの重複を排除し、保守性を向上させる
- **KISS (Keep It Simple, Stupid): コードはシンプルに保ち、理解しやすく、デバッグしやすいコードを心がける**
  - 複雑な解決策より単純な解決策を優先

## Context7の利用の順守

- 使用できる状況では常にContext7で最新のドキュメントに基づいて実装をしてください

## 技術スタック

<!-- 技術スタックを記述

### フロントエンド
react 18

### バックエンド
ruby on rails 7

### データベース

### インフラ

-->

## The following instructions are only to be applied when performing a code review.

### Prompt file guide

**Only apply to files that end in `.prompt.md`**

* [ ] The prompt has markdown front matter.
* [ ] The prompt has a `mode` field specified of either `agent` or `ask`.
* [ ] The prompt has a `description` field.
* [ ] The `description` field is not empty.
* [ ] The `description` field value is wrapped in single quotes.
* [ ] The file name is lower case, with words separated by hyphens.
* [ ] Encourage the use of `tools`, but it's not required.
* [ ] Strongly encourage the use of `model` to specify the model that the prompt is optimised for.

### Instruction file guide

**Only apply to files that end in `.instructions.md`**

* [ ] The instruction has markdown front matter.
* [ ] The instruction has a `description` field.
* [ ] The `description` field is not empty.
* [ ] The `description` field value is wrapped in single quotes.
* [ ] The file name is lower case, with words separated by hyphens.
* [ ] The instruction has an `applyTo` field that specifies the file or files to which the instructions apply. If they wish to specify multiple file paths they should formated like `'**.js, **.ts'`.

### Chat Mode file guide

**Only apply to files that end in `.chatmode.md`**

* [ ] The chat mode has markdown front matter.
* [ ] The chat mode has a `description` field.
* [ ] The `description` field is not empty.
* [ ] The `description` field value is wrapped in single quotes.
* [ ] The file name is lower case, with words separated by hyphens.
* [ ] Encourage the use of `tools`, but it's not required.
* [ ] Strongly encourage the use of `model` to specify the model that the chat mode is optimised for.
