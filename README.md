# web-service-gin

ginとmysqlを使った簡単なwebアプリケーションです。

## mysql

ホストでport 3306で起動してください。

## 環境変数

mysqlを使用するために以下の環境変数を設定してください

- DBUSER
- DBPASS

## database

- myappでdatabaseを作成してください。

- sqlディレクトリ以下にテーブル作成とseedデータ作成のsqlファイルを作成しているので実行してください

## docker

docker化はしていないため、dockerを使用する場合は適宜コードを書き換えてください。

## 環境構築方法

### .env を作成

```
DB_USER=
DB_PASSWORD=
DB_HOST=
DB_PORT=
DB_NAME=
```

### 起動する

`docker compose up -d`で airを起動する
初回は sql/init.sql でテーブル作成とデータ投入される

### curlコマンドでHTTPリクエストを送る

`curl http://localhost:8080/albums`

**出力結果**

| id | title | artist | price |
|---|---|---|---|
| 1 | Blue Train | John Coltrane | 56.99 |
| 2 | Giant Steps | John Coltrane | 63.99 |
| 3 | Jeru | Gerry Mulligan | 17.99 |

### 停止する

`docker compose down -v` でボリュームの削除と停止をする