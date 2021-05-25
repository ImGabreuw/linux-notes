# Comandos no terminal

## Instalações

### Git

```bash
> sudo apt install git
``` 

## Utilitários

### Remove 

> rm = (r)e(m)ove

```bash
> rm nome-da-pasta
``` 

* Exemplo

  ```bash
  > rm Projects
  ``` 

### Criar diretório

> mkdir = (m)a(k)e (dir)ectory

```bash
> mkdir nome-da-pasta
``` 

* Exemplo

  ```bash
  > mkdir Projects
  ``` 

### Mudar de diretório

> cd = (c)hange (d)iretory

```bash
> cd nome-do-diretorio
``` 

* Exemplo

  ```bash
  > cd Projects
  ``` 

### Descobrir o usário atual

```bash
> whoami
``` 

### Listagem dos diretório

* Listagem dos nomes dos diretórios
  ```bash
  > ls
  ``` 

* Listagem dos diretórios (+ detalhado)
  ```bash
  > ls -l
  ``` 
  
* Listagem dos diretórios ocultos
  ```bash
  > ls -la
  ``` 

* OBS
  * `.` = diretório atual
  * `..` = diretório anterior  
  * diretórios que comecem com `.` são ocultados

### Ajuda sobre um comando (o que ele faz / quais opções são aceitas)

```bash
> man nome_do_comando
``` 

* Exemplo

  ```bash
  > man ls
  ``` 

## Aparência

### Flat-Remix

* Clone dos repositórios do tema
  ```bash
  > git clone https://github.com/daniruiz/flat-remix
  ```

  ```bash
  > git clone https://github.com/daniruiz/flat-remix
  ```

* Criando um diretório para o tema e icones
  ```bash
  > mkdir -p ~/.icons && mkdir -p ~/.themes
  ```
  
* Movendo todo o conteúdo clonado para o diretório criado
  ```bash
  > cp -r flat-remix/Flat-Remix* ~/.icons/ && cp -r flat-remix-gtk/Flat-Remix-GTK* ~/.themes/
  ```

* Instalando o nome-tweak-tool
  ```bash
  > sudo apt install gnome-tweak-tool fonts-hack-ttf -y
  ```
* Basta seguir as instruções para a troca do tema: [guia](https://www.osradar.com/install-flat-remix-theme-ubuntu/)
  
