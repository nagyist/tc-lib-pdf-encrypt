# tc-lib-pdf-encrypt

*Please consider supporting this project by making a donation to <paypal@tecnick.com>*

* **category**    Library
* **package**     \Com\Tecnick\Pdf\Encrypt
* **author**      Nicola Asuni <info@tecnick.com>
* **copyright**   2011-2015 Nicola Asuni - Tecnick.com LTD
* **license**     http://www.gnu.org/copyleft/lesser.html GNU-LGPL v3 (see LICENSE.TXT)
* **link**        https://github.com/tecnickcom/tc-lib-pdf-encrypt

## Status
* **MASTER**: [![Build Status](https://secure.travis-ci.org/tecnickcom/tc-lib-pdf-encrypt.png?branch=master)](https://travis-ci.org/tecnickcom/tc-lib-pdf-encrypt?branch=master)
[![Coverage Status](https://coveralls.io/repos/tecnickcom/tc-lib-pdf-encrypt/badge.svg?branch=master&service=github)](https://coveralls.io/github/tecnickcom/tc-lib-pdf-encrypt?branch=master)
* **DEVELOP**: [![Build Status](https://secure.travis-ci.org/tecnickcom/tc-lib-pdf-encrypt.png?branch=develop)](https://travis-ci.org/tecnickcom/tc-lib-pdf-encrypt?branch=develop)
[![Coverage Status](https://coveralls.io/repos/tecnickcom/tc-lib-pdf-encrypt/badge.svg?branch=develop&service=github)](https://coveralls.io/github/tecnickcom/tc-lib-pdf-encrypt?branch=develop)


## Description

PHP library to encrypt data for PDF.

The initial source code has been extracted from TCPDF (<http://www.tcpdf.org>).


## Getting started

This library requires openssl and mcrypt php extensions to be able to test all functionalities.
On production either openssl or mcrypt are required.

First, you need to install all development dependencies using [Composer](https://getcomposer.org/):

```bash
$ curl -sS https://getcomposer.org/installer | php
$ mv composer.phar /usr/local/bin/composer
```

This project include a Makefile that allows you to test and build the project with simple commands.
To see all available options:

```bash
make help
```

To install all the development dependencies:

```bash
make build_dev
```

## Running all tests

Before committing the code, please check if it passes all tests using

```bash
make qa_all
```
this generates the phpunit coverage report in target/coverage.
Please check if the tests are covering all code.

Generate the documentation:

```bash
make docs
```

Generate static analysis reports in target/report:

```bash
make reports
```

Other make options allows you to install this library globally and build an RPM package.
Please check all the available options using `make help`.


## Example

Examples are located in the `example` directory.

Start a development server (requires PHP 5.5) using the command:

```
make server
```

and point your browser to <http://localhost:8000/index.php>


## Installation

Create a composer.json in your projects root-directory:

```json
{
    "require": {
        "tecnickcom/tc-lib-pdf-encrypt": "dev-master"
    },
    "repositories": [
        {
            "type": "vcs",
            "url": "git@github.com:tecnickcom/tc-lib-pdf-encrypt.git"
        }
    ]
}
```


## Packaging

This library is mainly intended to be used and included in other PHP projects using Composer.
However, since some production environments dictates the installation of any application as RPM or DEB packages,
this library includes make targets for building these packages (`make rpm` and `make deb`).
The packages are generated under the `target` directory.

When this library is installed using an RPM or DEB package, you can use it your code by including the autoloader:
```
require_once ('/usr/share/php/Com/Tecnick/Pdf/Encrypt/autoload.php');
```


## Developer(s) Contact

* Nicola Asuni <info@tecnick.com>