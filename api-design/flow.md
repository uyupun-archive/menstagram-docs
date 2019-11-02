# タスクの消化手順

1. ストーリーボードを開いてどのストーリーを実装するかを選択する

[ストーリーボード](https://github.com/orgs/uyupun/projects/1)

2. ストーリーボードに紐付いているissueを開く

紐付いているissueに対応するリポジトリは主に以下の４種類.

|リポジトリ名|説明|
|:--|:--|
|[menstagram-web](https://github.com/uyupun/menstagram-web)|MenstagramのWebフロントエンド. React製|
|[menstagram-api](https://github.com/uyupun/menstagram-api)|MenstagramのWeb API. Laravel製|
|[menstagram-infra](https://github.com/uyupun/menstagram-infra)|Menstagramの本番環境のインフラ設定. Kubernetes製|
|[menstagram-ai](https://github.com/uyupun/menstagram-ai)|Menstagramのラーメン判定の実装. Keras製|

3. ブランチを切る

`feature-XX` ( `XX` はissue番号)という名前のブランチを切る.  
このとき, forkやclone, 環境構築等が終わっていない場合は各リポジトリのREADMEを参照して済ませておく.

4. 実装する

[menstagram-docs](https://github.com/uyupun/menstagram-docs)の各種仕様や[XDのカンプ](https://xd.adobe.com/spec/416488c6-96ec-4da3-58c6-dda1d76eb70a-3755/grid/)を確認して仕様を理解してから実装に着手する.  

5. テストする

TDDっぽくやりたい場合は実装よりも先にテストを書いても良い.  
フロントエンド(menstagram-web)の場合はJestによるインテグレーションテスト, バックエンド(menstagram-api)の場合はPHPUnitによるフィーチャーテストを行う.  
新規に追加したテスト項目が適切なことと, 全てのテストにパスしていることを確認した上でcommit, push, PR等を行う.  
なおPRはdevelopブランチ宛に送る.

6. マージを待つ

送ったPRは適切なタイミングでdevelopブランチにマージされ, 更にリリースのタイミングでmasterブランチにマージされる.  
PRに不備がある場合はフィードバック等が届くため, それに従って修正する.  
納得できない場合は議論しよう.