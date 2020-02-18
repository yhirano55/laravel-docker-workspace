# laravel-docker-workspace

Development laravel app with docker-compose

refs. https://tech.windii.jp/backend/laravel/laravel-with-docker-compose

## Setup

```
$ cp my-laravel-app/.env.example my-laravel-app/.env
$ chmod -R a+w my-laravel-app/storage/*
$ docker-compose up -d --build

$ mysql -h 127.0.0.1 -uroot -p -P 3308
> CREATE DATABASE laravel;

$ docker-compose exec app bash
# --- in app container --
$ cd my-laravel-app
$ composer install
$ php artisan key:generate
$ php artisan migrate
```

And open 'http://localhost:8000'
