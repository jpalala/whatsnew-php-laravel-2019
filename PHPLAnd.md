https://medium.com/@advanceidea/whats-new-in-php-7-3-php-7-3-features-upcoming-f581e7c741f0



Repository Pattern

The idea with this pattern is to have a generic abstract way for the app to work with the data layer without being bothered what storage technology is used when saving/retrieving the data.

https://www.laravelbestpractices.com/#php_paas_providers

6. Use Of Autoload
In Laravel, any class or even plain PHP code can be used, as long as it could be auto-loaded. This improves the performance of the scripts by preventing PHP from checking if the file is already been loaded or not. PHP will let you know if it is needed when it is needed.

7. Using Migrations
Making generous use of migrations is yet another important point that when considered will help the programmers in creating web solutions. Database migrations can be put to use for constructing a table, adding and altering the fields

8. Validation
Move validation from controllers to Request classes.

Not To Use:

```
public function store(Request $request)
{
$request->validate([
  'title' => 'required|unique:articles|max:255',

  'body' => 'required',

'publish_at' => 'nullable|date',

]);

}
```

Should Use:
```
public function store(ArticleRequest $request)

{

}
```
-----------------------------------------------------------------------------------

<h2>Spatie</h2>.

<h2>Entrust</h2>.
spa
<h2>Laravel Debugbar</h2>.

<h2>Laravel User Verification</h2>
https://github.com/jrean/laravel-user-verification

Socialite.

Laravel Mix.
Eloquent-Sluggable.
Migration Generator.


Sociatleite
Passport
https://medium.com/@martin.riedweg/laravel-5-7-api-authentification-with-laravel-passport-92b909e12528






class ArticleRequest extends Request

{

public function rules()

{

return [

'title' => 'required|unique:articles|max:255',

'body' => 'required',

'publish_at' => 'nullable|date',

];

}

}





http://id.phptherightway.com/pages/Functional-Programming.html


Cloudways

Application Namespace
It is recommended to give your application a name. That is, instead of using the default App root namespace given by Laravel install, set it to what the application is all about. This can be set via
php artisan app:name YourAppName

https://medium.com/@adedotunolawale/using-modular-approach-with-laravel-building-module-based-application-part-1-b5c5a4e9ed38

#Symfony

## Scalability
WIP (work in progress): this will be filled up by collected best practices once we had done enough research about the subject matter.

## Scaling Up
- Load balancing,
- Allow storage session into Reids key value StorageEvent.

## Scaling Out
- Using serverless


Microservices
WIP (work in progress): this will be filled up by collected best practices once we had done enough research about the subject matter.

