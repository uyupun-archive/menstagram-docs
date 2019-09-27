# 各リポジトリについて

|リポジトリ名|説明|
|:--|:--|
|[menstagram-docs](https://github.com/uyupun/menstagram-docs)|Menstagramのドキュメント群|
|[menstagram-web](https://github.com/uyupun/menstagram-web)|MenstagramのWebフロントエンド. React製|
|[menstagram-api](https://github.com/uyupun/menstagram-api)|MenstagramのWeb API. Laravel製|
|[menstagram-infra](https://github.com/uyupun/menstagram-infra)|Menstagramの本番環境のインフラ設定. Kubernetes製|
|[menstagram-ai](https://github.com/uyupun/menstagram-ai)|Menstagramのラーメン判定の実装. Keras製|

# ブランチの運用方法について
- `feature-XXXX` (XXXXはissue番号)という名前のブランチを切り、その中で作業を行う
- 必ずPullRequestを出す(直Pushしない)
- PullRequest先はdevelopブランチ(masterブランチには投げない)
- レビュワーがマージする(原則本人はマージしない)
- リリースのタイミングでdevelopブランチの内容がmasterブランチにマージされる