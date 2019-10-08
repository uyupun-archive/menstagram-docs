# DB設計

## usres
ユーザー

|カラム名|型|属性|説明|
|:--|:--|:--|:--|
|id|bigIncrements|-|数値のID. ユーザーによる変更が不可|
|user_id|varchar|unique|ユーザーが任意に設定できるID. 半角英数字のみ|
|password|text|-|ハッシュ化されたパスワード|
|access_token|text|nullable|アクセストークン|
|screen_name|varchar|-|ユーザー表示名, 日本語|
|avatar|text|-|ユーザーアイコン画像|
|biography|text|-|ユーザーの自己紹介欄|
|created_at|timestamps|-|作成された日付. Laravelによってデフォルトで生成される|
|updated_at|timestamps|-|更新された日付. Laravelによってデフォルトで生成される|


## posts
ラーメン投稿
|カラム名|型|属性|説明|
|:--|:--|:--|:--|
|id|bigIncrements|-|数値のID. ユーザーによる変更が不可|
|user_id|unsigned int|references|投稿主ユーザーID(主キー)|
|text|text|-|ラーメン食った報告とかのテキスト|
|images|json|-|画像パスのJSON, 最大四枚で1枚以上必須|
|created_at|timestamps|-|作成された日付. Laravelによってデフォルトで生成される|
|updated_at|timestamps|-|更新された日付. Laravelによってデフォルトで生成される|


## likes
投稿いいね
|カラム名|型|属性|説明|
|:--|:--|:--|:--|
|id|bigIncrements|-|数値のID. ユーザーによる変更が不可|
|user_id|unsigned int|references|いいねしたユーザーのID|
|post_id|unsigned int|references|いいねする投稿のID|
|created_at|timestamps|-|作成された日付. Laravelによってデフォルトで生成される|
|updated_at|timestamps|-|更新された日付. Laravelによってデフォルトで生成される|

## Notices
通知
|カラム名|型|属性|説明|
|:--|:--|:--|:--|
|id|bigIncrements|-|数値のID. ユーザーによる変更が不可|
|user_id|unsigned int|references|通知送り先のユーザーID|
|type|integer|-|通知の種類|
|from_user_id|unsigned int|references|通知送信元のユーザーID|
|text|text|-|通知内容の文章|
|created_at|timestamps|-|作成された日付. Laravelによってデフォルトで生成される|
|updated_at|timestamps|-|更新された日付. Laravelによってデフォルトで生成される|