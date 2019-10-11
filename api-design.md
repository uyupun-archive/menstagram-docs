# API設計

### 一般ユーザー登録

##### Endpoint

```
POST /api/v1/user/register
```

### 一般ユーザーログイン

##### Endpoint

```
POST /api/v1/user/login
```

### 一般ユーザーログアウト

##### Endpoint

```
POST /api/v1/user/logout
```

### 管理ユーザー登録
// TODO

### 管理ユーザーログイン
// TODO

### 管理ユーザーログアウト
// TODO

### 特定のユーザの投稿を取得する

##### Endpoint

```
GET /api/v1/posts?user_id=XXXX
```

### プロフィールの取得

##### Endpoint

```
GET /api/v1/user/profile
```

### フォローの取得

##### Endpoint

```
GET /api/v1/user/following
```

### フォロワーの取得

##### Endpoint

```
GET /api/v1/user/followed
```

### フォローする

##### Endpoint

```
GET /api/v1/user/follow
```

### フォローをはずす

##### Endpoint

```
GET /api/v1/user/unfollow
```

### プロフィールを編集する

##### Endpoint

```
GET /api/v1/user/profile/edit
```

### いいね

##### Endpoint

```
GET /api/v1/posts/like
```

### プライベートタイムラインの取得

##### Endpoint

```
GET /api/v1/timeline/private
```

### グローバルタイムラインの取得

##### Endpoint

```
GET /api/v1/timeline/global
```

### 投稿詳細の取得

##### Endpoint

```
GET /api/v1/posts
```

### ラーメンじゃないよ報告

##### Endpoint

```
GET /api/v1/report/not-ramen
```

### 投稿

##### Endpoint

```
POST /api/v1/post
```

### いいね通知

##### Endpoint

```
GET /api/v1/notice/likes
```

### フォロー通知

##### Endpoint

```
GET /api/v1/notice/followed
```

### 運営からの通知

##### Endpoint

```
GET /api/v1/notice/systems
```