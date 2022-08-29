[![](https://img.shields.io/badge/P%C3%A1gina%20Inicial-323330?style=for-the-badge)](home)
[![](https://img.shields.io/badge/Processos-323330?style=for-the-badge)](processo)
[![](https://img.shields.io/badge/Design/Mockups-323330?style=for-the-badge)](design_mockups)
[![](https://img.shields.io/badge/Instala%C3%A7%C3%A3o-FF4500?style=for-the-badge)](Instalação)
[![](https://img.shields.io/badge/Escopo%20e%20Cronograma-323330?style=for-the-badge)](escopo)
[![](https://img.shields.io/badge/Arquitetura-323330?style=for-the-badge)](arquitetura)
[![](https://img.shields.io/badge/Configura%C3%A7%C3%A3o-323330?style=for-the-badge)](configuracao)
[![](https://img.shields.io/badge/Utiliza%C3%A7%C3%A3o-323330?style=for-the-badge)](utilizacao)
[![](https://img.shields.io/badge/C%C3%B3digo-323330?style=for-the-badge)](codigo)
[![](https://img.shields.io/badge/Banco%20de%20dados-323330?style=for-the-badge)](banco_dados)
[![](https://img.shields.io/badge/Qualidade-323330?style=for-the-badge)](qualidade)
[![](https://img.shields.io/badge/Markdown-323330?style=for-the-badge)](markdown)
[![](https://img.shields.io/badge/ger%C3%AAncia-323330?style=for-the-badge)](gerencia)
[![](https://img.shields.io/badge/squads-323330?style=for-the-badge)](squads)
[![](https://img.shields.io/badge/retrospectivas-323330?style=for-the-badge)](Retro)
[![](https://img.shields.io/badge/estudos-323330?style=for-the-badge)](estudos)

---

# Instalação dos programas necessários para o desenvolvimento

---

## IDE

* Intellij (Em construção)
* Datagrip (Em construção)
* VSCODE (Em construção)

## Backend

* [**Postman**](#postman)
* [**Java**](#java)
* [**Maven**](#maven)

## Frontend

* 

## Database

* [**PostgreSQL**](#postgresql)
* Pgadmin 4 (Em construção)


---

### Postman

* [**Linux**](#postmanlinux)
* [**Windows**](#postmanwindows)

#### Postman Linux

* Acesse [Site oficial](https://www.postman.com/downloads/)
* Abra um console no diretório onde foi baixado o postman:

```shell
$ tar -xzvf tar -xzvf postman-linux-x64.tar.gz 
```

* Acesse o Diretório criado e rode o executável **Postman**

```shell
$ cd Postman
$ ./Postman
```

* Faça login no seu email Google
* Pode trocar o tema para escuro caso seja muito claro

---


### Java

* Versão do Java que iremos utilizar: `Java 11`

#### Linux

**Instalação do Java 11 no linux**

```shell
sudo apt install openjdk-11-jre-headless
```

* Para testar se instalou

```shell
java --version

#openjdk 11.0.16 2022-07-19
#OpenJDK Runtime Environment (build 11.0.16+8-post-Ubuntu-0ubuntu122.04)
#OpenJDK 64-Bit Server VM (build 11.0.16+8-post-Ubuntu-0ubuntu122.04, mixed mode, sharing)
```

**Instalação do Javac (Java compiler) no linux**

```shell
sudo apt install openjdk-11-jdk-headless
```

* Para testar se instalou

```shell
javac --version

#javac 11.0.16
```

**Java 11.0.16** é a ultima versão dessa versão do java


---

### Maven

#### Linux

* Abra um console e coloque os seguintes comandos

```shell
cd ~/Downloads/
wget https://mirrors.estointernet.in/apache/maven/maven-3/3.6.3/binaries/apache-maven-3.6.3-bin.tar.gz
tar -xvf apache-maven-3.6.3-bin.tar.gz
sudo mv apache-maven-3.6.3 /opt/
```

* Abra o arquivo do perfil (.profile) com o vim

```shell
vim ~/.profile
```

* Coloque no arquivo (copie e cole com Ctrl+ C e Ctrl + V) no arquivo

```shell
M2_HOME='/opt/apache-maven-3.6.3'
PATH="$M2_HOME/bin:$PATH"
export PATH
```

* Após colado essa info, feche o VIM com `:wq`
* Atualize o arquivo profile com o comando abaixo:

```shell
source ~/.profile
```

* Verifique se o maven foi devidamente instalado:

```shell
mvn -version

# Apache Maven 3.6.3 (cecedd343002696d0abb50b32b541b8a6ba2883f)
# Maven home: /opt/apache-maven-3.6.3
# Java version: 11.0.16, vendor: Ubuntu, runtime: /usr/lib/jvm/java-11-openjdk-amd64
# Default locale: pt_BR, platform encoding: UTF-8
# OS name: "linux", version: "5.15.0-46-generic", arch: "amd64", family: "unix"
```



---

### POSTGRESQL

* [**Linux**](#linux)
* [**Windows**](#windows)

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

<img src="resources/images/installation/conexao_datagrip.png">

* Com isso, estamos conectados no banco de dados e na base de dados que iremos utilizar

---



