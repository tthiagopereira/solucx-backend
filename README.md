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
* nano .env


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

# Cliente
* http://localhost:8080
  

* GET /api/cliente
* GET /api/cliente/{id}
* PUT /api/cliente/{id}
* DEL /api/cliente/{id}
* POST /api/cliente

# Colaborador

* GET /api/colaborador
* GET /api/colaborador/{id}
* PUT /api/colaborador/{id}
* DEL /api/colaborador/{id}
* POST /api/colaborador

# Loja
* GET /api/lojas
* GET /api/lojas/{id}
* PUT /api/lojas/{id}
* DEL /api/lojas/{id}
* POST /api/lojas
 
# Trasações
* GET /api/transacoes
* PUT /api/transacoes/{id}
* POST /api/transacoes
# Avaliação
* GET /api/avaliacao
* POST /api/avaliacao

