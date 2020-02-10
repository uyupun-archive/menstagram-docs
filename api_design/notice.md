# 通知系API

### ヤム通知

##### Endpoint

```
GET /api/v1/notice/yummed
```

##### Request

- 最新10件のヤム通知を取得する

```json
{}
```

- 指定したIDから10件のヤム通知を取得する

```json
{
    "yum_notice_id": 1
}
```

##### Response

```json
[
    {
        "id": 1,
        "src_user": {
            "user_id": "XXXX",
            "user_name": "XXXX",
            "avater": "XXXX"
        },
        "slurp": {
            "id": 1,
            "image": "XXXX"
        },
        "yum": {
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
            "user_name": "XXXX",
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