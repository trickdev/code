# Linux

## Comandos

### Instalações
- Instalar WSL:
    ```
    wsl --update
    wsl --set-default-version 2
    wsl --install
    ```
- Atualização:
    ```
    apt-get update
    ```
- Git:
    ```
    sudo apt install git
    ```
- Curl:
    ```
    sudo apt-get install curl
    ```
- Node:
    ```
    curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
    sudo apt install Node.js
    ```
- Yarn:
    ```
    npm install --global yarn
    ```
- Oh My Zsh:
    ```
    sudo apt install zsh sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
    ```
- Make:
    ```
    sudo apt install make
    ```
- NestJs:
    ```
    npm i -g @nestjs/cli
    ```
- Docker:
    ```
    sudo apt update && sudo apt upgrade
    sudo apt remove docker docker-engine docker.io containerd runc
    sudo apt-get install \
        apt-transport-https \
        ca-certificates \
        curl \
        gnupg \
        lsb-release \
        software-properties-common
    ```
- Docker no sources do Ubuntu:
    ```
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
    echo \
      "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
      $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
    ```
- Docker Engine:
    ```
    sudo apt-get update
    sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
    ```
- Permissão Docker:
    ```
    sudo usermod -aG docker $USER
    ```

### Logs
- Espaço em disco:
    ```
    wsl.exe --system -d <distribution-name> df -h /mnt/wslg/distro
    ```
- Nome da máquina:
    ```
    uname -a
    ```
- Recursos:
    ```
    cat /proc/cpuinfo
    ```
- Verificar status:
    ```
    sudo systemctl status <process-name>
    ```

### Criação
- Escrever arquivos:
    ```
    echo "content" > <file-name>
    ```
- Criar diretório:
    ```
    mkdir <dir-name>
    ```
- Criar arquivo:
    ```
    touch <file-name>
    ```
- Acessar diretório:
    ```
    cd <dir-name>
    ```
- Acessar arquivo:
    ```
    cat <file-name>
    ```
- Acessar root WSL:
    ```
    cd /mnt
    ```

### Execução
- Rodar docker:
    ```
    sudo service docker start
    ```
- Reiniciar WSL:
    ```
    wsl --shutdown
    ```
- Restart:
    ```
    systemctl restart <process-name>
    ```

### Exclusões
- Remover arquivo:
    ```
    rm -f <file-name>
    ```
- Remover diretório:
    ```
    rm -rf <dir-name>
    ```

### Configurações
- Limite recurso <C:/Users/<user-name>/.wslconfig>:
  ```
    [wsl2]
    memory=8GB
    processors=4
    swap=2GB
  ```
