### Wiki normal

<br>

[![](https://img.shields.io/badge/P%C3%A1gina%20Inicial-323330?style=for-the-badge)](home)
[![](https://img.shields.io/badge/Instala%C3%A7%C3%A3o-323330?style=for-the-badge)](Instalação)

---

### Wiki Backend

<br>

[![](https://img.shields.io/badge/Página_inicial_backend-323330?style=for-the-badge)](backend/backend_home)
[![](https://img.shields.io/badge/Instalando_Java-FF4500?style=for-the-badge&logo=java&logoColor=white)](backend/java_instalacao)
[![](https://img.shields.io/badge/Instalando_maven-323330?style=for-the-badge)](backend/maven_instalacao)
[![](https://img.shields.io/badge/Instalando_postman-323330?style=for-the-badge)](backend/postman_instalacao)[![](https://img.shields.io/badge/Instalando_intellij-323330?style=for-the-badge)](backend/intellij_instalacao)
[![](https://img.shields.io/badge/Instalando_Datagrip-323330?style=for-the-badge)](backend/datagrip_instalacao)

<br>

[![](https://img.shields.io/badge/Utilizando_postman-323330?style=for-the-badge)]()

---

# Instalação do Java para o projeto

* Versão do Java que iremos utilizar: ![](https://img.shields.io/badge/JAVA-11.0.16-orange)

## Glossário

- [**Java no Linux**](backend/java_instalacao#linux)
- [**Java no Windows**](backend/java_instalacao#windows)

---

<a name="linux"></a>

### Linux

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

<a name="windows"></a>

### Java no Windows

* O arquivo para baixar o Java 11 para facilitar o trabalho se encontra [Aqui](https://drive.google.com/file/d/1oRNhV8FQokBOebcAWhkjy0zM0ih1hlvv/view?usp=sharing).
    * Esse arquivo é o **Java JDK**, é o Java necessário para o desenvolvimento nessa linguagem.

Para instalar o programa no windows, clique duas vezes nele e verá a seguinte página:

Clique em **Next**.

<img src="resources/images/java_windows/1.png">

Clique em **Next**.

<img src="resources/images/java_windows/2.png">

Ele vai instalar o Java em seu computador na pasta definida acima e configurar o JAVA_PATH automaticamente nas suas variáveis de ambiente, versões anteriores não faziam isso por nós.

<img src="resources/images/java_windows/3.png">

Depois de instalado, abra um terminal clicando <kbd>Windows</kbd> + <kbd>R</kbd> e escrevendo **cmd**.

<img src="resources/images/java_windows/4.png">

No terminal rode o seguinte comando: `java -version` para verificar se tem o java padrão instalado.

<img src="resources/images/java_windows/5.png">

Por último, para verificar se o JDK foi instalado com sucesso, rode o comando `javac -version`, se aparecer a mensagem da versão do java compiler, funcionou.

<img src="resources/images/java_windows/6.png">