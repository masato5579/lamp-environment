作りたい環境

- WEBサーバ1台 apache
- キャッシュはredies
- データベースはMySQL

stack
- Laravel v12.0.2
- PHP 8.4.4
- MySQL 8.4.4

-  /bin/bash -c "$(curl -fsSL https://php.new/install/mac/8.4)"
- source ~/.zshrc
- php -v
```
PHP 8.4.1 (cli) (built: Nov 21 2024 08:58:37) (NTS)
Copyright (c) The PHP Group
Zend Engine v4.4.1, Copyright (c) Zend Technologies
    with Zend OPcache v8.4.1, Copyright (c), by Zend Technologies
```
- composer global require laravel/installer
- laravel new example-app
Which starter kit would you like to install? > none
Which database will your application use? > MySQL
Default database updated. Would you like to run the default database migrations? > no
Would you like to run npm install and npm run build? > Yes
- cd example-app
- touch docker-compose.yml
