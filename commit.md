## Docker Commit

Existem duas formas de criar e construir nossas proprias imagens

1. Dockerfile 
2. Ou commitar em um container que j? exista


Depois de subir um container e fazer altera?oes nele como por exemplo, instalar o vim, para commitar o estado do container:

```docker commit IdDoContainer nomeDaNovaImagemGerada``` 

Ap?s gerar essa imagem, ? poss?vel vela nos repost?rios locais atrav?s do:

```docker images```

Gerar um novo container atrav?s da imagem gerada com o nomeDaNovaImagemGerada de tiagosilvestre/nginx-commit

```docker run -d --name=nginx2 -p 8082:80 tiagosilvestre/nginx-commit```


