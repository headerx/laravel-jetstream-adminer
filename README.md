### Start

Clone
```bash
git clone git@github.com:headerx/laravel-jetstream-adminer.git
```
Configure Database credentials by copying env.example to .env and editing as appropriate.
```bash
php -r \"file_exists('.env') || copy('.env.example', '.env');\"
```
create an adminer database

```bash
mysql -u root -p "create database adminer"
```

run migrations and seed
```bash
php artisan migrate:fresh --seed
```

run server 
```bash
php artisan serve
```

login as `admin@admin.com` with password `secret`
