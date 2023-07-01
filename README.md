# nestjsテンプレート

## 技術構成

```
Node 18.16.0
Nestjs 10.0.0
TypeScript 5.1.3
MySQL 8.0.33
Prisma 4.16.2
```


## 環境構築

### データベース作成

table_nameは、設定したいDBの名前を指定

```bash
$ mysql -u root -p
> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
> CREATE DATABASE table_name;
```

### env作成

```bash
$ touch .env
```

#### env記載

<img src="https://www.prisma.io/docs/static/a3179ecce1bf20faddeb7f8c02fb2251/42cbc/mysql-connection-string.png"/>

上記画像を参考に`DATABASE_URL`の値に設定

```.env
# Environment variables declared in this file are automatically made available to Prisma.
# See the documentation for more detail: https://pris.ly/d/prisma-schema#accessing-environment-variables-from-the-schema

# Prisma supports the native connection string format for PostgreSQL, MySQL, SQLite, SQL Server, MongoDB and CockroachDB.
# See the documentation for all the connection string options: https://pris.ly/d/connection-strings

例)
DATABASE_URL="mysql://root:password@127.0.0.1:3306/nest_template"
```

### インストール

```bash
$ npm install
```

### 起動

```bash
$ npm run start:dev
```
