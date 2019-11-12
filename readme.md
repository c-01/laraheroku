<p align="center"><img src="https://res.cloudinary.com/dtfbvvkyp/image/upload/v1566331377/laravel-logolockup-cmyk-red.svg" width="200"></p>

## setup migrate first
```php

in App\Providers\AppServiceProvider

use Illuminate\Support\Facades\Schema;

public function boot()
{
    Schema::defaultStringLength(191);
}
```
## Create Factory Seeders
```php
$ php artisan make:factory UserFactory --model=User
$ php artisan make:seeder UsersTableSeeder

use App\User;
use Illuminate\Database\Seeder;

class UsersTableSeeder extends Seeder
{
    public function run()
    {
        factory(User::class, 100)->create();
    }
}

$ php artisan migrate --seed
```
## using Heroku
```
$ heroku login


```