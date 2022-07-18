# 開発環境 Docker について

## 準備

docker と docker-compose が必要です。  
[Docker Desktop](https://docs.docker.jp/get-docker.html)を導入すれば両方インストールできます。  

## 初回起動

```sh
> cd THIS_REPOSITORY_DIR
> rm laravel/.env
> docker-compose up -d --build
> docker exec -it tttest-laravel /mnt/.docker/laravel/firstexec.sh
```

- `laravel/.env.docker` が更新された場合、反映のために一度 `laravel/.env` ファイルを削除する必要があります。それ以外の場合に `laravel/.env` を削除する必要はありません。  
- 現在、 `laravel/firstexec.sh` を実行するとDBのデータが初期化されます。データを削除したくない場合は、引数 `--nodb` をつけて実行してください。  

```sh
> docker exec -it tttest-laravel /mnt/.docker/laravel/firstexec.sh --nodb
```

## 2回目以後の起動と終了

コンテナ起動

```sh
> docker-compose up -d
```

コンテナ停止

```sh
> docker-compose stop
```

コンテナ削除

```sh
> docker-compose down
```

## アクセス

コンテナ起動後に、以下のURLでアクセスできます  

- Web [http://localhost:8000/](http://localhost:8000/)
- phpMyAdmin [http://localhost:8880/](http://localhost:8880/)  
- MailHog [http://localhost:8025/](http://localhost:8025/)  

コンテナ内のシェルに移動する  

```sh
> cd THIS_REPOSITORY_DIR
> docker-compose up -d
> docker exec -it tttest-laravel bash
$ pwd
/var/www/laravel
$ php artisan list
$ exit
```

- リポジトリルートが `/mnt` にmountされています。
- laravel フォルダが `/var/www/laravel` になっています。
- シェルの初期位置が `/var/www/laravel` になっています。

## UnitTestの実行

```sh
> cd THIS_REPOSITORY_DIR
> docker-compose up -d
> docker exec -it tttest-laravel php artisan test
```

もしくは

```sh
> cd THIS_REPOSITORY_DIR
> docker-compose up -d
> docker exec -it tttest-laravel bash
$ php artisan test
```
