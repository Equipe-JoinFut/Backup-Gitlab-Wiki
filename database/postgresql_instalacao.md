[![](https://img.shields.io/badge/P%C3%A1gina%20Inicial-323330?style=for-the-badge)](home)
[![](https://img.shields.io/badge/Instala%C3%A7%C3%A3o-323330?style=for-the-badge)](Instalação)

---

# Instalação do PostgreSQL

## Glossário

* [**Linux**](database/postgresql_instalacao#linux)
* [**Windows**](database/postgresql_instalacao#windows)

---

<a name="linux"></a>
##### Linux

- **POSTGRESQL**

1) Instalando o postgresql no linux

```shell
# criando o arquivo de configuração do postgresql
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'

# import das chaves do postgresql
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -

# atualizar o sistema
sudo apt-get update

# instalação do postgresql versão 12 e sua dependencia de contribuição
sudo apt-get -y install postgresql-12 postgresql-contrib

# testar se o postgres foi instalado com sucesso
apt show postgresql
# sudo systemctl status postgresql
sudo pg_isready
```

2) Dando uma senha para o postgres

```shell
# acessando o template inicial do postgres
sudo -u postgres psql template1

# Alterando o usuario postgres e colocando a senha (obs: não esqueça o ; final)
ALTER USER postgres with encrypted password 'postgres';

# Clique Ctrl + D para sair do postgres
# acesse o arquivo abaixo
sudo vim /etc/postgresql/12/main/pg_hba.conf

# troque a mensagem de vez de peer para md5 e depois salve no vim (:wq)
local all postgres md5

# reinicie o arquivo de configuração
sudo /etc/init.d/postgresql restart

# Acesse seu usuario
psql -U postgres

# se pedir a senha de depois logar, funcionou corretamente
```

3) Criando uma base de dados pelo console

```shell
# pelo console comum, iremos usar o comando createdb
createdb -h localhost -p 5432 -U postgres <nome base>
```

* onde está escrito `<nome base>` você coloca o nome da base de dados
* o comando oficial que iremos usar é o abaixo

```shell
createdb -h localhost -p 5432 -U postgres joinfut
```

* Ele vai pedir a senha do usuario postgres e vai criar

4) Acessando a base de dados em um programa

* O melhor programa do mercado para ele é o [**Datagrip**](https://www.jetbrains.com/datagrip/download/?source=google&medium=cpc&campaign=15034927825&term=datagrip&gclid=Cj0KCQjw9ZGYBhCEARIsAEUXITUIhh1cPnp63OxJKXGRFET-UVxhvsri2Iga3RZm5zSMqvaykbdsqKoaAji3EALw_wcB#section=linux)

* Nele, colocamos os dados necessários, como abaixo:

<img src="../resources/images/installation/conexao_datagrip.png">

* Com isso, estamos conectados no banco de dados e na base de dados que iremos utilizar

---

<a name="windows"></a>
#### PostgreSQL no Windows