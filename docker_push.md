## Docker Push

Para subir as alterações commitadas do seu container para o repositório remoto, primeiro é necessário logar

```docker login```

Subir as alteraçoes para o remoto 

```docker push nomeDoRepositorio:Tag``` 

```docker push tiagosilvestre/nginx-commit:latest```

Remover o container

```docker rm + containerName ou containerID``` exclui o container

Remover a imagem

```docker rmi + containerName ou containerID``` exclui a imagem

Depois de remover a imagem do repositorio local, experimente baixa-la novamente do remoto

```docker run -d --name nginx -p 8080:80 tiagosilvestre/nginx-commit:v2```