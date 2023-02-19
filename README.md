# Executando o conteiner
~~~docker
docker pull ubuntu
docker run ubuntu
docker run ubuntu sleep 10
docker run ubuntu sleep 1500
docker stop [id]
docker run --help
docker run -it ubuntu
~~~

# Executando aplicações dentro do conteiner

~~~ docker
docker run -dti  ubuntu 
docker exec -it [id ou nome]  /bin/bash
~~~



# Excluindo e nomeando contêineres

~~~ docker
docker stop [id]
docker rm [id]
docker rmi [imagem]

docker run -dti --name Ubuntu-A ubu
~~~


# Copiando arquivos para o contêiner
~~~ docker
docker exec -ti Ubuntu-A /bin/bash
docker exec Ubuntu-A mkdir /destino/
docker exec Ubuntu-A mkdir ls -l /
nano Arquivo.txt
docker cp arquivo.txt Ubuntu-A:/aula/
~~~


# Copiando arquivos do contêiner
~~~ docker
docker cp Ubuntu-A:/destino/Meuzip.zip  Zipcopia.zip
~~~


# Criando um contêiner do MySQL
~~~ docker
docker pull mysql
 
docker run -e MYSQL_ROOT_PASSWORD=senhaQualquer --name mysql-A -d -p 3306:3306 mysql

docker exec -it mysql-A bash

mysql -u root -p --protocol=tcp


CREATE DATABASE aula;
show databases;

docker inspect mysql-A

mysql -u root -p --protocol=tcp
~~~



# Acessando um container externamente
~~~ docker
docker run -e MYSQL_ROOT_PASSWORD=SenhaQualquer --name mysql-A -d -p 3306:3306 --volume=/data:/var/lib/mysql mysql

mysql -u root -p --protocol=tcp --port=3306

CREATE TABLE alunos (
    AlunoID int,
    Nome varchar(50),
    Sobrenome varchar(50),
    Endereco varchar(150),
    Cidade varchar(50)
);



INSERT INTO alunos (AlunoID, Nome, Sobrenome, Endereco, Cidade) VALUES (1, 'Carlos Alberto', 'da Silva', 'Av. que sobe e desce que ninguém conhece', 'Manaus');
~~~

# Salvando o Banco de Dados para a máquina host - Montando (mount) um local de armazenamento
Até agora, se fizéssemos a exclusão da imagem que contém o Banco de Dados, todos os dados seriam perdidos, para evitar isso, iremos configurar para salvar os dados fora do conteiner.

 ~~~ docker
docker run -e MYSQL_ROOT_PASSWORD=Senha123 --name mysql-A -d -p 3306:3306 --volume=/data:/var/lib/mysql mysql

mysql -u root -p --protocol=tcp --port=3306

CREATE TABLE alunos (
    AlunoID int,
    Nome varchar(50),
    Sobrenome varchar(50),
    Endereco varchar(150),
    Cidade varchar(50)
);



INSERT INTO alunos (AlunoID, Nome, Sobrenome, Endereco, Cidade) VALUES (1, 'Carlos Alberto', 'da Silva', 'Av. que sobe e desce que ninguém conhece', 'Manaus');
~~~

# Exemplos de tipos de mount
~~~
****bind mount *****

docker run -dti --mount type=bind,src=/opt/teste,dst=/teste debian

docker run -dti --mount type=bind,src=/opt/teste,dst=/teste,ro debian

***volumes****

docker volume create teste
docker volume ls

	/var/lib/docker/volumes/teste/_data
	
docker run -dti --mount type=volume,src=teste,dst=teste debian

docker volume rm teste


~~~

# Instalando Apache Contêiner
~~~ docker
docker run  --name apache-A -d -p 80:80 --volume=/data/apache-A:/usr/local/apache2/htdocs/ httpd

docker run  --name php-A -d -p 8080:80 --volume=/data/php-A:/var/www/html php:7.4-apache

~~~


~~~php
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8"/>
<title>Exemplo Apache</title>
</head>
<body>
<h1> OK !! Apache funcionando!!!!! </h1>
</body>
</html>

<?php
phpinfo();
?>
~~~
