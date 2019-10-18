# ユーザー系API

### ログインユーザーのプロフィールの取得

##### Endpoint

```
GET /api/v1/user/profile
```

##### Request

- ログインユーザーのプロフィールの取得  
ヘッダに `Authorization: Bearer <access_token>` 形式でアクセストークンの指定が必須

```json
{}
```

- 指定したユーザーのプロフィールの取得

```json
{
    "user_id": "XXXX"
}
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

### フォロー一覧の取得

##### Endpoint

```
GET /api/v1/user/following
```

##### Request

- ログインユーザーのフォロー一覧の取得  
ヘッダに `Authorization: Bearer <access_token>` 形式でアクセストークンの指定が必須

```json
{}
```

- 指定したユーザーのフォロー一覧の取得

```json
{
    "user_id": "XXXX"
}
```

- 取得する範囲の指定  
以下の場合200〜299件目までを取得する  
指定しない場合, 最新100件を取得する

```json
{
    "page": 2
}
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

- ログインユーザーのフォロワー一覧の取得  
ヘッダに `Authorization: Bearer <access_token>` 形式でアクセストークンの指定が必須

```json
{}
```

- 指定したユーザーのフォロワー一覧の取得

```json
{
    "user_id": "XXXX"
}
```

- 取得する範囲の指定  
以下の場合200〜299件目までを取得する  
指定しない場合, 最新100件を取得する

```json
{
    "page": 2
}
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

ヘッダに `Authorization: Bearer <access_token>` 形式でアクセストークンの指定が必須

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

ヘッダに `Authorization: Bearer <access_token>` 形式でアクセストークンの指定が必須

```json
{}
```

### プロフィールを編集する

##### Endpoint

```
PATCH /api/v1/user/profile
```

##### Request

ヘッダに `Authorization: Bearer <access_token>` 形式でアクセストークンの指定が必須

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

### ユーザーの投稿の取得

##### Endpoint

```
GET /api/v1/user/posts
```

##### Request

- ログインユーザーの投稿の取得  
ヘッダに `Authorization: Bearer <access_token>` 形式でアクセストークンの指定が必須

```json
{}
```

- 指定したユーザーの投稿の取得

```json
{
    "user_id": "XXXX"
}
```

- 取得する範囲の指定  
以下の場合200〜299件目までを取得する  
指定しない場合, 最新100件を取得する

```json
{
    "page": 2
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

ヘッダに `Authorization: Bearer <access_token>` 形式でアクセストークンの指定が必須

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