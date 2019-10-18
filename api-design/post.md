# 投稿系API

### 投稿

##### Endpoint

```
POST /api/v1/post
```

##### Request

ヘッダに `Authorization: Bearer <access_token>` 形式でアクセストークンの指定が必須

```json
{
    "text": "XXXX",
    "images": [
        "XXXX", "XXXX", "XXXX", "XXXX"
    ]
}
```

##### Response

```json
{}
```

### いいね

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
                "user_id": "XXXX"
            },
            {
                "user_id": "XXXX"
            }
        ]
    }
]
```