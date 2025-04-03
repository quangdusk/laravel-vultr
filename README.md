# Create .env file for config docker
```
$ cp .env.example .env
```
# Docker
```
$ docker-compose up -d --build

```

# Composer install
```
$ docker-compose exec app composer install

```
# Copy .env of app
```
$cd src

$cp .env.example .env

```
# Config DB in .env 
```
DB_NAME=laravel-docker
DB_USER=user
DB_PASS=password
TZ=Asia/Tokyo
WEB_PORT=8868
APP_PORT=9989
DB_PORT=3022

```

# Migrate and seed data
```
$ docker-compose exec app ash

[/work/app]

$php artisan key:generate

$php artisan migrate

$php artisan db:seed

$chmod -R 777 storage/

$php artisan storage:link

```

# Link local

```
http://localhost:8868

```

# Config JWT to login in users app

```
$ docker-compose exec app ash

[/work/app]

$ composer update

$ php artisan jwt:secret

```
