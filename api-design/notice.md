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

##### Response

```json
[
    {
        "id": 1,
        "src_user": {
            "id": 1,
            "avater": "XXXX"
        },
        "post": {
            "id": 1,
            "image": "XXXX"
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

##### Response

```json
[
    {
        "id": 1,
        "src_user": {
            "id": 1,
            "avater": "XXXX"
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

##### Response

```json
[
    {
        "id": 1,
        "text": "XXXX",
    }
]
```