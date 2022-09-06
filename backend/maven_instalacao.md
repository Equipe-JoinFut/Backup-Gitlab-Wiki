### Wiki normal

<br>

[![](https://img.shields.io/badge/P%C3%A1gina%20Inicial-323330?style=for-the-badge)](home)
[![](https://img.shields.io/badge/Instala%C3%A7%C3%A3o-323330?style=for-the-badge)](Instalação)

---

### Wiki Backend

<br>

[![](https://img.shields.io/badge/Página_inicial_backend-323330?style=for-the-badge)](backend/backend_home)
[![](https://img.shields.io/badge/Instalando_Java-323330?style=for-the-badge&logo=java&logoColor=white)](backend/java_instalacao)
[![](https://img.shields.io/badge/Instalando_maven-FF4500?style=for-the-badge)](backend/maven_instalacao)
[![](https://img.shields.io/badge/Instalando_postman-323330?style=for-the-badge)](backend/postman_instalacao)[![](https://img.shields.io/badge/Instalando_intellij-323330?style=for-the-badge)](backend/intellij_instalacao)
[![](https://img.shields.io/badge/Instalando_Datagrip-323330?style=for-the-badge)](backend/datagrip_instalacao)


<br>

[![](https://img.shields.io/badge/Utilizando_postman-323330?style=for-the-badge)]()

---

# Instalação do Maven

* Versão do Maven que iremos utilizar: ![](https://img.shields.io/badge/Maven-3.6.3-green)

## Glossário

* [**Linux**](backend/maven_instalacao#linux)
* [**Windows**](backend/maven_instalacao#windows)

---

<a name="linux"></a>

### Linux

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

<a name="windows"></a>

### Maven no Windows

* Baixe o Maven do projeto escolhido [Aqui](https://drive.google.com/file/d/1n8T50n9bRk9PEYk4jdpMbFRvyaHf5TXT/view?usp=sharing)
    * Coloque o .zip do maven no diretório **Downloads**

Clique com o botão direito encima do .zip do maven e procure pela opção **Extrair Tudo...**

<img src="resources/images/maven_windows/1.png">

Vai abrir uma página pedindo a localização para extrair, clique no botão **Procurar...**

<img src="resources/images/maven_windows/2.png">

Selecione o seu computador oficial de uso, normalmente o **C:/**

<img src="resources/images/maven_windows/3.png">

Selecione os **Arquivos de Programas (X86)**

<img src="resources/images/maven_windows/4.png">

Essa é a pasta para onde devemos enviar os dados do **.zip**

<img src="resources/images/maven_windows/5.png">

Clique no botão de **Extrair**

<img src="resources/images/maven_windows/6.png">

Dê a permissão para o seu computador poder fazer essa ação

<img src="resources/images/maven_windows/7.png">

Deixe ele concluir a extração

<img src="resources/images/maven_windows/8.png">

Pronto! ele vai criar um diretório nos arquivos de programas com o nome do programa e a versão dele.

<img src="resources/images/maven_windows/9.png">

Acesse a página **Editar as variáveis de ambiente do sistema**

<img src="resources/images/maven_windows/10.png">

Clique em **Variáveis de Ambiente**

<img src="resources/images/maven_windows/11.png">

Clique em **Novo...** na parte das variáveis do sistema

<img src="resources/images/maven_windows/12.png">

Copie e cole o caminho até a pasta do maven criada dentro dos Arquivos de Programas (x86), normalmente é o `C:/Program Files (x86)/apache-maven-3.8.6`

Coloque o nome dessa variável como **MAVEN_HOME**

<img src="resources/images/maven_windows/13.png">

Agora devemos clicar para editar o **Path** das variáveis de ambiente

<img src="resources/images/maven_windows/14.png">

Clique para criar um **Novo**

<img src="resources/images/maven_windows/15.png">

Coloque a variável do Maven criada e coloque a pasta interna dele chamada **bin**, dessa forma `%MAVEN_HOME%/bin`.

<img src="resources/images/maven_windows/16.png">

Agora iremos abrir um console com <kbd>Windows</kbd> + <kbd>R</kbd> e escrever **cmd**

<img src="resources/images/maven_windows/17.png">

Testamos para ver se instalou o maven com o comando `mvn -version`, se aparecer as informações de versão, significa que foi instalado com sucesso.

<img src="resources/images/maven_windows/18.png">
