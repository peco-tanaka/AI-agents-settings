# 全てのプロンプトでこのファイル内容を参照して下さい

# 最重要順守事項 

以下の原則は特に順守するように意識してください

- **１タスク１レビューの原則**
  - 1つのファイルを作成・編集したら、その実装の意図と概要を説明し、必ず開発者にレビューを依頼します
    - 開発者がレビューし、承認を受けるまで実装を続行してはいけません

## 基本規約 / Basic Rules

順守すべき基本的な規約を以下に示します

- 破壊的な変更を行うときは必ず確認をとって下さい
- タスクは細分化します
  - 実装する時は細分化されたタスクに対して、更に細かな粒度で実装します
- 一度のプロンプトから一度に大量のコードを生成しないでください
- 生成されたコードを逐一レビューするために、コードは非常に小さな単位で生成し、必ず使用者のレビューを受けてください
- ファイルの先頭にあるimport文を必ず確認して下さい

## コーディング規約 / Coding Standards

コーディングする時には以下の規約を遵守して下さい

- **YAGNI (You Aren't Gonna Need It): 将来使うかもしれない機能は実装しない**
  - 現在の要件に集中し、推測による実装は避ける
- **DRY (Don't Repeat Yourself): 重複コードは必ず関数化・モジュール化する**
  - 同じロジックの重複を排除し、保守性を向上させる
- **KISS (Keep It Simple, Stupid): コードはシンプルに保ち、理解しやすく、デバッグしやすいコードを心がける**
  - 複雑な解決策より単純な解決策を優先

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
