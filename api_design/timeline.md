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
            "user_id": "XXXX",
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

### プライベートタイムラインの取得

##### Endpoint

```
GET /api/v1/timeline/private
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
            "user_id": "XXXX",
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
