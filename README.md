## 環境
- Ruby version
  - 3.1.2
- MySQL
  - 8.0.16
- System dependencies
  [Docker](https://docs.docker.com/docker-for-mac/install/)を使って開発環境を立ち上げる

- Configuration

### Ports

| service  | port |
| -------- | ---- |
| api      | 3000 |
| mysql    | 3306 |

#### 環境変数

データベースの接続情報などは環境変数を利用しています。

[direnv](https://github.com/direnv/direnv)を利用する場合は `/.envrc.sample` を参考に `/.envrc` で指定してください。

### 立ち上げ

```
docker-compose up --build -d
```

### データベースのセットアップ

```
docker-compose exec api bin/rails db:create db:migrate
```
