# ユーザー系API

### ログインユーザーのプロフィールの取得

##### Endpoint

```
GET /api/v1/user/profile
```

##### Request

- ログインユーザーのプロフィールの取得

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
    "is_followed": false,
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
        "avater": "XXXX",
        "is_follwed": true
    },
    {
        "user_id": "XXXX",
        "screen_name": "XXXX",
        "avater": "XXXX",
        "is_follwed": true
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
        "avater": "XXXX",
        "is_follwed": false
    },
    {
        "user_id": "XXXX",
        "screen_name": "XXXX",
        "avater": "XXXX",
        "is_follwed": false
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
{
    "target_user_id": "XXXX"
}
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
{
    "target_user_id": "XXXX"
}
```

##### Response

```json
{}
```

### プロフィールを編集する

##### Endpoint

```
PATCH /api/v1/user/edit
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

### ユーザーの投稿の取得

##### Endpoint

```
GET /api/v1/user/posts
```

##### Request

- ログインユーザーの投稿の取得

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
- 最新から10件の投稿を取得する

```json
{}
```

- 指定したIDから10件の投稿を取得する(デフォルトは新しい方向)

```json
{
    "post_id": 11
}
```

- 指定したIDから時系列で新しい方向に10件の投稿を取得する

```json
{
    "post_id": 11,
    "type": "new"
}
```

- 指定したIDから時系列で古い方向に10件の投稿を取得する

```json
{
    "post_id": 11,
    "type": "old"
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
        "user": {
            "id": "XXXX",
            "screen_name": "XXXX",
            "avatar": "XXXX"
        },
        "liked": 1,
        "is_liked": true,
        "created_at": "XXXX",
        "updated_at": "XXXX"
    }
]
```