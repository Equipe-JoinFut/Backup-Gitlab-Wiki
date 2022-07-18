| [Home](../home) | [**Adicionando Imagens**](./adicionando-imagens) | [Escrevendo em markdown](./escrevendo-em-markdown) | [Wiki no editor de texto](./wiki-no-editor-de-texto) |
| :--: | :--: | :--: | :--: |

# Como adicionar imagens no Gitlab

---
**Acesso Rápido**

---

* [Adicionando por um Editor de Texto](Extra/add_image#vscode)
* [Formas de Adicionar imagens em Markdown](Extra/add_image#adding)
* [Visualizacão das Imagens](Extra/add_image#organize)

---

<a name="vscode"></a>

## Adicionando por um Editor de Texto:

* Em editores, podemos colocar imagens em **diretórios que ficarão ocultos** para as pessoas que irão ler mas podemos manipular as imagens que estarão armazenadas

* Isso serve para quando trocarmos o local dos arquivos da Wiki para outro Repositório não sejam perdido as imagens.

### Como funciona:

* Primeiro criamos um Diretorio na nossa Wiki e Adicionamos uma imagem nele, no exemplo o Diretório **tutorial-imagens**

---

<img src="../resources/images/tutorial/gitlab.png">

---

* Agora essa imagem esta dentro de um Diretorio Oculto que so em um editor de texto como o VScode voce consegue ver, onde a unica coisa que devemos fazer agora e referenciar no Markdown a imagem que se encontra nesse Repositorio, que nos leva ao proximo topico abaixo



<a name="adding"></a>
## Formas de Adicionar imagens em Markdown

* Existem algumas formas de adicionar imagens no Markdown:
    * [Por link externo](Extra/add_image#extern)
    * [Por link interno](Extra/add_image#oculto)
    * [por html interno](Extra/add_imagem#html)

<a name="extern"></a>

## Por link Externo

iremos usar a seguine estrutura para trazer imagens externa ao Markdown:

```
![nome desejado da imagem](link da imagem)
```

Com essa estruturação podemos pegar um link qualquer de uma imagem e adicionar, colocando um nome para a imagem em si

`EXEMPLO:` 

* Em uma imagem na internet selecione `copiar o endereço da imagem`

* Coloque o link e o nome da imagem como abaixo

```
![Terminal](https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/144_Gitlab-512.png)
```

* vai aparecer como abaixo: 

![Terminal](https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/144_Gitlab-512.png)


<a name="oculto"></a>

## Por link interno

* Se voce estiver trabalhando com diretorios de imagens em um editor de texto como o vscode, podemos simplesmente chamar o arquivo de seu diretorio 

* por link se usa uma estrutura como abaixo para chamar a imagem
```
![nome da imagem](caminho/para/imagem)
```

Exemplo: 

* Descobrimos onde esta a nossa imagem:

<img src="../resources/images/tutorial/ocult-folder.png">

* Colocamos o caminho para a imagem do diretorio como abaixo 

```
![](../resources/images/tutorial/gitlab.png)
```

* Colocamos `..` em todo diretorio que nao for interno do Reposiorio, entao como o diretorio imagens e interno, devemos dizer todos os diretorio ate a imagem e a extensao dela

* Abaixo fica a imagem em si

![](../resources/images/tutorial/gitlab.png)


<a name="html"></a>

## Por html interno

* por html usamos a tag epecial do html para exportar imagem, dizendo como fonte o local da imagem e o titulo dela

```
<img src="caminho/para/imagem" tittle="nome da imagem">
```
* se desejamos **Transformar markdown em PDF**, devemos sempre chamar as imagens como `tag` 
* se desejamos **Fazer resize de imagens**, devemos usar também as tags, porque fica mais facil de usar, foi explicado mais a fundo [Aqui](add_image#organize)

`EXEMPLO:`

* Descobrimos onde esta a nossa imagem:

<img src="../resources/images/tutorial/ocult-folder.png">

* Colocamos o caminho para a imagem do diretorio como abaixo 

```
<img src="../resources/images/tutorial/gitlab.png">
```

* Colocamos `..` em todo diretorio que nao for interno do Reposiorio, entao como o diretorio imagens e interno, devemos dizer todos os diretorio ate a imagem e a extensao dela

* Abaixo fica a imagem em si

<img src="../resources/images/tutorial/gitlab.png">

<a name="organize"></a>

## Visualização das Imagens

* Podemos redefinir o tamanho e centralizar as imagens usando tags

```
<p align="center">
    <img src="imagem" height="300" tittle="nome imagem">
</p>
```

* `align=""` : e uma forma de orientar aonde a imagem vai ficar 
* `height=""` : define o tamanho que a imagem vai ficar na wiki

Exemplo:

* **CENTRALIZANDO**

```
<p align="center">
    <img src="../resources/images/tutorial/gitlab.png" height="100">
</p>
```
<p align="center">
    <img src="../resources/images/tutorial/gitlab.png" height="100">
</p>

* **Diversos tamanhos**

```
<img src="../resources/images/tutorial/gitlab.png" height="20">
<img src="../resources/images/tutorial/gitlab.png" height="50">
<img src="../resources/images/tutorial/gitlab.png" height="100">
<img src="../resources/images/tutorial/gitlab.png" height="200">
```

<img src="../resources/images/tutorial/gitlab.png" height="20">
<img src="../resources/images/tutorial/gitlab.png" height="50">
<img src="../resources/images/tutorial/gitlab.png" height="100">
<img src="../resources/images/tutorial/gitlab.png" height="200">