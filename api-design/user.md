# ユーザー系API

### プロフィールの取得

##### Endpoint

```
GET /api/v1/user/profile/XXXX
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

### フォローの取得

##### Endpoint

```
GET /api/v1/user/following/XXXX
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

### フォロワーの取得

##### Endpoint

```
GET /api/v1/user/followed/XXXX
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
POST /api/v1/user/profile/edit
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