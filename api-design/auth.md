# 認証系API

### 一般ユーザー登録

##### Endpoint

```
POST /api/v1/auth/register
```

##### Request

```json
{
    "user_id": "XXXXX",
    "screen_name": "XXXXX",
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
POST /api/v1/auth/login
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

```
POST /api/v1/auth/logout
```

##### Request

```json
{}
```

##### Response

```json
{}
```

### 管理ユーザー登録
// TODO

### 管理ユーザーログイン
// TODO

### 管理ユーザーログアウト
// TODO