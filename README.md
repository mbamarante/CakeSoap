# CakeSoap

## Requirements
* CakePHP 4.x

## Installation

You can install this plugin into your CakePHP application using [composer](http://getcomposer.org).

The recommended way to install composer packages is:

```
composer require mbamarante/cakesoap
```

You can also add `"mbamarante/cakesoap" : "dev-master"` to `require` section in your application's `composer.json`. Use for latest updates.

-- or --

You can also add `"mbamarante/cakesoap" : "~3.2"` to `require` section in your application's `composer.json`. Stable Release.

## Usage

Include the CakeSoap library files:
```php
    use CakeSoap\Network\CakeSoap;
```

### Sample Request

```php
    $soap = new CakeSoap([
        'wsdl' => 'http://mydomain.com/api?wsdl',
        'userAgent' => 'MySoapClientAgent'
    ]);

    $response = $soap->sendRequest($action, [
        'SomeData' => [
            'SomeSubData' => 'item1',
            'SomeMoreSubData' => 'item2'
        ]
    ]);
```

