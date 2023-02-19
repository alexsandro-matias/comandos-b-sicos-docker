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