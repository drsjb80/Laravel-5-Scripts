# Laravel-5-Scripts
Some basic scripts for the creation of Laravel 5 applications and
scaffolds. Requires laravel and git be in $PATH.

You should be able to run create\_app and then cd to the newly-created
directory and run create\_scaffold as many times as needed.

```bash
beatys@ms16142->Laravel-5-Scripts$ ./create_app 
/Users/beatys/.composer/vendor/bin/laravel
/usr/local/bin/git
---- Please enter the name of the application you want to create: todo
Crafting application...
Loading composer repositories with package information
Installing dependencies (including require-dev) from lock file
  - Installing jakub-onderka/php-console-color ([33m0.1[39m)
    Loading from cache

  - Installing vlucas/phpdotenv ([33mv2.3.0[39m)
    Loading from cache

[...]

Generating autoload files
> php -r "copy('.env.example', '.env');"
> Illuminate\Foundation\ComposerScripts::postInstall
> php artisan optimize
Generating optimized class loader
> php artisan key:generate
Application key [base64:tnaH/m0w9oikhCq6Vw2WTY0k0e8fdxic1yd01GXD+tk=] set successfully.
Application ready! Build something amazing.
Installing composer
All settings correct for using Composer
Downloading 1.1.3...
Composer successfully installed to: /Users/beatys/Documents/DU/4561/scripts/Laravel-5-Scripts/todo/composer.phar
Use it: php composer.phar
Installing l5scaffold
./composer.json has been updated
Loading composer repositories with package information
Updating dependencies (including require-dev)
  - Installing laralib/l5scaffold (dev-master 623ae62)
    Cloning 623ae6207c42371a60ffce3daceb728217d93c9e

Writing lock file
Generating autoload files
> Illuminate\Foundation\ComposerScripts::postUpdate
> php artisan optimize
Generating optimized class loader
Patching config/app
Patching .env
Creating empty database

beatys@ms16142->Laravel-5-Scripts$ cd todo/

beatys@ms16142->todo$ ../create_scaffold 
---- Please enter the name of the scaffold you want to create: todo
---- Please enter the name of a field: todo
---- Please enter the type of field todo: string
---- Would you like to enter another field? y/n: n
Running php artisan make:scaffold --schema=todo:string todo
Configuring Todo...
Migration created successfully
Seed created successfully.
Model created successfully.
Controller created successfully.
Layout created successfully.
Error created successfully.
Views created successfully.
Dump-autoload...
Route::resource("todos","TodoController"); // Add this line in routes.php
Patching app/Http/routes.php
Migrating database
Migration table created successfully.
Migrated: 2014_10_12_000000_create_users_table
Migrated: 2014_10_12_100000_create_password_resets_table
Migrated: 2016_07_12_124227_create_todos_table
Created a model in app/Todo.php
Created a controller in app/Http/Controllers/TodoController.php
Created views in resources/views/todos
Created resource in app/Http/routes.php, see 'artisan route:list' for details.

beatys@ms16142->todo$ php Kartisan serve
Laravel development server started on http://localhost:8000/
```
