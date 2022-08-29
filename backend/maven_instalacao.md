[![](https://img.shields.io/badge/P%C3%A1gina%20Inicial-323330?style=for-the-badge)](home)
[![](https://img.shields.io/badge/Instala%C3%A7%C3%A3o-323330?style=for-the-badge)](Instalação)

---

# Instalação do Maven

## Glossário

* [**Linux**](backend/maven_instalacao#linux)
* [**Windows**](backend/maven_instalacao#windows)

---

<a name="linux"></a>
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

<a name="windows"></a>
#### Maven no Windows