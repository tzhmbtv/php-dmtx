# php-dmtx

> **Note**: This is a fork of the original [ptachoire/php-dmtx](https://github.com/ptachoire/php-dmtx) project with added support for newer PHP versions and PHPUnit 10.x compatibility.

Datamatrix reader/writer based on [libdmtx](https://github.com/dmtx).

⚠️ The installation of [dmtx-utils](https://github.com/dmtx/dmtx-utils) is required to use the lib.

## Install

```sh
composer require "tzhmbtv/php-dmtx:*"
```

## Usage

```php
use Dmtx\Writer;

$writer = new Writer();

//encode message into file
$writer->encode('this is a message')
    ->saveAs('/tmp/image.png');

//encode message and output image 
echo $writer->encode('this is a message')
    ->dump();
```

```php
use Dmtx\Reader;

$reader = new Reader();

//decode message from data
$reader->decode($encoded_value);

//decode message from file 
echo $reader->decodeFile('/tmp/image.png');
```

## Test

```sh
composer install
./vendor/bin/phpunit
```

## Compatibility

This fork is compatible with:
- PHP 8.2 or higher
- PHPUnit 10.x
- Symfony 3.4, 4.x, 5.x, 6.x, and 7.x packages

## Requirements

- PHP 8.2 or higher
- [dmtx-utils](https://github.com/dmtx/dmtx-utils) must be installed on your system

## Credits

Project structure inspired by
[Negotiation](https://github.com/willdurand/Negotiation) by
[willdurand](https://github.com/willdurand).

Original package created by [ptachoire](https://github.com/ptachoire).

Maintained by [elnur9924 @tzhmbtv](https://github.com/tzhmbtv).

## License

php-dmtx is released under the MIT License. See the bundled LICENSE file for
details.
