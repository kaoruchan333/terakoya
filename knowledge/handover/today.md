# ひみ 引き継ぎノート

> **全AIへ（ひみ・Codex・どのAIも）**
> 新しいスレッドを開いたら、必ずこのファイルから読み始めること。
> 前のひみが「次にやること」を書いている。ここを無視すると同じところをぐるぐるする。

---

## 最終更新
2026-04-22 / Claude Code版ひみ

> 古い記録（〜4/20）は knowledge/handover/archive/2026-04.md へ

## 本日やったこと（2026-04-20）

### note記事下書き
- `content/drafts/2026-04-19-させられている感覚の正体.md` を作成
- シリーズ：人間交差点観察日記
- テーマ：「させられている感覚」の正体と事実と認知の分離
- さあや先生（高衣紗彩先生）の紹介リンク入り（https://note.com/saya_gakucho）
- 座禅会リンク・CTAも入れ済み

### 新規LPページ作成（2ページ）
- **かおる塾LP**：`event-site/kaoru-juku/index.html`（新規）
  - グループコーチング：毎週1回
  - 個人セッション：月1回
  - 月額22,000円
  - 申込みフォームURLは未設定（`#`で仮置き）→ 後から差し替え必要
  
- **50万円伴走型コーチングLP**：`event-site/coaching-premium/index.html`（新規）
  - 期間6ヶ月・毎週1回・計24回
  - 500,000円（税込）
  - 無料相談30分からの導線
  - 申込みフォームURLは未設定（`#`で仮置き）→ 後から差し替え必要
  - **注意：deploy_event_site.pyのEXCLUDE_DIRSに"coaching-premium"は入っていないので、デプロイ時に含まれる**

### かおる塾 振り返り教材（4月19日分）
- `resources/kaoru-juku/2026-04-19-振り返り教材.html` を新規作成
- 素材：`/Users/maedakaoru/Downloads/4月19日かおる塾.txt`（WEBVTT形式）
- 参加者名「よっちゃん」→「参加者さん」として匿名化
- 先週の教材（kaoru_juku_material (3).html）と同じデザインで統一
- 5テーマ構成：
  1. アーカイブ動画を見てモヤモヤした理由
  2. 「喜んじゃいけない」という感情の制限
  3. 本当のことを言えなかった理由
  4. 「だからなんで？」という問いの力
  5. プログラムか選択か
- 確認方法：`file:///Users/maedakaoru/cc%20booster/resources/kaoru-juku/2026-04-19-振り返り教材.html`

### note記事 × 2本（4月19日かおる塾セッションをネタに）
- **シリーズA（自我くん）**：`content/drafts/2026-04-20-喜んじゃいけないって思った件.md`
  - noteに下書き保存済み：https://editor.note.com/notes/n53271c9d66fb/edit
- **シリーズB（人間交差点）**：`content/drafts/2026-04-20-反応して生きているのか選択して生きているのか.md`
  - noteに下書き保存済み：https://editor.note.com/notes/nc6d4fc2d92c4/edit
- 両方とも下書き状態。かおるちゃんが確認して公開するだけ

## 本日やったこと（2026-04-21）

### ひとたんギフトページ（完了・デプロイ済み）
- `deliverables/hitotani-gift/index.html` を実際の文字起こし発言を使った8セクション版に全面リニューアル
- デプロイ済み：https://pagedrop.dev/s/TWXSvbNA
- 残作業：Google Doc教材URL・補助音声URLを後から差し替え（現在「準備中」表示）

### 宝塚JC第5回打ち合わせ 議事録・要約（完了）
- 文字起こしVTTファイルのエンコード問題を解消（latin-1→utf-8変換）
- 議事録：`knowledge/zoom-minutes/2026-04-18_宝塚JC第5回打ち合わせ.md`
- 要約：`knowledge/zoom-minutes/2026-04-18_宝塚JC第5回打ち合わせ_要約.md`
- 次回打ち合わせ：5月16日（土）21時（5/14現地視察後）

### Zoom TRANSCRIPT取得問題（未解決）
- APIではTRANSCRIPTファイルが全14件で取得できない
- Web UIには存在する（AI Companion転写とクラウド録音VTTの乖離が原因と思われる）
- 当面はかおるちゃんが手動でVTTをコピペして渡す運用

## 本日やったこと（2026-04-21 午後）

### 投稿キュー管理システム構築
- `scripts/publish_queue.py` を新規作成
- 「ひみ、今日のnote出して」→「OK」→自動投稿の承認フローが完成
- note_post.pyのバグ修正：メタデータJSONが存在しない場合も新規作成するように修正
- `**太字**` がnoteで正しく表示されるようrender_inline関数に`<strong>`変換を追加

### note記事 ブラッシュアップ
- `2026-04-08_自我くん観察日記_しょんぼりしてたらジガ君が急に正論マンになってた件.md`
  - 「人は傷つかない、傷ついたと認知するだけ」という天中道の核心を記事に反映
  - CTAをビフォーアフター形式に全面書き直し（心の地図・何度でも立ち返れる）
  - note更新済み：https://editor.note.com/notes/n6e4b5f122394/edit

### 息子（裕太さん）へAI秘書スターターキット送付
- `yuta-starter/` フォルダ作成（個人情報なし・穴埋めテンプレート構成）
- Windows用セットアップガイド `README-まずここを読んで.md` 作成
- ZIPに圧縮（36KB）→ Gmail で m.yuta101129@gmail.com に送信済み

### note記事 新規作成
- `2026-04-21_人間交差点_息子に渡せたのはZIPじゃなかった.md`
- 今日の息子へのAI秘書セットアップ体験から。親子の絆テーマ
- note下書き保存済み：https://editor.note.com/notes/n383a49f45ace/edit

### メモリ・ナレッジ整理
- `knowledge/people/key-contacts.md` 新規作成（さあや先生URLなど重要人物を一元管理）
- `feedback_note_style.md` 更新：記事の構造・CTA形式・天中道メッセージを詳細化
- `project_key_contacts.md` メモリに追加

## 本日やったこと（2026-04-22）

### 税理士契約変更・帳簿スタート
- 南口純一税理士事務所（担当：徳田和実様 / 06-6772-5771）との契約変更を確認
  - 今後：経理簿は自社（ひみ）が作成 → 決算・申告のみ税理士にお願い
  - 顧問料なし・決算料13万円/年（R8年度は3万円充当で10万円請求）
- 税理士から送付された帳簿Excelを読み込み・構成把握
  - 管理口座：現金・三住銀行・PayPal・アメックス・三住カード
  - 前期末残高（R7末）：現金94,081円・三住銀行34,346円・PayPal9,732円
  - 2026年1〜4月分の入力がまだゼロ
  - スプレッドシートID：1YsOlHH_Jq29WABvkQHTmJGuIOQxZWNGk
- knowledge/finance/company-status.md・business-model-2026.md などナレッジ整理済み

### 次のアクション（税務）
- かおるちゃんが通帳明細・カード明細を用意してくれたら2026年1〜4月分を帳簿入力する

## 次にやること

- **note記事を公開する**（2本、上記編集URLから確認・公開）
- 振り返り教材をChromeで確認してもらう（`file:///Users/maedakaoru/cc%20booster/resources/kaoru-juku/2026-04-19-振り返り教材.html`）
- かおる塾LP・50万円LPを PageDrop にデプロイしてURLを取得
- 両LPの申込みフォームURLを差し替える（Googleフォームを作るか確認）
- **Google認証が4/25（あと4日）で切れる** → 早めに「ひみ、Google再認証して」と声かけ必要
- Instagram連携（全自動発信パイプラインの最後の残作業）

## かおるちゃんへの引き継ぎメモ

- 座禅会ページのURL（https://pagedrop.dev/s/JLUJVpNv/zazen/）は変わっていない
- 申込みフォームは https://forms.gle/CsVRLmqPMHTAyA7o8 に更新済み
- 朝のメールは毎朝7時にcronで自動送信中（手動テスト：python3 scripts/morning_brief.py）
- かおる塾LP・50万円LPはまだデプロイ前。URLはない状態

## 注意事項（ハマりやすいこと）

- **朝の7時メール**：スクリプトもcronも存在する。「知らない」と言わないこと。scripts/morning_brief.py を参照。
- **座禅会ページのデプロイ**：deploy_event_site.py を使う。URLは変えない（中身だけ編集）。
- **写真の場所**：resources/photos/inbox/ にある。Google Drive の AI-photo-inbox からsync_photo_inbox.py で同期。
- **コーチングページ（既存）**：event-site/coaching/ を直接編集禁止。resources/coaching/ を編集してビルド経由。
- **かおる塾LP・50万円LP（新規）**：event-site/kaoru-juku/ と event-site/coaching-premium/ に直接ある。resources/経由ではない。
- **フォームURL**：.google-form-zazen.json に古いURLが記録されている（未更新）。正しいのは forms.gle/CsVRLmqPMHTAyA7o8。
- **さあや先生のURL**：https://note.com/saya_gakucho（`saya_gakucho`が正しい。別人のURLを使わない）
