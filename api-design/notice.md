# 通知系API

### いいね通知

##### Endpoint

```
GET /api/v1/notice/liked
```

##### Request

ヘッダに `Authorization: Bearer <access_token>` 形式でアクセストークンの指定が必須

- 最新10件のいいね通知を取得する

```json
{}
```

- 指定したIDから10件のいいね通知を取得する

```json
{
    "like_notice_id": 1
}
```

##### Response

```json
[
    {
        "id": 1,
        "src_user": {
            "user_id": "XXXX",
            "screen_name": "XXXX",
            "avater": "XXXX"
        },
        "post": {
            "id": 1,
            "image": "XXXX"
        },
        "like": {
            "created_at": "XXXX"
        }
    }
]
```

### フォロー通知

##### Endpoint

```
GET /api/v1/notice/followed
```

##### Request

ヘッダに `Authorization: Bearer <access_token>` 形式でアクセストークンの指定が必須

- 最新10件のフォロー通知を取得する

```json
{}
```

- 指定したIDから10件のフォロー通知を取得する

```json
{
    "follow_notice_id": 1
}
```

##### Response

```json
[
    {
        "id": 1,
        "src_user": {
            "user_id": "XXXX",
            "screen_name": "XXXX",
            "avater": "XXXX"
        },
        "follow": {
            "is_followed": false,
            "created_at": "XXXX"
        }
    }
]
```

### 運営からの通知

##### Endpoint

```
GET /api/v1/notice/system
```

##### Request

ヘッダに `Authorization: Bearer <access_token>` 形式でアクセストークンの指定が必須

- 最新10件の運営からの通知を取得する

```json
{}
```

- 指定したIDから10件の運営からの通知を取得する

```json
{
    "system_notice_id": 1
}
```

##### Response

```json
[
    {
        "id": 1,
        "text": "XXXX",
        "created_at": "XXXX"
    }
]
```