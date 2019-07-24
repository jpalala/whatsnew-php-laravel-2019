

JSON_THROW_ON_ERROR
json_decode(�{�); -> will error

json_last_error() === JSON_ERROR_NONE

json_last_error_msg()

try {
return json_decode(�{�, JSON_THROW_ON_ERROR);
} catch (JsonException $error) {
$e->getMessage();
}

Wordpress use:

## WP JSON API

## Argon2 password hashing
Argon2 is a hashing algorithm that was introduced in PHP 7.2 as an alternative to the Bcrypt algorithm. The PASSWORD_ARGON2I constant can be used as follows in password_* functions:

password_hash('password', PASSWORD_ARGON2I);



Starting 7.3, Function calll with extra comma - no issue anymore.

getNumberOfClients( $company, $year, )

# removed Case-Insensitive Constants

---
## Nullable types
Type declarations for parameters and return values can now be marked as nullable
prefix with question mark.

# Void type
A void return type has been introduced.

# Multi catch exception handling �

now be specified using the pipe character (|)

# Symmetric array destructuring �
may now be used to destructure arrays for assign.


// [] style
[$id1, $name1] = $data[0];



// [] style
foreach ($data as [$id, $name]) {
    // logic here with $id and $name
}
