# 投稿系API

### 投稿

基本的に画像送信API(次節で説明)を使用して `post_id` を取得した場合のみしか使用できない.  

##### Endpoint

```
POST /api/v1/post
```

##### Request

ヘッダに `Authorization: Bearer <access_token>` 形式でアクセストークンの指定が必須.  
また, `post_id` には画像送信APIを使用して取得したIDを指定する.

```json
{
    "post_id": 1,
    "text": "XXXX"
}
```

##### Response

```json
{
    "can_posted": true
}
```

### 画像送信

画像投稿の場合, 投稿に先立って画像を送信する.

##### Endpoint

```
POST /api/v1/post/media
```

##### Request

画像は最低１枚, 最大４枚含めることができる.

```
multipart/form-data
```

##### Response

```json
{
    "post_id": 1
}
```

### いいねする

##### Endpoint

```
POST /api/v1/post/like
```

##### Request

ヘッダに `Authorization: Bearer <access_token>` 形式でアクセストークンの指定が必須

```json
{}
```

##### Response

```json
{}
```

### いいねをはずす

##### Endpoint

```
POST /api/v1/post/unlike
```

##### Request

ヘッダに `Authorization: Bearer <access_token>` 形式でアクセストークンの指定が必須

```json
{}
```

##### Response

```
{}
```

### 投稿詳細の取得

##### Endpoint

```
GET /api/v1/post/detail
```

##### Request

```json
{
    "post_id": 1
}
```

##### Response

```json
[
    {
        "id": 1,
        "text": "XXXX",
        "images": [
            "XXXX", "XXXX", "XXXX", "XXXX"
        ],
        "liked": 1,
        "liker": [
            {
                "user_id": "XXXX",
                "avatar": "XXXX"
            },
            {
                "user_id": "XXXX",
                "avatar": "XXXX"
            }
        ],
        "created_at": "XXXX",
        "updated_at": "XXXX"
    }
]
```

### いいねした人一覧の取得

##### Endpoint

```
GET /api/v1/post/liker
```

##### Request

```json
{
    "post_id": 1
}
```

- 取得する範囲を指定する  
20〜29件目までを取得する

```json
{
    "post_id": 1,
    "page": 2
}
```

- 取得する個数を指定する

```json
{
    "post_id": 1,
    "take": 5
}
```

##### Response

```json
[
    {
        "id": 1,
        "user": {
            "user_id": "XXXX",
            "screen_name": "XXXX",
            "avater": "XXXX"
        }
    }
]
```

### ラーメン判定

投稿APIが内部的に使用する

// TODO