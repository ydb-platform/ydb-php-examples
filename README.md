# YDB PHP Basic Example

## Prerequisites

- Install PHP 7.3+
- Install Composer
- Install PHP extensions:
    - grpc
    - bcmatch
    - curl

Bash commands:

```bash
sudo apt install php
curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer
sudo apt install php-pear
sudo pecl install grpc
sudo apt install php-curl php-bcmath
```

## Installation

Clone this repository.
```bash
git clone git@github.com:yandex-cloud/ydb-php-examples.git
cd ydb-php-examples
```

Copy the .env file:
```bash
cp .env.example .env
```

Edit your .env file:
```
# Common YDB settings
DB_ENDPOINT=ydb.serverless.yandexcloud.net:2135
DB_DATABASE=/ru-central1/b1gxxxxxxxxx/etnyyyyyyyyy

# Auto discovery
DB_DISCOVERY=false

# Auth option 1:
# OAuth token authentication
DB_OAUTH_TOKEN=AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA

# Auth option 2:
# Private key authentication
SA_PRIVATE_KEY_FILE=./private.key
SA_ACCESS_KEY_ID=ajexxxxxxxxx
SA_ID=ajeyyyyyyyyy

# Auth option 3:
# Service account JSON file authentication
SA_SERVICE_FILE=./sa_name.json

# Root CA file (dedicated server only)
YDB_SSL_ROOT_CERTIFICATES_FILE=./CA.pem

# Logging settings
USE_LOGGER=false
```

Install dependencies:
```bash
composer install
```

Or update dependencies:
```bash
composer update
```

Run the console application:
```bash
php console

php console whoami

php console list-endpoints

php console ls
php console mkdir test1
php console ls test1
php console rmdir test1

php console create table1
php console select table1
```
