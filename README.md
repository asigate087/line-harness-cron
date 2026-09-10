# line-harness-cron

line-crm-worker（LINEステップ配信）の外部スケジューラー。

Cloudflare cron トリガーがアカウント側の問題で発火しないため、
GitHub Actions が5分おきに配信エンドポイント `/api/cron/run` を呼び出す。

- 認証: リポジトリシークレット `WORKER_API_KEY`
- Cloudflare cron が復旧したら Actions タブからこのワークフローを Disable にする
- 注意: GitHub の仕様で、リポジトリに60日間コミットがないと scheduled workflow は自動停止する
