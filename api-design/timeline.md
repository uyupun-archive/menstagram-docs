# タイムライン系API

### グローバルタイムラインの取得

##### Endpoint

```
/api/v1/timeline/global
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
        "created_at": "XXXX",
        "updated_at": "XXXX"
    }
]
```

### プライベートタイムラインの取得

##### Endpoint

```
/api/v1/timeline/private
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
        "liked": 1,
        "created_at": "XXXX",
        "updated_at": "XXXX"
    }
]
```