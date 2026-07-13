# sns-unyou-assets

`sns-unyou`（SNS運用プロジェクト本体・非公開）から投稿する画像のうち、外部APIに「公開HTTPS URL」として渡す必要があるものだけを置く公開リポジトリ。

## 用途

Instagram Graph API（`.claude/skills/instagram-api/`）はカルーセル画像を `image_url` パラメータでサーバーサイド取得する方式のため、投稿処理の実行時点で認証なしにアクセスできる公開URLが必要。Canvaの`export-design`が返すダウンロードURLは数時間で失効するため、投稿承認までに日をまたぐ運用（スプレッドシートでの事前スケジュール）に耐えられない。そのため、生成した画像をここに置いて恒久的な公開URL（`raw.githubusercontent.com`）を得る。

## 配置ルール

```
<account>/instagram/<slug>/slide-<N>.jpg
```

例：`kurabel/instagram/tsubotanka-ranking/slide-1.jpg`

## 参照URL

```
https://raw.githubusercontent.com/kyky1109-sys/sns-unyou-assets/main/<account>/instagram/<slug>/slide-<N>.jpg
```

## 注意

- ここに置くのは投稿予定・投稿済みの画像のみ。企画メモや未公開の検討中コンテンツは置かない（公開リポジトリのため）
- 画像自体はいずれ実際にInstagramへ公開されるものなので、事前ホスティングによる追加の情報漏洩リスクは実質的にない
