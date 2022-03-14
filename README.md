# Clients-Transactions REST API.

A small JSON API which allows consumers to deposit, list, and search transfer history.

## Contents.

- [Getting Started.](#getting-started)
  - [Prerequisites.](#prerequisites)
  - [Installing.](#installing)
  - [How to consume this API.](#how-to-consume-api)
- [Running Tests.](#testing)
- [Built With.](#built-with)
- [Helpful Guides.](#helpful-guides)
- [Authors.](#authors)

## <a id="getting-started"></a> Getting Started.
The easiest way is to run the project inside a Docker Container, but you can still manually configure and run the project with ```composer``` and ```php``` without Docker. Note that if you run the project **without using Docker**, you will need to manually setup a Database.

### <a id="prerequisites"></a> Prerequisites.
- [PHP >= 7.3.](https://www.php.net/downloads) - Scripting Language.
- [Composer](https://getcomposer.org/) - PHP Dependency Manager.
- [Laravel](https://laravel.com/) - PHP Web Framework.
- Database [MySQL](https://www.mysql.com/)...).

### <a id="installing"></a> Installing.

Install dependencies:
```
composer install
```
Create ```.env``` file (Windows):
```
copy .env.example .env
```
Create ```.env``` file (Linux):
```
cp .env.example .env
```
Generate Laravel's APP_KEY:
```
php artisan key:generate
```
Configure the Database in ```.env```. For example for MySQL running on ```localhost:8000```:
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=5432
DB_DATABASE=restful-api
DB_USERNAME=user
DB_PASSWORD=secret
```
Run the server:
```
php artisan serve
```
You can start making requests to ```http://localhost:8000```.

## <a id="how-to-consume-api"></a> How to consume this API.

### Clients:
  - ```(GET)``` - Get Clients -> /api/clients
  - ```(GET)``` - Get Client -> /api/clients/{id}
  - ```(POST)``` - Create Client -> /api/clients
  - ```(PUT)``` - Modify Client -> /api/clients/{id}
  - ```(DELETE)``` - Delete Client -> /api/clients/{id}

#### JSON Format to Create/Update Client.
```json
{
  "name": "somename",
  "lastname": "somelastname",
  "phone_number": "+2349021345678"
}
```

### Transactions:
  - ```(GET)``` - Get Transactions -> /api/transactions
  - ```(GET)``` - Get Transaction -> /api/transactions/{id}
  - ```(POST)``` - Create Transaction -> /api/transactions
  - ```(PUT)``` - Modify Transaction -> /api/transactions/{id}
  - ```(DELETE)``` - Delete Transaction -> /api/transactions/{id}
  
#### JSON Format to Create Transaction.
```json
{
  "client_id": "id",
  "deposit_amount": "amount",
  "deposit_date": "yyyy-mm-dd"
}
```

## <a id="testing"></a> Running Tests.
Simply run:
```bash
composer run-script test
```
or:
```bash
composer test
```

## <a id="built-with"></a> Built With.
- [Composer](https://getcomposer.org/) - Dependency Manager.
- [Laravel](https://laravel.com/) - Web Framework.

## <a id="helpful-guides"></a> Helpful Guides.
  - [The Smart Way to Handle Request Validation in Laravel - Medium.](https://medium.com/@kamerk22/the-smart-way-to-handle-request-validation-in-laravel-5e8886279271)
  - [Disable Validation Redirect in Laravel.](https://paulund.co.uk/disable-validation-redirect-in-laravel)
  - [Tests Laravel Applications - Blog Pusher.](https://blog.pusher.com/tests-laravel-applications/)  
  - [Testing - Laravel's Official Documentation.](https://laravel.com/docs/5.7/testing)
  - [HTTP Tests- Laravel's Official Documentation.](https://laravel.com/docs/5.7/http-tests)  
  - [Database Testing - Laravel's Official Documentation.](https://laravel.com/docs/5.7/database-testing)  
  - [How to Run PHPUnit Tests in Laravel.](https://stackoverflow.com/questions/47009667/how-to-run-phpunit-in-laravel-5-5)  
  - [Migrating from Laravel 5.7 to 5.8.](https://laravel.com/docs/5.8/upgrade#upgrade-5.8.0)  
  - [Composer - Scripts.](https://getcomposer.org/doc/articles/scripts.md)
  - [A template to make good README.md.](https://gist.github.com/PurpleBooth/109311bb0361f32d87a2)

## <a id="authors"></a> Authors.
- Oluchukwu Udu.
