# Guia de Instalação

## # Java

```bash
# Atualiza os pacotes
$ sudo apt-get update

# Instalação do pacote JDK
$ sudo apt-get install default-jdk

# Instalação do pacote JRE
$ sudo apt-get install default-jre
```

## # Python

```bash
# Atualiza os pacotes
$ sudo apt-get update

# Adiciona o Python ao gerenciador de pacotes
$ sudo apt-add-repository ppa:deadsnakes/ppa -y

# Atualiza os pacotes
$ sudo apt-get update

# Instala o Python 3.8
$ sudo apt-get install -y python3.8-dev python3.8-distutils python3.8-pip

# Instala o virtualenv
$ pip3 install virtualenv
```

## [🔗](https://github.com/nvm-sh/nvm#install--update-script) Node

```bash
# Atualiza os pacotes
$ sudo apt-get update

# Baixa e executa o script de instalação
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash

# Adiciona as variáveis de ambiente do Node
$ export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")" [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"

# Recarrega as configurações do terminal
$ source ~/.bashrc

# Testando a instalação
$ nvm --version

# Reinicia o computador
$ reboot

# Instalação do Node
$ nvm install 12.18.4

# Testando a instalação
$ node --version
```

## # VSCode

```bash
# Atualiza os pacotes
$ sudo apt-get update

# Instala o VSCode via Snap
$ sudo snap install --classic code
```

## # DBeaver

```bash
# Atualiza os pacotes
$ sudo apt-get update

# Instala o DBeaver via Snap
$ sudo snap install dbeaver-ce
```

## # Git

```bash
# Atualiza os pacotes
$ sudo apt-get update

# Instala o git
$ sudo apt-get install git-all
```

## [🔗](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository) Docker Engine

```bash
# Atualiza os pacotes
$ sudo apt-get update

# Instala os pré-requisitos
$ sudo apt-get install ca-certificates curl gnupg lsb-release

# Adiciona o docker ao gerenciador de pacotes
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

$ echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

# Atualiza os pacotes
$ sudo apt-get update

# Instala o Docker Engine
$ sudo apt-get install docker-ce docker-ce-cli containerd.io

# Cria um grupo de usuários Docker
$ sudo groupadd docker

# Adiciona o usuário ao grupo
$ sudo usermod -aG docker $USER

# Reinicia o computador
$ reboot

# Testando a instalação
$ docker run hello-world
```

## [🔗](https://docs.docker.com/compose/install/#install-compose) Docker Compose

```bash
# Faz o download do Docker Compose
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

# Concede permissão de execução ao binário
$ sudo chmod +x /usr/local/bin/docker-compose

# Adiciona o auto complete
$ sudo curl -L https://raw.githubusercontent.com/docker/compose/1.29.2/contrib/completion/bash/docker-compose -o /etc/bash_completion.d/docker-compose

# Recarrega as configurações do terminal
$ source ~/.bashrc

# Testando a instalação
$ docker-compose --version
```
