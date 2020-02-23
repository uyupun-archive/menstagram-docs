# ユーザー系API

### ユーザーのプロフィールの取得

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
    "user_name": "XXXX",
    "user_id": "XXXX",
    "slurp_count": 1,
    "follow_count": 1,
    "follower_count": 1,
    "is_follow": false,
    "is_me": false,
    "biography": "XXXX"
}
```

### ユーザーのスラープの取得

##### Endpoint

```
GET /api/v1/user/slurps
```

##### Request
- 最新から100件のスラープを取得する

```json
{}
```

- 指定したユーザーIDのスラープを取得する

```json
{
    "user_id": "XXXX"
}
```

- 指定したIDから100件のスラープを取得する(デフォルトは新しい方向)

```json
{
    "slurp_id": 101
}
```

- 指定したIDから時系列で新しい方向に100件のスラープを取得する

```json
{
    "slurp_id": 101,
    "type": "new"
}
```

- 指定したIDから時系列で古い方向に100件のスラープを取得する

```json
{
    "slurp_id": 101,
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
            "user_id": "XXXX",
            "user_name": "XXXX",
            "avatar": "XXXX"
        },
        "yum_count": 1,
        "is_yum": true,
        "created_at": "XXXX",
        "updated_at": "XXXX"
    }
]
```

### ログインユーザーのプロフィールを編集する

##### Endpoint

```
PATCH /api/v1/user/edit
```

##### Request
`biography`は空文字でのリクエストが可能.

```json
{
    "user_name": "XXXX",
    "biography": "XXXX"
}
```

##### Response

```json
{}
```

### ログインユーザーのアバターを編集する

##### Endpoint

```
PUT /api/v1/user/edit/avatar
```

##### Request
`Content-Type` には `multipart/form-data` を指定する.

```json
{
    "avatar": <image-data>
}
```

##### Response

```
{}
```

### ログインユーザーがヤムしたスラープの取得

##### Endpoint

```
GET /api/v1/user/yums
```

##### Request
- 最新から10件のスラープを取得する

```json
{}
```

- 指定したIDから10件のスラープを取得する(デフォルトは新しい方向)

```json
{
    "slurp_id": 11
}
```

- 指定したIDから時系列で新しい方向に10件のスラープを取得する

```json
{
    "slurp_id": 11,
    "type": "new"
}
```

- 指定したIDから時系列で古い方向に10件のスラープを取得する

```json
{
    "slurp_id": 11,
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
            "user_id": "XXXX",
            "user_name": "XXXX",
            "avatar": "XXXX"
        },
        "yum_count": 1,
        "is_yum": true,
        "created_at": "XXXX",
        "updated_at": "XXXX"
    }
]
```

### フォロー

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

### アンフォロー

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

### ユーザーのフォロイーの取得

##### Endpoint

```
GET /api/v1/user/followee
```

##### Request

- ログインユーザーのフォロイー一覧の取得

```json
{}
```

- 指定したユーザーのフォロイー一覧の取得

```json
{
    "user_id": "XXXX"
}
```

- 指定したIDから10件のスラープを取得する(デフォルトは新しい方向)

```json
{
    "follow_id": 101
}
```

- 指定したIDから時系列で新しい方向に10件のスラープを取得する

```json
{
    "follow_id": 101,
    "type": "new"
}
```

- 指定したIDから時系列で古い方向に10件のスラープを取得する

```json
{
    "follow_id": 101,
    "type": "old"
}
```

##### Response

```json
[
    {
        "user_id": "XXXX",
        "user_name": "XXXX",
        "avater": "XXXX",
        "is_follow": false,
        "is_me": false
    }
]
```

### ユーザーのフォロワーの取得

##### Endpoint

```
GET /api/v1/user/follower
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

- 指定したIDから10件のスラープを取得する(デフォルトは新しい方向)

```json
{
    "follow_id": 101
}
```

- 指定したIDから時系列で新しい方向に10件のスラープを取得する

```json
{
    "follow_id": 101,
    "type": "new"
}
```

- 指定したIDから時系列で古い方向に10件のスラープを取得する

```json
{
    "follow_id": 101,
    "type": "old"
}
```

##### Response

```json
[
    {
        "user_id": "XXXX",
        "user_name": "XXXX",
        "avater": "XXXX",
        "is_follow": false,
        "is_me": false
    }
]
```