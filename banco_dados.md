[![](https://img.shields.io/badge/P%C3%A1gina%20Inicial-323330?style=for-the-badge)](home)
[![](https://img.shields.io/badge/Processos-323330?style=for-the-badge)](processo)
[![](https://img.shields.io/badge/Design/Mockups-323330?style=for-the-badge)](design_mockups)
[![](https://img.shields.io/badge/Instala%C3%A7%C3%A3o-323330?style=for-the-badge)](Instalação)
[![](https://img.shields.io/badge/Escopo%20e%20Cronograma-323330?style=for-the-badge)](escopo)
[![](https://img.shields.io/badge/Arquitetura-323330?style=for-the-badge)](arquitetura)
[![](https://img.shields.io/badge/Configura%C3%A7%C3%A3o-323330?style=for-the-badge)](configuracao)
[![](https://img.shields.io/badge/Utiliza%C3%A7%C3%A3o-323330?style=for-the-badge)](utilizacao)
[![](https://img.shields.io/badge/C%C3%B3digo-323330?style=for-the-badge)](codigo)
[![](https://img.shields.io/badge/Banco%20de%20dados-FF4500?style=for-the-badge)](banco_dados)
[![](https://img.shields.io/badge/Qualidade-323330?style=for-the-badge)](qualidade)
[![](https://img.shields.io/badge/Markdown-323330?style=for-the-badge)](markdown)
[![](https://img.shields.io/badge/ger%C3%AAncia-323330?style=for-the-badge)](gerencia)
[![](https://img.shields.io/badge/squads-323330?style=for-the-badge)](squads)
[![](https://img.shields.io/badge/retrospectivas-323330?style=for-the-badge)](Retro)
[![](https://img.shields.io/badge/estudos-323330?style=for-the-badge)](estudos)

---

# Banco de Dados

## Descrição

Para o sistema, foi definido que seria utilizado o banco de dados Postgres. Esta decisão foi tomada em conjunto com a equipe, após uma votação entre outras tecnologias levantadas no dia oito de agosto de dois mil e vinte e dois.

## Sumário

- [Modelagem](#modelagem)
  - [Esquema Conceitual](#esquema-conceitual)
  - [Esquema Lógico](#esquema-lógico)
- [Implementação](#implementação)
  - [Knex](#knex)
  - [Schemas](#schemas)
  - [Postgrees](#postgrees)

## Modelagem

<br>

### **Esquema Conceitual**

<br>

### Sprint 0

<br>

Durante a sprint zero, foram definidas as primeiras entidades que serão realizadas pela equipe, sendo elas os dois usuários maiores do sistema: Atleta e Clube.

Durante a primeira versão do projeto, foi definido que seria utilizado o método de especialização, criando-se uma entidade descrita como Usuário, contendo id e nome. A partir deste, foram criadas as entidades Atleta e Clube.

Para a entidade Atleta, temos os atributos:
- peso
- perna_dominante
- altura
- imc
- data_nascimento
- idade
- posicao
- estilo_jogo
- codigo_bid_cbf (opcionall)
- endereco
    - logradouro
    - numero
    - bairro
    - cidade
    - estado
    - pais

Para a entidade Clube, temos os atributos:
- cnpj
- inscricao_estadual
- inscricao_municipal
- endereco
    - logradouro
    - numero
    - bairro
    - cidade
    - estado
    - pais

Podemos ver também a entidade JoinFut, que representa o aplicativo neste modelo. E por fim a entidade Pesquisa, que neste modelo é meramente representativa da função de realizar pesquisas que a aplicação deve realizar.

<br>

A modelagem para esta etapa do proceso foi realizada com a ferramenta BrModelo em sua versão 3.31.

<br>

Abaixo, segue definida a modelagem conceitual do projeto na Sprint 0:

<img src="resources/images/database/JoinFut_Conceitual.png">

<br>

### Sprint 1

<br>

Seguindo o processo de modelagem na sprint 1, foram definidas novas entidades e relações no modelo conceitual do projeto. As entidades novas são: Subgrupos, Calendário e Peneira

A entidade Subgrupo se baseia na capacidade de um clube poder adicionar Atletas específicos a uma determinada lista. Ela é composta pelos atributos: 
- id_subgrupo
- id_atleta
- id_clube

A entidade Calendário é meramente ilustrativa, demonstrando a existência de um calendário dentro da aplicação.

E por fim a entidade Peneira, que se baseia na capacidade de peneiras serem criadas na aplicação para a divulgação patrocinada/oferecida por clubes em buscas de atletas. Ela é composta pelos atributos: 
- id_peneira
- data_peneira
- hora_inicio
- hora_fim

Também houveram alterações pequenas na entidade Atleta, com a adição de um novo atributo opcional, composto e multivalorado, que seria o histórico do atleta, relacionado a suas participações anteriores em outros clubes.

- historico_atleta
	- id_clube_anterior

<br>

Abaixo, o primeiro modelo desta etapa:

<img src="resources/images/database/JoinFut_Conceitual2.png">

<br>

Após a apresentação deste modelo, foi validado com os demais membros da equipe responsável pela modelagem, que alterações deveriam ser feitas para a melhor compreensão do modelo.

As alterações são resumidas em:
Remoção da entidade Calendário da modelagem.
Adição de um novo atributo na entidade Subgrupo, chamado: título.

A entidade Calendário fora removida devido ao fato que não havia necessidade de sua existência, vendo que o calendário na aplicação seria utilizado somente para a visualização de peneiras.

E adição de um novo atributo na entidade de Subgrupo fora simplesmente para que o usuário clube possa livremente dar nomes às listas de atletas que deseja criar.

<br>

Abaixo, o modelo com suas alterações:

<img src="resources/images/database/JoinFut_Conceitual3.png">

<br>

E, para a atualização do modelo conceitual do banco, os atributos de endereço dos usuários Atleta e Clube foram colocados juntamente com a entidade Usuário, para evitar redundância de dados. 

<br>

Abaixo, o modelo conceitual relacionado a esta atualização: 

<img src="resources/images/database/JoinFut_Conceitual4.png">

<br>

Durante a Sprint, tivemos novas informações apresentadas pelos Stakeholders, logo, foram necessárias novas atualizações no modelo do banco de dados. Estas tendo grande impacto na modelagem e alterando uma boa parte do modelo original proposto. 

Foi validado com o cliente que as peneiras da aplicação teriam uma troca de nome, agora chamadas de pré-selecao, possuidoras dos seguintes atributos:

- endereco
    - logradouro
    - numero
    - bairro
    - cidade
    - estado
    - pais

Essa pré-seleção é criada a partir de um subgrupo, e engloba a ação de um clube poder iniciar uma “peneira” com os atletas já pré-selecionados pelo clube em subgrupos.

Ocorreu também a adição do campo de email e de senha do usuário, juntamente com a remoção do histórico de clubes do atleta.

Abaixo, o modelo conceitual relacionado a esta atualização:

<br>

<img src="resources/images/database/JoinFut_Conceitual5.png">

<br>

E para a finalização do modelo conceitual, foi levantado com a equipe a necessidade de mais uma entidade, chamada de Avaliação. Esta entidade deve englobar a capacidade do clube de dar dar notas a um atleta após a conclusão de sua pré-seleção.

A entidade Avaliação possui os seguintes atributos:
- id_avalicao
- nota_clube

<br>

**Abaixo, o modelo conceitual da aplicação completo, englobando todas as requisições do cliente :**

<img src="resources/images/database/Joinfut_Conceitual6 .png">

<br>

### **Esquema Lógico**

<br>

### Sprint 1

<br>

TBD

## Implementação

TBD

### Knex

TBD

### Schemas

TBD

### Postgrees

TBD

### Ferramentas Utilizadas

- [BrModelo 3.31](https://www.sis4.com/brModelo/download.html).

<br>

*Wiki editada por: [Alexya Silva Rocha de Oliveira](https://tools.ages.pucrs.br/alexya.oliveira)*
