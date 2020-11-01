## Docker Network

Existem 3 tipos de redes que se pode criar no docker

1. Bridge = é uma ponte de comunicação entre os containers, quando um container precisa conversar com outro tem uma network de bridge
2. None = essa config diz pro container que ele nao vai ter acesso a nenhuma rede externa
3. Host = quando o seu container fala com a rede do seu computador de igual pra igual


```docker network ls``` = traz as networks criadas

```docker network inspect bridge``` = traz mais informações sobre a rede, neste caso a bridge


### Criar network

```docker network create -d bridge my_network``` =  cria uma network do tipo bridge chamada "my_network"

### Testando a network criada

- Criar 2 containers e fazer um pingar no outro:

```docker run -d --name nginx3 --net=my_network nginx``` = cria um container passando a network criada acima

```docker run -d --name nginx4 --net=my_network nginx``` = cria outro container passando a network criada acima

- Entrar no bash de um deles e instalar o ping
```
docker exec -it nginx3 bash
apt-get update
apt-get install iputils-ping
ping nginx4
```
As informaçoes do ping irao aparecer na tela.
