このリポジトリは Java 教材作成プロジェクトです（HTML教材＋サンプルJava）。
Claude Code に依頼するときは、まず `.cursorrules` を読み、そこにある「絶対ルール」を必ず守ってください。

---

## 重要（絶対ルールの参照先）

- **最優先**: `.cursorrules`
  - HTML出力ルール（bodyのみ/1行目タイトル/JS・styleタグ禁止/インラインstyle）
  - Java規約（var禁止、用語統一、protected禁止、インデントはタブ等）
- **補助**: `_doc/`
  - `_doc/4-デザインルール.md`（details/summary、区切り線、解答ブロックなど）
  - `_doc/0-基本ルール.md`（構成の考え方、参照の集約）
  - `_doc/3-EXERCISE.md`（練習問題フォーマット）

---

## 現状（ここまで完了）

- Unit03（DAO参照系）まで完了済み。
- 「練習問題の題材は動物/社員のみ」といった固定ルールは撤去済み（今後Web教材では動物/社員は題材として使わない方針）。

---

## これからの作業方針（Unit04_DAO_Update から）

### ゴール
- **Unit04_DAO_Update** を起点に、DAO更新系（INSERT/UPDATE/DELETE）とトランザクションを扱う教材を整備する。
- 次のWeb単元へ繋げやすいように、**更新件数**・**例外時のrollback**・**同一Connectionの重要性**が伝わる構成にする。

### 題材（DB）
- DB題材は **商品DB** または **社員DB** を参照する（方針）。
- 難易度設計は次のイメージ：
  - **テキストのサンプル**: 単表で簡単なCRUD（例：商品 items）
  - **練習問題（難しい方）**: 関連テーブルあり（例：emps / depts のJOINやプルダウン選択）

※ 実際の採用題材・テーブル名は既存Unit（Unit01〜03）で使っているDBに合わせる。

---

## Unit04 の作業チェックリスト（依頼テンプレ）

Claude Code への依頼は、次を上から順にやってください。

1. `Unit04_DAO_Update/01-テキスト-DAO更新とトランザクション.html` の構成を見直し
   - 更新系は `executeUpdate()` と「更新件数」を強調
   - トランザクションは `setAutoCommit(false)` → `commit/rollback` → `finally` で `true` に戻す流れ
2. `Unit04_DAO_Update/03-練習問題-DAO更新とトランザクション.html` の問題設計
   - 基本（単発更新）→ 発展（同一Connectionで複数操作を1トランザクション）の段階
3. PDFが必要なら `Unit04_DAO_Update/src/template.html` と `scripts` の生成手順に合わせて整合
4. 文言・表記の整合
   - 「動物」「社員」を“題材”として使わない（DBの `emps/depts` などの説明として必要な範囲は可）
   - 用語・デザインは `.cursorrules` と `_doc/4-デザインルール.md` に合わせる

---

## 依頼するときに渡す情報（最小）

- どの単元（Unit04〜）を、どの題材（商品/社員）で進めるか
- テキストを「単表」、練習問題を「関連あり」にする方針でOKか
- JSTL導入のタイミング
  - **Unit08（JSP & JavaBeans）の後半で最小導入**（`c:out` / `c:forEach` / `c:if`）
  - Unit09（演習）以降は **JSTL前提**で問題を作る

