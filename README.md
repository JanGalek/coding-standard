# Forked
I forked from [nette/coding-standard](https://github.com/nette/coding-standard)

# Check & Fix Your Code with Nette Coding Standard

[![Downloads this Month](https://img.shields.io/packagist/dm/galek/coding-standard.svg)](https://packagist.org/packages/galek/coding-standard)
[![Build Status](https://travis-ci.org/JanGalek/coding-standard.svg?branch=master)](https://travis-ci.org/JanGalek/coding-standard)
[![Latest Stable Version](https://img.shields.io/packagist/v/JanGalek/coding-standard.svg)](https://github.com/JanGalek/coding-standard/releases)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](/LICENSE)


This is set of [sniff](https://github.com/squizlabs/PHP_CodeSniffer) and [fixers](https://github.com/FriendsOfPHP/PHP-CS-Fixer) combined under [EasyCodingStandard](https://github.com/Symplify/EasyCodingStandard) that **checks and fixes** your PHP code against [Coding Standard in Documentation](https://nette.org/en/coding-standard).


## What Rules are Covered?

This package covers **part of [official rules](https://nette.org/en/coding-standard)**, not all.

When you open [`/examples`](/examples) directory, all files you'll see are checked by this coding standard. The code might look invalid compared to Nette code you know, but it's only because this tool doesn't check it (yet).

All **general rules** you can find in [`coding-standard-php56.yml`](/coding-standard-php56.yml) file.


## Install and Use


### Local Setup

Installation into global folder named `coding-standard`:

```
composer create-project galek/coding-standard
```

Check coding standard:

```bash
coding-standard/ecs check src tests --config coding-standard/coding-standard-php56.yml
```

And fix it:

```bash
coding-standard/ecs check src tests --config coding-standard/coding-standard-php56.yml --fix
```

### Travis Setup

```yaml
# .travis.yml
install:
    - composer create-project galek/coding-standard temp/coding-standard

script:
    - temp/coding-standard/ecs check src tests --config temp/coding-standard/coding-standard-php56.yml
```
