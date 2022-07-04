
# Anbiente Docker Para Projetos PHP e Laravel


### Passo a passo
Clone Repositório
```sh
git clone https://github.com/wagnersorio/docker-php-81.git
```

```sh
cd docker-php-81/
```

Remova o versionamento
```sh
rm -rf .git/
```


Crie o Arquivo .env
```sh
cp .env.example .env
```


Atualize as variáveis de ambiente do arquivo .env
```dosini

NGINX_HTTP_PORT=8089

MYSQL_DATABASE=MYSQL_DB
MYSQL_ROOT_PASSWORD=root
MYSQL_PASSWORD=root
MYSQL_USER=root
MYSQL_PORT=33060

REDIS_PORT=6379 

MAILHOG_PORT=1025
MAILHOG_DASHBOARD_PORT=8025

```


Suba os containers do projeto
```sh
docker-compose up -d
```


Acessar o container
```sh
docker-compose exec php bash
```


Instalar as dependências do projeto
```sh
composer install
```


Gerar a key do projeto Laravel
```sh
php artisan key:generate
```

