# ユーザー系API

### ログインユーザーのプロフィールの取得

##### Endpoint

```
GET /api/v1/user/profile
```

##### Request

```json
{}
```

##### Response

```json
{
    "id": 1,
    "avatar": "XXXX",
    "screen_name": "XXXX",
    "user_id": "XXXX",
    "posted": 1,
    "following": 1,
    "followed": 1,
    "biography": "XXXX"
}
```

### 特定のユーザーのプロフィールの取得

##### Endpoint

```
GET /api/v1/user/profile?user_id=XXXX
```

##### Request

```json
{}
```

##### Response

```json
{
    "id": 1,
    "avatar": "XXXX",
    "screen_name": "XXXX",
    "user_id": "XXXX",
    "posted": 1,
    "following": 1,
    "followed": 1,
    "biography": "XXXX"
}
```

### ログインユーザーのフォローの取得

##### Endpoint

```
GET /api/v1/user/following
```

##### Request

```json
{}
```

##### Response

```json
[
    {
        "user_id": "XXXX",
        "screen_name": "XXXX",
        "avater": "XXXX"
    },
    {
        "user_id": "XXXX",
        "screen_name": "XXXX",
        "avater": "XXXX"
    }
]
```

### 特定のユーザーのフォローの取得

##### Endpoint

```
GET /api/v1/user/following?user_id=XXXX
```

##### Request

```json
{}
```

##### Response

```json
[
    {
        "user_id": "XXXX",
        "screen_name": "XXXX",
        "avater": "XXXX"
    },
    {
        "user_id": "XXXX",
        "screen_name": "XXXX",
        "avater": "XXXX"
    }
]
```

### ログインユーザーのフォロワーの取得

##### Endpoint

```
GET /api/v1/user/followed
```

##### Request

```json
{}
```

##### Response

```json
[
    {
        "user_id": "XXXX",
        "screen_name": "XXXX",
        "avater": "XXXX"
    },
    {
        "user_id": "XXXX",
        "screen_name": "XXXX",
        "avater": "XXXX"
    }
]
```


### 特定のユーザーのフォロワーの取得

##### Endpoint

```
GET /api/v1/user/followed?user_id=XXXX
```

##### Request

```json
{}
```

##### Response

```json
[
    {
        "user_id": "XXXX",
        "screen_name": "XXXX",
        "avater": "XXXX"
    },
    {
        "user_id": "XXXX",
        "screen_name": "XXXX",
        "avater": "XXXX"
    }
]
```

### フォローする

##### Endpoint

```
POST /api/v1/user/follow
```

##### Request

```json
{}
```

##### Response

```json
{}
```

### フォローをはずす

##### Endpoint

```
POST /api/v1/user/unfollow
```

```json
{}
```

##### Response

```json
{}
```

### プロフィールを編集する

##### Endpoint

```
PATCH /api/v1/user/profile
```

##### Request

```json
{
    "screen_name": "XXXX",
    "biography": "XXXX"
}
```

##### Response

```json
{}
```

### ログインユーザーの投稿の取得

##### Endpoint

```
GET /api/v1/user/posts
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
        "liked": 1
    }
]
```

### 特定のユーザーの投稿の取得

##### Endpoint

```
GET /api/v1/user/posts?user_id=XXXX
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
        "liked": 1
    }
]
```

### ログインユーザーがいいねした投稿の取得

##### Endpoint

```
GET /api/v1/user/likes
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
        "liked": 1
    }
]
```