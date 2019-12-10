# 投稿系API

### 画像投稿

##### Endpoint

```
POST /api/v1/post
```

##### Request

画像は最低１枚, 最大４枚含めることができる.  
`Content-Type` には `multipart/form-data` を指定する.

- １枚のパターン

```json
{
    "image1": <image-data>
}
```

- ４枚のパターン

```json
{
    "image1": <image-data>,
    "image2": <image-data>,
    "image3": <image-data>,
    "image4": <image-data>
}
```

##### Response

```json
{
    "post_id": 1
}
```

### テキスト投稿

テキストのみの投稿はできず, まずは画像投稿APIから `post_id` を得る必要がある.

##### Endpoint

```
POST /api/v1/post/text
```

##### Request

また, `post_id` には画像投稿APIを使用して取得したIDを指定する.

```json
{
    "post_id": 1,
    "text": "XXXX"
}
```

##### Response

```json
{}
```

### いいねする

##### Endpoint

```
POST /api/v1/post/like
```

##### Request

```json
{
    "post_id": 1
}
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

```json
{
    "post_id": 1
}
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
{
    "id": 1,
    "text": "XXXX",
    "images": [
        "XXXX", "XXXX", "XXXX", "XXXX"
    ],
    "liked": 1,
    "is_liked": true,
    "user": {
        "id": 1,
        "user_id": "XXXX",
        "screen_name": "XXXX",
        "avatar": "XXXX",
    },
    "liker": [
        {
            "user_id": 1,
            "avatar": "XXXX"
        }
    ],
    "created_at": "XXXX",
    "updated_at": "XXXX"
}
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