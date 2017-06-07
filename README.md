# Deep Art Effects SDK for PHP
Use this SDK to access the Deep Art Effects API with PHP.

## Requirements

PHP 5.4.0 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/deeparteffects/sdk-php.git"
    }
  ],
  "require": {
    "deeparteffects/sdk-php": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/sdk-php/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php

require_once(__DIR__ . '/vendor/autoload.php');

$api_key = '--Your API Key--';
$access_key = '--Your ACCESS Key--';
$secret_key = '--Your SECRET KEY--';

$api_instance = new \Deeparteffects\Client\Api\DefaultApi();
$api_instance->setApiKey($api_key);
$api_instance->setApiAccessKey($access_key);
$api_instance->setApiSecretKey($secret_key);

try {
    $styles = $api_instance->stylesGet();

    foreach ($styles as $style) {
        print_r($style->getTitle());
    }

} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->stylesGet: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *https://api.deeparteffects.com/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**resultGet**](docs/Api/DefaultApi.md#resultget) | **GET** /result | 
*DefaultApi* | [**stylesGet**](docs/Api/DefaultApi.md#stylesget) | **GET** /styles | 
*DefaultApi* | [**uploadPost**](docs/Api/DefaultApi.md#uploadpost) | **POST** /upload | 


## Documentation For Models

 - [Error](docs/Model/Error.md)
 - [ModelEmpty](docs/Model/ModelEmpty.md)
 - [Result](docs/Model/Result.md)
 - [Style](docs/Model/Style.md)
 - [Styles](docs/Model/Styles.md)
 - [UploadRequest](docs/Model/UploadRequest.md)
 - [UploadResponse](docs/Model/UploadResponse.md)


## Documentation For Authorization


## api_key

- **Type**: API key
- **API key parameter name**: x-api-key
- **Location**: HTTP header


## Author
Deep Art Effects GmbH



