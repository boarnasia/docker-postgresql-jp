# README

docker-compose settings for postgresql with ja_JP.utf-8

## Install

```shell
$ git clone git@github.com:boarnasia/docker-postgresql-jp.git .
$ cd docker-postgresql-jp
$ docker-compose up -d
```

## Unintall

```shell
$ cd docker-postgresql-jp
$ docker-compose down
$ docker volume rm postgresql_pgdata
$ cd ..
$ rm -fr ${docker-dir}
```

## Usage

Initial settings:

- usernamse: postgres
- password: password
- port: 5432

Connect to:

```shell
$ psql -h localhost -U postgres postgres
Password for user postgres: 
psql (10.5)
Type "help" for help.

postgres=# \l
                                  List of databases
   Name    |  Owner   | Encoding |   Collate   |    Ctype    |   Access privileges   
-----------+----------+----------+-------------+-------------+-----------------------
 postgres  | postgres | UTF8     | ja_JP.UTF-8 | ja_JP.UTF-8 | 
 template0 | postgres | UTF8     | ja_JP.UTF-8 | ja_JP.UTF-8 | =c/postgres          +
           |          |          |             |             | postgres=CTc/postgres
 template1 | postgres | UTF8     | ja_JP.UTF-8 | ja_JP.UTF-8 | =c/postgres          +
           |          |          |             |             | postgres=CTc/postgres
(4 rows)

postgres=#
```

Boot:

```shell
$ cd docker-postgresql-jp
$ docker-compose up -d
```

Showtdown:

```shell
$ cd docker-postgresql-jp
$ docker-compose down
```
