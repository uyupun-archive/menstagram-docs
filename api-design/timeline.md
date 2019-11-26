# タイムライン系API

### グローバルタイムラインの取得

##### Endpoint

```
/api/v1/timeline/global
```

##### Request
- 最新から32件の投稿を取得する

```json
{}
```

- 指定したIDから32件の投稿を取得する(デフォルトは新しい方向)

```json
{
    "post_id": 33
}
```

- 指定したIDから時系列で新しい方向に32件の投稿を取得する

```json
{
    "post_id": 33,
    "type": "new"
}
```

- 指定したIDから時系列で古い方向に32件の投稿を取得する

```json
{
    "post_id": 33,
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

- 最新から32件の投稿を取得する

```json
{}
```

- 指定したIDから32件の投稿を取得する(デフォルトは新しい方向)

```json
{
    "post_id": 33
}
```

- 指定したIDから時系列で新しい方向に32件の投稿を取得する

```json
{
    "post_id": 33,
    "type": "new"
}
```

- 指定したIDから時系列で古い方向に32件の投稿を取得する

```json
{
    "post_id": 33,
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
        "created_at": "XXXX",
        "updated_at": "XXXX"
    }
]
```
