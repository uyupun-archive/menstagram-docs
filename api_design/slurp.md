# スラープ系API

### スラープ

##### Endpoint

```
POST /api/v1/slurp
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
ラーメン判定成功時(全ての判定に成功した場合)は `slurp_id` に任意の非負整数, `is_ramens` にそれぞれの判定結果が入ったレスポンスが返却される.  
ラーメン判定失敗時(１枚でも判定に失敗した場合)は `slurp_id` に `0` , `is_ramens` にそれぞれの判定結果が入ったレスポンスが返却される.

```json
{
    "slurp_id": 1,
    "is_ramens": [
        true,
        false,
        true,
        false
    ]
}
```

### スラープ(テキスト)

テキストのみのスラープはできず, まずはスラープAPIから `slurp_id` を得る必要がある.

##### Endpoint

```
POST /api/v1/slurp/text
```

##### Request

また, `slurp_id` にはスラープAPIを使用して取得したIDを指定する.

```json
{
    "slurp_id": 1,
    "text": "XXXX"
}
```

##### Response

```json
{}
```

### ヤムする

##### Endpoint

```
POST /api/v1/slurp/yum
```

##### Request

```json
{
    "slurp_id": 1
}
```

##### Response

```json
{}
```

### ヤムをはずす

##### Endpoint

```
POST /api/v1/slurp/unyum
```

##### Request

```json
{
    "slurp_id": 1
}
```

##### Response

```
{}
```

### スラープ詳細の取得

##### Endpoint

```
GET /api/v1/slurp/detail
```

##### Request

```json
{
    "slurp_id": 1
}
```

##### Response
`yums` は最大５件まで取得する.

```json
{
    "id": 1,
    "text": "XXXX",
    "images": [
        "XXXX", "XXXX", "XXXX", "XXXX"
    ],
    "yum_count": 1,
    "is_yum": true,
    "user": {
        "id": 1,
        "user_id": "XXXX",
        "user_name": "XXXX",
        "avatar": "XXXX",
    },
    "yums": [
        {
            "user_id": 1,
            "avatar": "XXXX"
        }
    ],
    "created_at": "XXXX",
    "updated_at": "XXXX"
}
```

### ヤムしたユーザー一覧の取得

##### Endpoint

```
GET /api/v1/slurp/yums
```

##### Request
取得件数の指定等はできず, 最新から最大100件取得する.

```json
{
    "slurp_id": 1
}
```

##### Response

```json
[
    {
        "user_id": "XXXX",
        "user_name": "XXXX",
        "avater": "XXXX",
        "is_follow": true,
        "is_me": false
    }
]
```

### ラーメン判定

スラープAPIが内部的に使用する

##### Endpoint

```
POST /api/v1/ramen/judge
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
"is_ramens": [
    true,
    false,
    true,
    false
]
```