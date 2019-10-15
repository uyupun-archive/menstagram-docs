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

### グローバルタイムラインの取得

##### Endpoint

```
/api/v1/post/tl/global
```

##### Request

```json

```

##### Response

```json

```

### プライベートタイムラインの取得

##### Endpoint

```
/api/v1/post/tl/private
```

##### Request

```json

```

##### Response

```json

```

### 特定のユーザーの投稿の取得

##### Endpoint

```
GET /api/v1/post/user/XXXX
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
        "like": 1
    }
]
```

### いいねした投稿一覧の取得

##### Endpoint

```
GET /api/v1/post/liked
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
        "like": 1
    }
]
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