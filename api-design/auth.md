# 認証系API

### 一般ユーザー登録

##### Endpoint

```
POST /api/v1/user/register
```

##### Request

```json
{
    "screen_name": "XXXXX",
    "user_id": "XXXXX",
    "email": "XXXXX",
    "password": "XXXXX"
}
```

##### Response

```json
{
    "access_token": "XXXXX"
}
```

### 一般ユーザーログイン

##### Endpoint

```
POST /api/v1/user/login
```

##### Request

```json
{
    "user_id": "XXXXX",
    "password": "XXXXX"
}
```

##### Response

```json
{
    "access_token": "XXXXX"
}
```

### 一般ユーザーログアウト

##### Endpoint

ヘッダに `Authorization: Bearer <access_token>` 形式でアクセストークンの指定が必須

```
POST /api/v1/user/logout
```

##### Request

```json
{
    "user_id": "XXXXX",
    "password": "XXXXX"
}
```

### 管理ユーザー登録
// TODO

### 管理ユーザーログイン
// TODO

### 管理ユーザーログアウト
// TODO