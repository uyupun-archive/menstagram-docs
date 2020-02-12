# タイムライン系API

### グローバルタイムラインの取得

##### Endpoint

```
GET /api/v1/timeline/global
```

##### Request
- 最新から10件の投稿を取得する

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

### プライベートタイムラインの取得

##### Endpoint

```
GET /api/v1/timeline/private
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
