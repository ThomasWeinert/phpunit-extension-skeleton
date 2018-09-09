# PHPUnit Extension Skeleton

A skeleton for an extension for [PHPUnit](https://phpunit.de/). It provides the necessary files and build scripts.
The ["Hello World" example](https://github.com/ThomasWeinert/phpunit-extension-skeleton-example) is based on the 
skeleton and implements a simple constraint and assertion for PHPUnit.
.

## Requirements

* [Composer](https://getcomposer.org/)
* [Phive](https://phar.io/)

## Usage

Use [Composer](https://getcomposer.org/) to create a new extension project from this skeleton. 

```
$ composer create-project thomasweinert/phpunit-extension-skeleton your-awesome-extension
```

Go into the new project directory.

```
$ cd your-awesome-extension
```

Install tools used to build and package your extension using Phive.

```
$ phive install
```

Start adding new 

## Build Targets

The repository includes a [Phing](https://www.phing.info/) build file. Phive installs
Phing and the other tools into the `tools/` subdirectory. 

### build

```
$ tools/phing build
```

Create a Phar package for the extension. The phar will be put into the `build/` directory. The name and information
for a Phive `manifest.xml` will be read from the `composer.json`. The latest tag from current Git branch will
be used as version number.

### clean

```
$ tools/phing clean
```

Delete build artifacts.

### package

```
$ tools/phing package
```

Create a Phar package for the extension and sign it using GPG. the first time you will be asked 
GPG user. The user will be stored in the `build.properties` file.

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





