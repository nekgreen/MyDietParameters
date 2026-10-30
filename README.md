# MyDietParameters

体重管理ダッシュボード。スマホ・デスクトップ両対応の静的サイトです。

## 公開方法

1. `index.html` と `data.json` をリポジトリの **main ブランチ直下**にアップロード。
2. GitHub リポジトリの **Settings → Pages** を開く。
3. **Build and deployment** の Source を **Deploy from a branch**、Branch を **main / (root)** にして Save。
4. 公開後、GitHub Pages のURLで表示。反映に時間がかかる場合があります。

## 更新

`data.json` の `records` に次の形式で記録を追加してコミットすると公開画面に反映されます。

```json
{"date":"2026-10-31","weight":96.8}
```

日付は `YYYY-MM-DD`、weight は kg の数値。目標は `goalWeight`、身長は `heightCm` から設定可能。7日平均は暦上の直近7日間で計算します（データのある日のみ）。表示の「記録した日数」は実際の入力件数です。

**注意:** このリポジトリは公開リポジトリです。体重・計測日が誰でも見られます。あすけんの食事詳細や個人情報は含めないでください。

**現在の制約:** Googleスプレッドシートからの自動同期はまだありません。現時点は2026-10-30までのデータを静的JSONに記録しています。
