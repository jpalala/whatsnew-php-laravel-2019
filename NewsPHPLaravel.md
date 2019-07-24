Front-end development: HTML, CSS, Javascript

PHP - General programming skills from javascript (vars, arrays, loops, functions, etc.) and other languages will apply, but the syntax of php requires some acclimation.

7.3

JSON_THROW_ON_ERROR
json_decode(“{“); -> will error

json_last_error() === JSON_ERROR_NONE

json_last_error_msg()

try {
return json_decode(“{“, JSON_THROW_ON_ERROR);
} catch (JsonException $error) {
$e->getMessage();
}

Wordpress use:

WP JSON API

Argon2 password hashing
Argon2 is a hashing algorithm that was introduced in PHP 7.2 as an alternative to the Bcrypt algorithm. The PASSWORD_ARGON2I constant can be used as follows in password_* functions:

password_hash('password', PASSWORD_ARGON2I);



Function calll with extra comma - no issue anymore. 
getNumberOfClients( $company, $year, )

removed Case-Insensitive Constants

---
Nullable types
Type declarations for parameters and return values can now be marked as nullable
prefix with question mark.

# Void type
A void return type has been introduced.

# Multi catch exception handling ¶

now be specified using the pipe character (|)

# Symmetric array destructuring ¶
may now be used to destructure arrays for assign. 


// [] style
[$id1, $name1] = $data[0];



// [] style
foreach ($data as [$id, $name]) {
    // logic here with $id and $name
}


php http2 support



https://www.php.net/manual/en/class.traversable.php -> Foreach 'iterable' Pseudo type (similar to callable)


7.2: 
https://medium.com/@secmuhammed/php-7-2-new-features-fb7b8f88adb5  - new features 7.2

7.3:

array_key_first(), array_key_last()

https://laravel-news.com/spread-operator-in-array-expressions-coming-to-php-7-4

Laravel: 

April 24 - https://laravel-news.com/job-based-retry-delay
code4mk/lara-head - https://laravel-news.com/lara-head-seo-package june 10
june 3 https://laravel-news.com/laravel-sns-events-package
may 3 https://laravel-news.com/laravel-mix-alias
may 10 - https://laravel-news.com/short-arrow-functions
may 15 - https://laravel-news.com/laravel-5-8-17-tappable-trait







