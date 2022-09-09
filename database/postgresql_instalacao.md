[![](https://img.shields.io/badge/P%C3%A1gina%20Inicial-323330?style=for-the-badge)](home)
[![](https://img.shields.io/badge/Instala%C3%A7%C3%A3o-323330?style=for-the-badge)](Instalação)

---

# Instalação do PostgreSQL

* Versão do PostgreSQL para baixar: ![PostgreSQL12](https://img.shields.io/badge/PostgreSQL-12-blue)

## Glossário

* [**Linux**](database/postgresql_instalacao#linux)
* [**Windows**](database/postgresql_instalacao#windows)

---

<a name="linux"></a>

## Linux

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

## PostgreSQL no Windows

* Acesse este site para fazer [Download](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads)

* Baixe a versão **12.12** do PostgreSQL 
<img src="resources/images/install_windows/1.png">

---

* Ele vai começar a baixar e vai mostrar um tutorial de como instalar, mas esse aqui ja é o suficiente, com detalhes para o nosso projeto
<img src="resources/images/install_windows/2.png">

---

* Deixe terminar de baixar

<img src="resources/images/install_windows/3.png">

---

* Após baixado, clique no **.Exe** e libere as permissões para começar a instalar o programa. 

<img src="resources/images/install_windows/4.png">

---

* Mantenha o diretório padrão de instalação e clique em **NEXT**

<img src="resources/images/install_windows/5.png">

---

* Deixe todas as opções marcadas e só clique em **NEXT**

<img src="resources/images/install_windows/6.png">

---

* Ele vai mostrar qual pasta vai ser instalado os extras, mantenha o padrão e clique em **NEXT**

<img src="resources/images/install_windows/7.png">

---

* O **usuário** e **senha** padrão para teste local é [**posgtres**](), depois de colocar nos dois clique em **NEXT**

<img src="resources/images/install_windows/8.png">

---

* A porta liberada para o projeto deve ser a porta [**5433**](), só clique em **NEXT**
<img src="resources/images/install_windows/9.png">

---

* Selecione a linguagem para o Português do brasil e clique em **NEXT**

<img src="resources/images/install_windows/10.png">

---

* Ele vai mostrar um resumo de tudo que vai ser instalado e alterado, só clicar em **NEXT**

<img src="resources/images/install_windows/11.png">

---

* Agora vai começar a instalação, deixe concluir ela

<img src="resources/images/install_windows/12.png">
<img src="resources/images/install_windows/13.png">

---

* Depois de instalado, ele vai pedir para começar um outro programa chamado **Stack Builder** para instalar os outros programas que vem junto com o PostgreSQL 

<img src="resources/images/install_windows/14.png">

---

* Selecione qual o sistema de banco de dados vai ser utilizado para fazer a instalação, **Tenha certeza** de qual banco postgreSQL está sendo usado

<img src="resources/images/install_windows/15.png">

---

* Selecione o **PgAgent** como extensão que deseja instalar, porque ele auxilia o pessoal do windows a visualizar dados

<img src="resources/images/install_windows/16.png">

---

* Diga qual o diretório onde ele vai instalar os extras, deixe o diretório padrão se esse diretório é no seu computador.

<img src="resources/images/install_windows/17.png">

---

* Deixe ele fazer a instalação dos extras

<img src="resources/images/install_windows/18.png">

---

* Após baixado todos os extras, somente clique em **NEXT** para continuar 

<img src="resources/images/install_windows/19.png">

---

## Instalação do PgAgent

* Agora vai começar a configuração do PgAgent, que vai instalar o programa **PgAdmin**, que é o visualizados do PostgreSQL dos bancos de dados, mas iremos usar como padrão o Datagrip, clique em **NEXT**

<img src="resources/images/install_windows/20.png">

---

* Nessa tela só clique em **NEXT**

<img src="resources/images/install_windows/21.png">

---

* As informações do Pgadmin devem ser as mesmas do postgres, portanto ele trás alguns dados padrão como abaixo, mas a senha tem que ser para o local [**postgres**](), depois só clique em **NEXT**

<img src="resources/images/install_windows/22.png">

---

* Usuario de acesso também, **usuário** e **senha** como [**postgres**]()

<img src="resources/images/install_windows/23.png">

---

* Clique em **NEXT** que ele vai começar a instalação do PgAgent

<img src="resources/images/install_windows/24.png">
<img src="resources/images/install_windows/25.png">

---

* Ele vai mostrar que foi criado o pgAgent e que foi criado o Schema padrão postgres

<img src="resources/images/install_windows/26.png">

---

* Só clicar **NEXT** nas próximas duas telas para finalizar

<img src="resources/images/install_windows/27.png">
<img src="resources/images/install_windows/28.png">

## Testando a instalação

* Procure por **PgAdmin** em seu computador

<img src="resources/images/install_windows/29.png">

---

* Clique para iniciar, ele vai mostrar uma área de carregamento

<img src="resources/images/install_windows/30.png">

---

* Quando finalizar o carregamento, ele vai pedir a senha de acesso, a senha é [**postgres**]() como definido na instalação.

<img src="resources/images/install_windows/31.png">

---

* No canto esquerdo, tem os servidores instalados em seu computador, procure pelo [**PostgreSQL 12**]()

<img src="resources/images/install_windows/32.png">

---

* Clique duas vezes encima dele e ele vai pedir outra senha, essa senha também é [**postgres**]()

<img src="resources/images/install_windows/33.png">

---

* Clique com o botão direito encima do nome do **Database** e selecione **Create > Database**

<img src="resources/images/install_windows/34.png">
<br>
<img src="resources/images/install_windows/35.png">

---

* Coloque o nome do database como **joinfut** (assim como está escrito) e deixe como owner o **postgres**
* Depois disso só clicar em **Save**

<img src="resources/images/install_windows/36.png">

---

* Ele vai criar o nosso database e vai mostrar no canto direito as informações sobre ele e ele vai aparecer no canto esquerdo, como mostrado abaixo

<img src="resources/images/install_windows/37.png">

---

## Acessando no Datagrip

* Agora iremos acessar o Datagrip e iremos conectar no banco de dados criado
* Clique no **+** bem na ponta esquerda do programa para podermos fazer uma conexão

<img src="resources/images/install_windows/38.png">

---

* Selecione a opção **Data Source** e depois **PostgreSQL**

<img src="resources/images/install_windows/39.png">

---

* Ele vai abrir para colocar as informações da conexão, antes de colocarmos os dados, temos que baixar as dependencias do drive do postgreSQL como mostra na imagem

<img src="resources/images/install_windows/40.png">

---

* Os dados essenciais para a conexão são
  * Nome do projeto é opcional, mas se quiser coloque **Projeto Joinfut**
  * Host é **localhost**
  * Port é **5433**
  * User é **postgres**
  * Password é **postgres**
  * Database é **joinfut**
  * URL é gerada automaticamente com os dados acima, É A MESMA URL QUE VAI APARECER NO BACKEND NO APPLICATION.PROPERTIES

* Clique em **Test Connection** para ver se foi configurado direito e depois em **Apply** e **OK**

<img src="resources/images/install_windows/41.png">

---

* Pronto! agora o datagrip vai configurar sozinho, iniciar o banco e abrir um console como abaixo, é nesse console que iremos colocar os comando em SQL do projeto

<img src="resources/images/install_windows/42.png">




