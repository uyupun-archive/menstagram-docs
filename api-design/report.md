# 報告系API

### ラーメンじゃないよ報告

##### Endpoint

```
POST /api/v1/report/not-ramen
```

##### Request

ヘッダに `Authorization: Bearer <access_token>` 形式でアクセストークンの指定が必須

```json
{
    "post_id": "XXXX"
}
```

##### Response

```json
{}
```