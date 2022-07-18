| [Home](home) | [Escopo e Cronograma](escopo) | [Processo](processo) | [Design/Mockups](design_mockups) | [Configuração](configuracao) | [Arquitetura](arquitetura) | [Código](codigo) | [BD](banco_dados) | [Qualidade](qualidade) | [Utilização](utilizacao) |
| :----------: | :---------------------------: | :------------------: | :--------------: | :--------------------------: | :------------------------: | :--------------: | :---------------: | :--------------------: | :----------------------: |

# Instruções de Utilização da Wiki

## Descrição

Aqui serão apresentadas instruções para utilizar a wiki de maneira simples.

## Sumário

- [Adicionando Imagens](#adicionando-imagens)
  - [Clonando o Repositório](#clonando-o-repositório)
  - [Adicione as Imagens ao Repositório](#adicione-as-imagens-ao-repositorio)
  - [Referenciando as Imagens](#referenciando-as-imagens)
- [Formatações de Texto](#formatações-de-texto)
  - [Títulos](#títulos)
  - [Estilos](#estilos)
  - [Links](#links)
  - [Teclas](#teclas)
  - [Marcação](#marcação)
- [Estruturas de Texto](#estruturas-de-texto)
  - [Divisores](#divisores)
  - [Tópicos](#tópicos)
  - [Trecho de Código](#trecho-de-código)
  - [Citações](#citações)
  - [Tabelas](#tabelas)

## Adicionando Imagens

### Clonando o Repositório

No canto superior direito, selecione a opção `Clone Repository` e siga os passos até ter repositório da docuemntação no seu computador.

### Adicione as Imagens ao Repositório

Arraste a imagem ou imagens que deseja adicionar em alguma pasta do diretório `resources`.

### Referenciando as Imagens

Para referenciar a imagem escreva a seguinte no formato abaixo:

```
<img src="resources/images/imagem.png">
```

É possível alterar o tamanho da imagem utilizando as seguintes opções:

```
width="300"
height="200"
```

## Formatações de Texto

### Títulos

Na linguagem MarkDown, os títulos são representados pelo caractere `#` quanto mais `#` menos será o título

# Título 1

```
# Título 1
```

## Título 2

```
## Título 2
```

### Título 3

```
### Título 3
```

#### Título 4

```
#### Título 4
```

### Estilos

Para utilizar estilos no texto, envolva eles com símbolos específicos.

**Negrito**

```
**Negrito**
```

_Itálico_

```
*Itálico*
```

<ins>Sublinhado</ins>

```
<ins>Sublinhado</ins>
```

### Links

Para adicionar links, utilze o formato `[]()`

Exemplo Prático:
[Link para o Youtube](https://youtube.com)

Exemplo Técnico:

```
[Link para o Youtube](https://youtube.com)
```

Para referenciar outras partes do documento, insira o nome do mesmo

Exemplo Prático:
[Home](home)

Exemplo Técnico:

```
[Home](home)
```

### Teclas

Para referenciar teclas utilize a tag `<kbd/>`

Exemplo Prático:
<kbd>Ctrl</kbd>

Exemplo Técnico:

```
<kbd>Ctrl</kbd>
```

### Marcação

Para marcar textos utilize o símbolo `

Exemplo Prático:
`texto marcado`

Exemplo Técnico:

```
`texto marcado`
```

## Estruturas de Texto

### Divisores

Para adicionar um divisor/separador, simplesmente adicione o simbolo `---`

Exemplo Prático:

---

Exemplo Técnico:

```
---
```

### Tópicos

Para adicionar um tópicos adicione o símbolo `-` antes dos itens.

Exemplo Prático:

- Item 1
  - Item 2
    - Item 3

Exemplo Técnico:

```
- Item 1
    - Item 2
        - Item 3
```

### Trecho de Código

Para adicionar um trechos de código adicione o símbolo ` três veze seguidas no começo do código e no final do mesmo.

Exemplo Prático:

```
 public static void main(String args[]){
     System.out.println("Hello World");
 }
```

Exemplo Técnico:

````
.```.
public static void main(String args[]){
    System.out.println("Hello World");
}
.```.
````

> Não considerar os símbolos de `.`

### Citações

Para adicionar um citações adicione o símbolo `>` antes dos itens.

Exemplo Prático:

> Citação

Exemplo Técnico:

```
> Citação
```

### Tabelas

Para adicionar uma tabela utilize o formato providenciado abaixo:

Exemplo Prático:

|             | **Coluna 1** | **Coluna 1** |
| ----------- | :----------: | :----------: |
| **Linha 0** |   Item 0-0   |   Item 1-0   |
| **Linha 1** |   Item 0-1   |   Item 1-1   |
| **Linha 2** |   Item 0-2   |   Item 1-2   |

Exemplo Técnico:

```
|             | **Coluna 1** | **Coluna 1** |
| ----------- | :----------: | :----------: |
| **Linha 0** |   Item 0-0   |   Item 1-0   |
| **Linha 1** |   Item 0-1   |   Item 1-1   |
| **Linha 2** |   Item 0-2   |   Item 1-2   |
```
