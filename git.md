# Git

## Comandos

### Instalação
- Git:
    ```
    cd ~/.ssh
    ssh-keygen -t rsa -C "email" -f "github-username"
    ssh-add -K ~/.ssh/github-username
    clip < ~/.ssh/github-username.pub
    touch config
    ```
- Git <config>:
    ```
    #username account
     Host github.com-username
          HostName github.com
          User git
          IdentityFile ~/.ssh/github-username
    ```
- Clonar repositório:
    ```
    git clone git@github.com-{github-username}:username/reponame.git
    ```
- Alternar usuário:
    ```
    git config user.email "email"
    git config user.name "username"
    ```
- Adicionar repositório:
    ```
    git remote add origin git@github.com-{github-username}:reponame
    ```
- Publicar/Baixar:
    ```
    git push
    git pull
    ```
