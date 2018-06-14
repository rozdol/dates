PHP Class for Date manipulations
====================================


About
-----

Dedicated to Cyprus Otrhodox Calendar to be used in local projects and libraries.

Install
-------

cd to `your_project_root_dir`

```bash
composer require rozdol/dates:"v1.*"
```

in Table or Model or Controller

```php
use Rozdol\Dates\Dates;
$this->dates = new Dates();
$date_normalized = $this->dates->F_date('01/01/20', 1); // 01.01.2020
```

### Unit Test

`cd dates`

```bash
composer update rozdol/dates
```

To test
```bash
./vendor/bin/phpunit tests/
```

## Compose library Tutorial

```bash
mkdir dates
cd dates
composer init # or composer update
git init
git add composer.json
git commit -m 'Initial Composer'
mkdir src
```

Copy `src`

```bash
git add src
git commit -m 'Added initial source'
```

add to `composer.json`

```
	"autoload": {
        "psr-4": {
            "Rozdol\\": "src"
        }
    }
```

```bash
git add composer.json
git commit -m 'add autoloader'
git push origin master
```

Create github repo

```bash
git remote add origin git@github.com:rozdol/dates.git
git push origin master
```

- Login to [packagist.org](https://packagist.org/)
- Submit `https://github.com/rozdol/dates`
- on github add new release (v1.0.0)
- On packagist Update Package

cd to dates

```bash
composer require rozdol/dates:"v1.*"
```

in Table

```php
use Rozdol\Funcs\Test;
```


#### Connecting Github to Packagist

In Github->Settings->Integrations..->Add->Packagist
user: packagist user
api_key: packagist->User->Profile->Show API KEY
Domain: https://packagist.org

Test: New reslease in Github and check the version in Packagist


### Unit Tests

install local phpunit
```bash
composer require --dev phpunit/phpunit ^6
```

```bash
mkdir tests
cd tests
mkdir TestCase
cd TestCase
mkdir Funcs
```
edit `DatesTest.php`

`cd dates`
```bash
composer update rozdol/dates
```

To test
```bash
./vendor/bin/phpunit tests/
```

### Travis CI

```bash
git checkout -b travis
git add .travis.yml
git push origin travis
```

##### Detactach from original source

```bash
git remote -v
git remote remove origin
git remote add origin git@github.com:rozdol/dates.git
git push origin random_changes
```
