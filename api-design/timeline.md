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
    }
]
```

### プライベートタイムラインの取得

##### Endpoint

```
/api/v1/timeline/private
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
    }
]
```