# PHPUnit Extension Skeleton

A skeleton for an extension for [PHPUnit](https://phpunit.de/).

## Requirements

* [Composer](https://getcomposer.org/)
* [Phive](https://phar.io/)

## Usage

Use [Composer](https://getcomposer.org/) to create a new extension project from this skeleton. 

```
$ composer create-project thomasweinert/phpunit-example-extension your-awesome-extension
```

Go into the new project directory.

```
$ cd your-awesome-extension
```

Install tools used to build and package your extension using Phive.

```
$ phive install
```

## Build Targets

The repository includes a [Phing](https://www.phing.info/) build file. Phive installs
Phing and the other tools into the `tools/` subdirectory. 

### build

```
$ tools/phing build
```

Create a Phar package for the extension.

### clean

```
$ tools/phing clean
```

Delete build artifacts.

### package

```
$ tools/phing package
```

Create a Phar package for the extension and sign it using GPG.

### reformat

```
$ tools/phing reformat
```

Uses the [PHP Coding Standards Fixer](https://cs.sensiolabs.org/) to reformat the 
source code according the PHPUnit coding standard. 

### test

```
$ tools/phing test
```

Run unit tests.





