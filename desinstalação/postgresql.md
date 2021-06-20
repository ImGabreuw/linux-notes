# Como desistalar o PostgreSQL e pgAdmin no Ubuntu 20.04

### PostgreSQL

```bash
$ sudo apt --purge remove postgresql

$ dpkg -l | grep postgres

$ sudo apt --purge remove postgresql-13 postgresql-client-13 postgresql-client-common postgresql-common

$ sudo apt --purge remove pgdg-keyring
```

### pgAdmin

```bash
$ sudo apt autoremove pgadmin4

$ dpkg -l | grep pgadmin4

$ sudo apt --purge remove pgadmin4-desktop pgadmin4-server pgadmin4-web

$ sudo rm -rf /usr/pgadmin4
```

### Tutoriais 

Título | Link
:----------: | :----------:
Uninstall Postgresql & PgAdmin4 in Ubuntu 18.04.4 LTS | [medium](https://vipulgupta-19290.medium.com/uninstall-postgresql-pgadmin4-in-ubuntu-18-04-4-lts-9e00fc79adfa)
How to uninstall PostgreSQL Database Completely from Ubuntu 20.04 LTS or Linux | [youtube](https://www.youtube.com/watch?v=igHxugGeON0)
