## Docker Commit

Existem duas formas de criar e construir nossas proprias imagens

1. Dockerfile 
2. Ou commitar em um container que já exista


Depois de subir um container e fazer alterçoes nele como por exemplo, instalar o vim, para commitar o estado do container:

```docker commit IdDoContainer nomeDaNovaImagemGerada``` gera na tag latest

```docker commit f03840a59c5e tiagosilvestre/nginx-commit:v2```  passando uma tag


Após gerar essa imagem, é possível vela nos repost?rios locais atrav?s do:

```docker images```

Gerar um novo container atrav?s da imagem gerada com o nomeDaNovaImagemGerada de tiagosilvestre/nginx-commit

```docker run -d --name=nginx2 -p 8082:80 tiagosilvestre/nginx-commit```

