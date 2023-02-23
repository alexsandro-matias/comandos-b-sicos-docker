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


# limitando memória RAM e CPU dos conteiners

docker stats php-A

docker update php-A -m 128M --cpus 0.2

docker run --name ubuntu-C -dti -m 128M --cpus 0.2 ubuntu

## Instalando programa no Ubuntu para simular o Stress dos recursos da máquina
apt update && apt install stress
stress --cpu 1 --vm-bytes 50m --vm 1 --vm-bytes 50m


# Configurando Redes no Conteiner
apt-get install iputils-ping
docker network create minha-rede
docker run -dit --name Ubuntu-B --network minha-rede  ubuntu


# Criando um Dockerfile

docker run -dti --name ubuntu-python ubuntu
docker exec -ti ubuntu-python bash


apt install python3 nano && apt clean


	<!-- nome = input("Qual é o seu nome? ")
	print (nome) -->



nano dockerfile

FROM ubuntu

RUN apt update && apt install -y python3 && apt clean

COPY app.py /opt/app.py

CMD python3 /opt/app.py

docker build . -t python-ubuntu



# Criando uma imagem personalizada do Apache

wget http://site1368633667.hospedagemdesites.ws/site1.zip

Dockerfile
==================

FROM debian

RUN apt-get update && apt-get install -y apache2 && apt-get clean

ADD site.tar /var/www/html

LABEL description="Apache Webserver 1.0"

VOLUME /var/www/html/

EXPOSE 80


ENTRYPOINT ["/usr/sbin/apachectl"]

CMD ["-D", "FOREGROUND"]


docker image build -t debian-apache:1.0 .

docker run  -dti -p 80:80 --name meu-apache debian-apache:1.0


# Criando imagens a partir de uma linguagem de programação
nome = input("Qual é o seu nome? ")
	print (nome)


FROM python

WORKDIR /usr/src/app

COPY app.py /usr/src/app

CMD [ "python", "./app.py" ]


# Criando imagens MultiStage
docker pull golang
docker pull alpine


package main
import (
    "fmt"
)

func main() {
  fmt.Println("Qual é o seu nome:? ")
  var name string
  fmt.Scanln(&name)
  fmt.Printf("Oi, %s! Eu sou a linguagem Go! ", name)
}


FROM golang as exec

COPY app.go /go/src/app/

ENV GO111MODULE=auto

WORKDIR /go/src/app

RUN go build -o app.go .

FROM alpine

WORKDIR /appexec
COPY --from=exec /go/src/app/ /appexec
RUN chmod -R 755 /appexec
ENTRYPOINT ./app.go


docker image build -t app-go:1.0 .
docker run -ti  app-go:1.0


# Enviando a imagem para o DockerHub
docker login

docker build . -t nome-de-usuário/my-go=app:1.0

docker push nome-deu-usuário/my-go=app:1.0


# Criando um servidor de imagens
docker run -d -p 5000:5000 --restart=always --name registry registry:2

docker logout

docker image tag [id] localhost:5000/meu-apache:1.0


curl localhost:5000/v2/_catalog


docker push  localhost:5000/my-go-app:1.0


nano /etc/docker/daemon.json 

	{ "insecure-registries":["10.0.0.189:5000"] }
	

systemctl restart docker

docker push  localhost:5000/my-go-app:1.0



# Referências


### O que são containers? 

https://www.ibm.com/br-pt/cloud/learn/containers

https://www.redhat.com/pt-br/topics/containers

 

### Diferenças entre containers e máquinas virtuais (VMs)

https://www.redhat.com/pt-br/topics/containers/containers-vs-vms

  

### O que é Docker? 

https://www.redhat.com/pt-br/topics/containers/what-is-docker

https://docs.microsoft.com/pt-br/dotnet/architecture/microservices/container-docker-introduction/docker-defined

  

### Comandos essenciais 

https://medium.com/xp-inc/principais-comandos-docker-f9b02e6944cd

https://docs.docker.com/engine/reference/commandline/docker/

https://dev.to/soutoigor/docker-imagens-containers-e-seus-principais-comandos-23p6 



### Exemplos com Docker Compose 
https://aws.amazon.com/pt/blogs/aws-brasil/como-conteinerizar-uma-aplicacao-em-15-minutos/ 

  

### O que é YAML? 
https://www.redhat.com/pt-br/topics/automation/what-is-yaml

  

### O que é o Docker Compose 
https://blog.4linux.com.br/docker-compose-explicado/

 

