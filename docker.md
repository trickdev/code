# Docker

## Definições
- Dockerfile: Arquivo para criar imagem
- docker-compose.yml: Arquivo de configurações Docker
- Makefile: Arquivo para executar comandos

## Comandos

### Criação
- Criar image: `docker build -t <image-name> .`

### Execução
- Executar: `docker run -p 80:80 <image-name>`
- Executar/volumes: `docker run -p 80:80 -v $(pwd)/html:/usr/share/nginx/html nginx`
- Executar/CLI: `docker run -it <image-name> bash` ou `docker exec -it <image-name> bash` ou `docker compose exec <image-name> bash`

- Subir Docker: `docker compose up` ou `docker compose up -d`
- Baixar Docker: `docker compose down`
- Baixar Container: `docker stop <container-id>`

### Logs
- Lista de imagens: `docker image list` ou `docker images ls` ou `docker images ls | grep mysql`
- Lista container: `docker compose ps -a` ou `docker ps` ou `docker ps -a`
- Informações do container: `docker inspect <container-name>`
- Lista da rede: `docker network ls`
- Exibir logs: `docker logs <container-name>` ou `docker logs <container-name> -f`
- NingX Config: `docker exec <container-name> cat /etc/nginx/conf.d/default.conf`

### Exclusões
- Remover todos volumes: `docker volume rm $(docker volume ls -q)`
- Remover todos container: `docker rm -f $(docker ps -a -q)`
- Excluir image: `docker rmi <image-id>` ou `docker -f rmi <image-id>`
- Excluir container: `docker rm <container-id>`
- Excluir todos container: `docker system prune`

### Commits
- Login: `docker login`
- Docker push: `docker push <image-name>:<tag>` (image-name = user-name/repository-name)
- Rename image: `docker image tag <original-image-name>` (image-name = user-name/repository-name)
- Baixar image: `docker pull <image-url>`
