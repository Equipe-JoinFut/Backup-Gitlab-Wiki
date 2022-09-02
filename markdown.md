[![](https://img.shields.io/badge/P%C3%A1gina%20Inicial-323330?style=for-the-badge)](home)
[![](https://img.shields.io/badge/Processos-323330?style=for-the-badge)](processo)
[![](https://img.shields.io/badge/Design/Mockups-323330?style=for-the-badge)](design_mockups)
[![](https://img.shields.io/badge/Instala%C3%A7%C3%A3o-323330?style=for-the-badge)](Instalação)
[![](https://img.shields.io/badge/Escopo%20e%20Cronograma-323330?style=for-the-badge)](escopo)
[![](https://img.shields.io/badge/Arquitetura-323330?style=for-the-badge)](arquitetura)
[![](https://img.shields.io/badge/Configura%C3%A7%C3%A3o-323330?style=for-the-badge)](configuracao)
[![](https://img.shields.io/badge/Utiliza%C3%A7%C3%A3o-323330?style=for-the-badge)](utilizacao)
[![](https://img.shields.io/badge/C%C3%B3digo-323330?style=for-the-badge)](codigo)
[![](https://img.shields.io/badge/Banco%20de%20dados-323330?style=for-the-badge)](banco_dados)
[![](https://img.shields.io/badge/Qualidade-323330?style=for-the-badge)](qualidade)
[![](https://img.shields.io/badge/Markdown-FF4500?style=for-the-badge)](markdown)
[![](https://img.shields.io/badge/ger%C3%AAncia-323330?style=for-the-badge)](gerencia)
[![](https://img.shields.io/badge/squads-323330?style=for-the-badge)](squads)
[![](https://img.shields.io/badge/retrospectivas-323330?style=for-the-badge)](Retro)
[![](https://img.shields.io/badge/estudos-323330?style=for-the-badge)](estudos)

---

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
