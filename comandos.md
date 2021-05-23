# Comandos no terminal

## Instalações

### Git

```bash
> sudo apt install git
``` 

## Utilitários

### Criação de pastas

```bash
> mkdir nome-da-pasta
``` 

* Exemplo

  ```bash
  > mkdir Projects
  ``` 

### Navegar para um diretório

```bash
> cd nome-do-diretorio
``` 

* Exemplo

  ```bash
  > cd Projects
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

