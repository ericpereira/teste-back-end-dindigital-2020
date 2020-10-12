# Teste Back-end DinDigital 2020

Foi desenvolvido uma API REST com [Laravel 8](https://laravel.com/docs/8.x) e [Laravel Responder](https://github.com/flugger/laravel-responder) com autenticação usando [JWT](https://jwt-auth.readthedocs.io/en/develop/laravel-installation/).
Link para as rotas da API no [Postman](https://documenter.getpostman.com/view/4732214/TVRn36iL)  

### Instalação
```sh
$ git clone https://github.com/ericpereira/teste-back-end-dindigital-2020.git
$ cd teste-back-end-dindigital-2020
$ git submodule init
$ git submodule update
$ cd laradock
$ cp env-example .env
$ docker stop $(docker ps -a -q)
$ docker-compose up -d php-fpm apache2 mysql workspace
$ docker-compose exec --user=laradock workspace sh -c "cd /var/www && php7.3 /usr/local/bin/composer install && cp .env.example .env && php7.3 artisan key:generate && php7.3 artisan migrate:fresh --seed && php7.3 artisan db:seed --class=UserSeeder"
```
 
