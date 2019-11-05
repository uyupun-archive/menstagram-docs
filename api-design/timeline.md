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
- 指定したIDの一つ前から32件の投稿を取得する

```json
{
    "post_id": 33
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
- 指定したIDの一つ前から32件の投稿を取得する

```json
{
    "post_id": 33
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
        "created_at": "XXXX",
        "updated_at": "XXXX"
    }
]
```