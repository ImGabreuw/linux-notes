# Instalação do pgAdmin no Ubuntu 20.04

### Passo 1: Baixar as chaves públicas

* Abrir o terminal com o atalho: `CTRL + ALT + T`
* Instale a chave pública para o repositório: `sudo curl https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo apt-key add`

### Passo 2: Arquivo de configuração

* Crie o arquivo de configuração do repositório: `sudo sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'`

### Passo 3: Instalação do pgAdmin

* Instalar para os modos desktop e web: `sudo apt install pgadmin4`
* Instalar apenas no modo desktop: `sudo apt install pgadmin4-desktop`
* Instalar apenas para o modo web: `sudo apt install pgadmin4-web`

### Passo 4: Configuração do servidor Web 

> Esse passo é apenas para o modo web

* Configure o servidor web, se você instalou pgadmin4-web: `sudo /usr/pgadmin4/bin/setup-web.sh`
