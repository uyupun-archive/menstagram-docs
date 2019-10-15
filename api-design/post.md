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
GET /api/v1/post/detail?post_id=XXXX
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