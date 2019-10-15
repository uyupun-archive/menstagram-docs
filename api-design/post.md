# 投稿系API

### 投稿

##### Endpoint

```
POST /api/v1/post
```

##### Request

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

### 特定のユーザーの投稿を取得する

##### Endpoint

```
GET /api/v1/post?user_id=XXXX
```

##### Request

```json
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
        "likes": 1
    }
]
```

### いいね

##### Endpoint

```
POST /api/v1/post/like
```

##### Request

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
GET /api/v1/post?post_id=XXXX
```

##### Request

```json
{}
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
        "likes": [
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