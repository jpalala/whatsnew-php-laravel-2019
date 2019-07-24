# Whats New in Laravel-2019


## Whats new in 5.8 (continuation)


1. Token guard token hashing

2. Cache TTL

3. Artisan serve improvements
    - Before 5.8.24: `php artisan serve --port=9006`
    - Via env or in the .env file
    ```php
       export SERVER_PORT="9006"
       php artisan serve
    ```
    - It will scan for next available port if it's already used.
    - New! [Symfony Dump Server](https://github.com/beyondcode/laravel-dump-server): Console log your server dumps inside terminal

4. Mock testing helper methods

This is another improvement to make your test code cleaner and readable. When we mock a transaction service and have it return some dummy transaction data, before,  we would write something like this:


```php

public function testBasicTest()
{       
  $service = Mockery::mock(TransactionService::class, function ($mock) {
        $mock->shouldReceive('find')->once()->with()->andReturn(['id' => 1, 'name' => 'foo']);
  });

  $this->instance(TransactionService::class, $service)
}
```

In Laravel 5.8 this can be shortened to:

```
public function testBasicTest()
{
  $this->mock(TransactionService::class, function($mock){
    $mock->shouldReceive('find')->once()->with(1)->andReturn(['id' => 1, 'name' => 'foo'])
  });
}

$users = AppUser::emailVerified()->orWhere->active()->get();
```

## Laravel News articles

### April 
- April 18: [Guzzler Testing Library](https://laravel-news.com/guzzler-testing-library)
- April 23: [Laraberg](https://laravel-news.com/laraberg-editor)
- April 24: [Job-based Retry delay](https://laravel-news.com/job-based-retry-delay)


### May 
- May 03: [Laravel mix alias](https://laravel-news.com/laravel-mix-alias)
- May 10: [Short Arrow functions coming to PHP](https://laravel-news.com/short-arrow-functions)
- May 15: [Laravel Tappable Trait](https://laravel-news.com/laravel-5-8-17-tappable-trait)

### June
- June 03: [Laravel sns events package](https://laravel-news.com/laravel-sns-events-package)
- June 05: [Array Collapse Performance Improvement in Laravel 5.8.20](https://laravel-news.com/laravel-5-8-20)
- June 10:  [LaraHead SEO Package](https://laravel-news.com/lara-head-seo-package)
- June 24: [Laravel Eloquent UUID](https://laravel-news.com/eloquent-uuid)



# Whats new in PHP


1. JSON_THROW_ON_ERROR
2. Argon2
3. Extra comma no longer throws error in function arguments.
4. PHP Void type
5. PHP Multi catch exception handling
6. PHP  Symmetric array destructuring: using `[]` instead of list()

Example:
 
```php
[$id1, $name1] = $data[0];
```

```php 
   foreach ($data as [$id, $name]) { 
     // logic here with $id and $name 
   }
```

- `array_key_first()` and `array_key_last()`
- [Iterable pseudotype](https://www.php.net/manual/en/class.traversable.php) 

Example:

```php

function foo(iterable $iterable) {
    foreach ($iterable as $value) {
        // ...
    } 
}

```
