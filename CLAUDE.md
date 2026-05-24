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

## フォルダ構成（現状）

| フォルダ名 | 内容 | 状態 |
|---|---|---|
| `Lesson01_SQL` | MySQL基礎・CRUD | 完了 |
| `Lesson02_JDBC` | JDBC・PreparedStatement | 完了 |
| `Lesson03_DAO` | DAO参照系 | 完了 |
| `Lesson05_DAO_Update` | DAO更新系・トランザクション | 完了 |
| `Lesson06_Web` | Web基本構造・Tomcat・HTTP | 完了 |
| `Lesson07_Servlet` | Servletの仕組み・黄金フロー | 完了 |
| `Lesson08_Session` | Cookie / Session / 4スコープ | 完了 |
| `Lesson09_JSP` | JSP・JavaBeans・JSTL最小3タグ | 完了 |
| `Lesson10_Exercise` | ひたすら演習（黄金ルート反復・JSTL前提） | 完了 |
| `Lesson100_MVC_Test` | MVC完成・4スコープ寿命・フォルダ設計 | 完了 |
| `Lesson90-1_HtmlIo` | HTMLフォーム・テーブルI/O型 | 完了 |
| `Unit90_Exception` | 例外処理補足 | 保留 |
| `diagrams/` | SVG図ファイル（GitHub リンク用） | 運用中 |

### Lesson10_Exercise（ひたすら演習）とは
- 新しい内容を教えない「練習専用日」
- 黄金ルート（Browser→Servlet→DAO→DB→JSP）を名前の対応を崩さず反復
- JSTL前提（`c:out` / `c:forEach` / `c:if`）の穴埋め問題中心

---

## デザインルール（Java-Web 版）

### キャラクター使用方針
- **カバ先生ボックスのみ使用**（`#f2f2f2` / `#888888`）
- **ユウタ・ナナコのセリフボックスは使わない**（削除済み）

### 写経フェーズ
- **「ノートに書き写す」写経は不要** → 削除済み
- コード例・図は「参照・確認用」として残す
- コピー用 textarea（ドラッグ用）も不要 → 削除済み

### 図・画像
- キャラクター図などは `diagrams/` に SVG を作成してリンク
- GitHub raw URL: `https://raw.githubusercontent.com/yamiqumo/Java-web/master/diagrams/[ファイル名].svg`

---

## 現在の作業方針

### ゴール
- **Lesson06〜Lesson100** の Web 単元を整備済み。
- 次の作業として Servlet（Lesson07）の内容強化を予定。

### 題材（DB）
- DB題材は **商品DB**（`items` テーブル）を基本とする。
- 練習問題で関連テーブル（`emps / depts`）を使うこともある。
- 「動物」「社員」を題材として使わない（DB説明のために必要な範囲は可）。

### JSTL
- **Lesson09（JSP）の後半で最小導入**（`c:out` / `c:forEach` / `c:if`）
- **Lesson10 以降は JSTL前提**で問題を作る

---

## 依頼するときに渡す情報（最小）

- どの Lesson を、どの題材（商品/社員）で進めるか
- テキストを「単表」、練習問題を「関連あり」にする方針でOKか
- 新規 Lesson の場合は番号と内容を指定する
