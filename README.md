# Laravel Pint Config

[![MIT Licensed](https://img.shields.io/badge/License-MIT-brightgreen.svg?style=flat-square)](LICENSE.md)
[![Latest version on Packagist](https://img.shields.io/packagist/v/portavice/laravel-pint-config.svg)](https://packagist.org/packages/portavice/laravel-pint-config)
[![Total downloads](https://img.shields.io/packagist/dt/portavice/laravel-pint-config.svg)](https://packagist.org/packages/portavice/laravel-pint-config)

This project contains the default configuration for [Laravel Pint](https://laravel.com/docs/12.x/pint#configuring-pint)
used at portavice GmbH.

The ruleset is based on [PSR12](https://cs.symfony.com/doc/ruleSets/PSR12.html) with additional rules for

- ordered class elements, imports, used interfaces and traits, parameter types,
- short syntax, proper indentation, trailing commas for arrays,
- consistent braces, operators, spacing, blank lines, 
- preferring single quotes,
- and avoiding useless code (`else`, `return`, `sprintf`, empty statements).

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
