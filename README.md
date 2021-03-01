#TESTE SOLUCX
* Ubuntu 20
* Docker
* Mysql 
* PHP 7.4
# Modelagem
![Alt text](tela%20relacional.png "Title")

API Documentação
https://documenter.getpostman.com/view/4150779/TWDdhsqB

# Recomendações usar o postman para testes

# Configurar projeto

* git clone https://github.com/tthiagopereira/solucx-backend.git
* cd solucx-backend
* composer install

# Configurar o arquivo .env

* cp .env.example .env

* DB_CONNECTION=mysql
* DB_HOST=mysql
* DB_PORT=3306
* DB_DATABASE=solucx
* DB_USERNAME=root
* DB_PASSWORD=12345

# Configurar Docker

* sudo docker-compose up -d
* verificar se os servisos subiu corretamente
* sudo docker container ls
* nginx, mysql, php 
* Caso não tenha subido de forma correta rode novamente esse comando sudo docker-compose up -d

# Criar banco de dados

* sudo docker exec -it mysql mysql -u root -p
* password: 12345
* create database solucx;
* exit ;
  
# Executar comando para criar as tabelas no banco de dados (Migration)

* sudo docker-compose run php php artisan migrate

# Usando o POSTMAN
