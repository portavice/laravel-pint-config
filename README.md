# Laravel Pint Config

[![MIT Licensed](https://img.shields.io/badge/License-MIT-brightgreen.svg?style=flat-square)](LICENSE.md)
[![Latest version on Packagist](https://img.shields.io/packagist/v/portavice/laravel-pint-config.svg)](https://packagist.org/packages/portavice/laravel-pint-config)
[![Total downloads](https://img.shields.io/packagist/dt/portavice/laravel-pint-config.svg)](https://packagist.org/packages/portavice/laravel-pint-config)

This projects contains the default configuration for [Laravel Pint](https://laravel.com/docs/10.x/pint#configuring-pint)
used at portavice GmbH.

## Contents

- [Installation](#installation)
- [Usage](#usage)

## Installation

First, install the package via [Composer](https://getcomposer.org/):

```bash
composer require portavice/laravel-pint-config --dev
```

Note that this automatically installs Laravel Pint as well.

## Usage

To simplify usage, you may configure the following scripts in your `composer.json`:

```json
{
    "scripts": {
        "csPHP": "pint --config vendor/portavice/laravel-pint-config/pint.json --test",
        "csfixPHP": "pint --config vendor/portavice/laravel-pint-config/pint.json"
    }
}
```

Just run `composer csPHP` to check and `composer csfixPHP` to fix the PHP files in your Laravel project.
Otherwise, you will have to call the `pint` command with the `--config` option.

To use and adjust the set of rules defined by this package,
you can also copy the `pint.json` from this repository into your project.
