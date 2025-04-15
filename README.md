# 📘 学習管理システム 開発プラン

- 使用技術：**Laravel + Docker**
- 期間：**2ヶ月**

---

## 🎯 ゴール

- DockerでLaravelアプリを開発
- 学習時間の記録（開始・終了・休憩）
- 総学習時間の集計、目標達成の評価表示
- ユーザー認証、コメント・評価機能の追加

---

## 🗓 開発スケジュール

### ✅ Week 1：環境構築と設計
- [○] DockerでLaravel環境構築
- [○] Gitでバージョン管理開始
- [ ] 画面設計・ER図作成
- [ ] LaravelルーティングとMVC基礎理解
- [ ] トップページ＆「今日の記録」表示作成

---

### ✅ Week 2：学習記録の基本機能
- [ ] 開始ボタンで `start_time` 記録
- [ ] 休憩ボタンで `break_start` / `break_end` 記録（複数対応）
- [ ] 終了ボタンで `end_time` 記録 → 総学習時間を算出
- [ ] ボタンの活性 / 非活性制御
- [ ] 終了忘れアラート（例：20時に通知）

---

### ✅ Week 3：学習内容のCRUD機能
- [ ] 学習内容（タイトル・カテゴリ・内容）登録
- [ ] 一覧表示・編集・削除機能
- [ ] 学習時間と学習内容を紐づけ
- [ ] 動的フォーム追加（Vue or Alpine.js ※任意）

---

### ✅ Week 4：集計とバッチ処理準備
- [ ] 総学習時間を別テーブルに保存（1日ごと）
- [ ] 日単位の履歴画面追加（カレンダー形式など）
- [ ] CLIコマンドで前日分の集計処理作成

---

### ✅ Week 5：目標設定と評価表示
- [ ] 曜日ごとの目標時間をDBに登録
- [ ] 実績と比較して「優」「劣」評価を表示
- [ ] 一覧画面に評価ステータスを表示

---

### ✅ Week 6：バッチ処理とDocker連携
- [ ] Laravelのスケジューラーで自動集計
- [ ] Docker起動時にバッチ処理を実行
- [ ] 前日の記録の削除 or アーカイブ化
- [ ] FeatureTestなど簡単なテストコード追加

---

### ✅ Week 7：ログイン・ユーザー管理
- [ ] Laravel Breeze or Jetstreamで認証導入
- [ ] 学習記録をユーザー単位で管理
- [ ] 他人の記録閲覧、非公開設定など追加

---

### ✅ Week 8：コメント・SNS機能とUI改善
- [ ] コメント機能（他人の記録に対して）
- [ ] 評価ボタン（いいね・称賛など）
- [ ] TailwindCSSなどでUI強化
- [ ] デプロイ作業（Render / Vercel / VPSなど）

---

## 🗃 テーブル設計（例）

### study_sessions テーブル

| カラム名       | 型        | 説明                     |
|----------------|-----------|--------------------------|
| id             | integer   | 主キー                   |
| user_id        | integer   | 紐づくユーザーID         |
| date           | date      | 学習した日付             |
| start_time     | datetime  | 学習開始時間             |
| end_time       | datetime  | 学習終了時間             |
| total_minutes  | integer   | 合計学習時間（分単位）   |
| created_at     | timestamp | 作成日時                 |
| updated_at     | timestamp | 更新日時                 |

---

## 📚 学べること

- **Laravel**：ルーティング、MVC、認証、バッチ処理、CLI操作
- **Docker**：開発環境構築、DB連携、コンテナ運用
- **DB設計**：リレーション、マイグレーション、設計力の向上
- **フロント**：Blade / JavaScript / Alpine.js / TailwindCSS など
- **運用スキル**：GitHub管理、スケジューラー活用、デプロイ経験

---

🎉 完成すれば、Laravel中級者レベルのスキルが手に入る！
