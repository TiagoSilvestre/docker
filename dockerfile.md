## Dockerfile

#### Criando uma imagem a partir de um dockerfile:

Adicionar a linha FROM php:7.3-cli, no dockerfile e rodar o comando abaixo

```docker build -t test_swoole . ``` vai fazer o build de um dockerfile, na tag test_swoole, da pasta atual, ou seja vai criar uma imagem local

Apos isso rodar o ```docker images``` para ver a imagem criada

#### No dockerfile

FROM = imagem de referencia 
RUN = para rodar algum comando ex: RUN pecl install swoole

COPY = copia um arquivo da maquina para uma pasta do container ex: COPY index.php /var/www

EXPOSE = deixa uma porta exposta caso uma aplicação precise rodar nela dentro do container ex: EXPOSE 9501

ENTRYPOINT = comando responsavel por ser executado no container quando ele estiver rodando, sem um entrypoint o container nao fica rodando 
ex: ENTRYPOINT ["php", "/var/www/index.php", "start"] == vai executar comandos 



Rodar o container docker run -d --name swoole -p 9501:9501 test_swoole


docker build -t tiagosilvestre/php-swoole:latest . 