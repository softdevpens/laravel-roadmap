# Cheat Laravel 
Berikut adalah cheat sheet untuk memudahkan pengodingan laravel dalam development aplikasi web
## Routes in Laravel

```php
Route::get('func', function(){});
Route::get('func', 'ControllerName@function');
Route::controller('func', 'argController');
```
### RESTful Controllers
```php
Route::resource('posts','PostsController');
```
#### Specify a subset of actions to handle on the route
```php
Route::resource('user', 'UserController',['only' => ['index', 'show']]);
Route::resource('project', 'ProjectController',['except' => ['update', 'destroy']]);
```

### Route Parameter
```php
Route::get('func/', function($arg){});
Route::get('func/', function($arg = 'arg'){});
```

### HTTP Method
```php
Route::any('func', function(){});
Route::post('func', function(){});
Route::put('func', function(){});
Route::patch('func', function(){});
Route::delete('func', function(){});
```

