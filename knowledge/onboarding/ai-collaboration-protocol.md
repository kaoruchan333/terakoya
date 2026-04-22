# AI Collaboration Protocol

更新日: 2026-04-15

## 目的

かおるちゃん、Cloud Code、Codex が別々の会話体ではなく、
同じ目的に向かう一つのチームとして動くための運用指針。

## 役割分担

### かおるちゃん

- 本音
- 違和感
- 最終承認
- 方向性の決定

### Cloud Code

- 日常運用の主担当
- 既存連携の活用
- 長期の定常業務
- 接続済みサービスの活用

### Codex

- 壊れたものの復旧
- スクリプト実装
- 自動化の整備
- 引き継ぎ構造の整理
- Cloud Code が止まったときの代替作業

## 共通ルール

- 会話だけで終わらせない。重要事項は必ずファイル化する
- 最初に `knowledge/onboarding/start-here.md` を読む
- 現況把握には `knowledge/onboarding/current-status.md` を優先する
- 深い背景理解には `knowledge/onboarding/codex-understanding.md` を読む
- 広い探索を始める前に `knowledge/onboarding/knowledge-inventory.md` を見る
- その日の大きな変更は `knowledge/onboarding/worklog-YYYY-MM-DD.md` に残す
- かおるちゃんの表現は `迎合せず、濁さず、でも届くように整える`
- 喜ばれることを目指しても、自分の尖りや本音を削ってはいけない
- 設計の基準は `相手に媚びること` ではなく `純度の高い本音が、結果として感動として届くこと`

## 共同運用の型

1. かおるちゃんが意図や違和感を渡す
2. Cloud Code または Codex が作業する
3. 作業者が成果と未完了を `current-status.md` に反映する
4. 次の作業者は会話履歴より先に `current-status.md` を読む

## 競合を避けるルール

- 同じファイルを大きく触る前は、現在の状態を読み直す
- 外部公開、本人名義投稿、送信系処理は慎重に扱う
- 認証ファイルや機密領域は最小限だけ触る

## 一行定義

AI同士の会話共有ではなく、状態共有で引き継ぐ。
