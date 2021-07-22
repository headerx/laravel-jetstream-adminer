### Start

Clone
```bash
git clone git@github.com:headerx/laravel-jetstream-adminer.git
```
Configure Database credentials by copying env.example to .env and editing as appropriate.
```bash
php -r "file_exists('.env') || copy('.env.example', '.env');"
```
create an adminer database

```bash
mysql -u root -p -e "create database adminer;"
```
install
```bash
composer install
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

Note
You may also want to edit the value of the HOME constant in `app/Providers/RouteServiceProvider.php` to match your details.
Query String (default) is for auto login (to adminer) with a database server running on localhost, and a user of root

```php
    /**
     * The path to the "home" route for your application.
     *
     * This is used by Laravel authentication to redirect users after login.
     *
     * @var string
     */
    public const HOME = '/iframes/adminer?server=127.0.0.1%3A3306&username=root&db=';
 ```
