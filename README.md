phpSmug 4.0 - PHP Wrapper for the SmugMug API
=============================================

# :construction: Work In Progress :construction: #

phpSmug 4.0 will be the first release to support the new SmugMug API 2.0. Consider this branch broken and not working until this text has been removed.

# phpSmug 4.0

A simple Object Orientated wrapper for the SmugMug API, written with PHP5.

Uses [SmugMug API v2](https://api.smugmug.com/api/v2/doc/index.html). The object API is very similar to the RESTful API.

## Features

* Follows PSR-0 conventions and coding standard: autoload friendly
* Light and fast thanks to lazy loading of API classes
* Extensively tested and documented

## Requirements

* PHP >= 5.3.2 with [cURL](http://php.net/manual/en/book.curl.php) extension,
* [Guzzle](https://github.com/guzzle/guzzle) library,
* (optional) PHPUnit to run tests.

## Autoload

The new version of `phpSmug` using [Composer](http://getcomposer.org).
The first step to use `phpSmug` is to download composer:

```bash
$ curl -s http://getcomposer.org/installer | php
```

Then we have to install our dependencies using:
```bash
$ php composer.phar install
```
Now we can use autoloader from Composer by:

```json
{
    "require": {
        "lildude/phpSmug": "~4.0"
    }
}
```

> `phpSmug` follows the PSR-0 convention names for its classes, which means you can easily integrate `phpSmug` classes loading in your own autoloader.

## Basic usage of `phpSmug` client

```php
<?php

// This file is generated by Composer
require_once 'vendor/autoload.php';

$client = new phpSmug\Client(array("APIKey" => "[YOUR_API_KEY]", "AppName" => "Your CoolApp/1.0 (http://yourapp.com)"));
$repositories = $client->get('user/[your_username]!albums');
?>
```

From the `$client` object, you can access to all SmugMug.

## Documentation

See the [`doc` directory](doc/) for more detailed documentation.

## License

`phpSmug` is licensed under the MIT License - see the LICENSE file for details
