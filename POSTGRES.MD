<div align="center">
    <img src="https://avatars0.githubusercontent.com/u/177543?s=200&v=4" width="200px">

# [POSTGRES](https://github.com/postgres)

</div>

## Instalação no Ubuntu

Criar arquivo no diretório:

    /etc/apt/sources.list.d/pgdg.list

Colar esse script no arquivo criado:

    deb http://apt.postgresql.org/pub/repos/apt/ focal-pgdg main

Executar comando no terminal:

    wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add - sudo apt-get update

Instalar o postgres e o pgAdmin4 com os comandos:

    apt-get install postgresql-12
    apt-get install pgadmin4

---

## Comandos úteis pelo terminal

Acessar o pg pelo terminal

    sudo su - postgres

Acessar pg como adm

    psql -U postgres

Lista todos os banco de dados disponíveis

    \l

Criar um novo banco

    createdb nome_do_banco

Acessa o banco especificado

    psql nome_do_banco

Lista as tabelas existentes no banco selecionado

    \dt

Alterar senha de usuário

    alter user postgres with password 'novasenha'

Sair do usuário

    \q

### ALTERAR SENHA DE USUÁRIO DO POSTGRES

    - sudo su - postgres
    - psql -d postgres -U postgres
    - alter user postgres with password 'novasenha'
