# Todos os erros que eu tive durante minha jornada com o Ubuntu 20.04

### "não foi possível obter trava /var/lib/dpkg/lock-frontend”

* Tutorial
  
  [![](http://img.youtube.com/vi/mcsD9TSU51c/hqdefault.jpg)](https://www.youtube.com/watch?v=mcsD9TSU51c)
  
### Permissão negada para editar o arquivo `go.mod` (sincronização de dependências)

Solução: `$ sudo chown <usuário>:<group> <arquivo>` (**Exemplo**: `$ sudo chown gabriel:gabriel go.mod`)

### Corrigir pacotes quebrados

* **Fonte**: [viva o linux](https://www.vivaolinux.com.br/topico/Duvidas-frequentes/-IMPOSSIVEL-CORRIGIR-PROBLEMAS-VOCE-MANTEVE-HOLD-PACOTES-QUEBRADOS)

* **Solução**
  
  ```shell
  sudo dpkg --configure -a
  sudo apt-get -f install
  sudo apt-get -f remove
  sudo apt-get update
  sudo apt-get upgrade
  ```
