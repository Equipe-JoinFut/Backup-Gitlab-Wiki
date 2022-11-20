[![](https://img.shields.io/badge/P%C3%A1gina%20Inicial-323330?style=for-the-badge)](home)
[![](https://img.shields.io/badge/Processos-323330?style=for-the-badge)](processo)
[![](https://img.shields.io/badge/Design/Mockups-FF4500?style=for-the-badge)](design_mockups)
[![](https://img.shields.io/badge/Instala%C3%A7%C3%A3o-323330?style=for-the-badge)](Instalação)
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

# Design do Sistema

## Descrição

Ao longo da _Sprint_ 0, o time desenvolveu as telas de baixa fidelidade com o objetivo de alinhar as expectativas de design com os _stalkeholders_. As telas foram pensadas buscando performar um fluxo intuitivo e de fácil entendimento para o futuro uso da aplicação.

Os protótipos de tela foram realizados através da ferramenta Figma, contando com a colaboração da equipe simultaneamente na edição das telas. O resultado total pode ser visualizado através do _link_ [Joinfut](https://www.figma.com/file/2Eqdteoq094EfowEjQz83E/JoinFut?node-id=0%3A1).

<br>

## Protótipos de Baixo Nível

Seguindo a ideia apresentada pelos _stakeholders_, foram primeiro criados modelos alguns modelos simples feitos a mão sobre as telas base, sendo elas as telas _login_ e cadastro.

<img src="resources/images/mockups/FotoQuadro.png">

<br>

Após este primeiro exemplo, a equipe deu andamento para a modelagem na ferramenta Figma, utilizando-se das cores pré apresentadas pelos stakeholders.

<br>

## Login 

 <br>

<img src="resources/images/mockups/Login.png">

<br> 

### Descrição:
Tela de _login_ da aplicação, onde o usuário pode fazer _login_ utilizando os dados cadastrados no sistema da Joinfut, ou realizar o cadastro no sistema da Joinfut.

<br>

## Escolha do usuário(fluxo)

<br>

<img src="resources/images/mockups/SouJogadorSouClube.png">

<br>

### Descrição:
Tela inicial de cadastro, onde é possível escolher o tipo de usuário que fará o cadastro.

<br>

## Pré Cadastro

<br>

<img src="resources/images/mockups/PreCadastro.png">

<br> 

### Descrição:
Tela de _login_ 2 da aplicação onde, após o usuário se identificar como clube ou atleta ao clicar em "Registre-se" no primeiro contato com o aplicativo, ele então preenche os primeiros dados que serão utilizados em seu cadastro: email e senha..

<br>

## Cadastro Atletas/Clubes

<br>

<img src="resources/images/mockups/CadastroJogador.png">
<img src="resources/images/mockups/CadastroClube.png">

<br>

### Descrição:
Telas de cadastro apresentadas para o usuário Atleta e usuário Clube, respectivamente. São requisitadas as informações necessárias para a inserção dos dados no banco do sistema. Próximo ao fim da página, há um botão para a validação dos dados.


<br>

## Termos de uso

<br>

<img src="resources/images/mockups/Termos.png">

<br>

### Descrição:
Tela de termos de uso. Cada usuário (atleta e clube), após realizar o cadastro no aplicativo, serão redirecionados para a tela onde constam os termos de uso do mesmo (cada termo é específico para o usuário em questão).

<br>

## Home calendário(atleta) & Menu lateral

<br>

<img src="resources/images/mockups/HomeCalendarioMenuLateral.png">

<br>

### Descrição:
Foi definido pela equipe que no fluxo do usuário, sua _homepage_ seria o calendário. Essa tela representa as datas que ocorrerão as peneiras, juntamente com os times que as estão oferecendo. Há também um _widget_ no canto superior direito que leva para um menu lateral. Neste menu existem as opções:
* Perfil: leva o atleta para a tela de seu perfil.
* Norificações: ---------

<br>

## Home filtro(clube) & Menu lateral

<br>

<img src="resources/images/mockups/HomeFiltroMenuLateral.png">

<br>

### Descrição:
Foi definido pela equipe que o fluxo do usuário clube, sua _homepage_ seria a tela de filtragem de atletas da aplicação. Nesta tela, o clube poderia selecionar atributos desejados em um atleta e o sistema da aplicação deveria devolver os atletas que mais se encaixam nas categorias. Há também um _widget_ no canto superior direito que leva para um menu lateral. Neste menu existem as opções: 
* Subgrupos: leva o clube para a tela de subgrupos.
* Créditos: ------------

<br>

## Subgrupos

<br> 

<img src="resources/images/mockups/Subgroup.png">

<br>

### Descrição:
Tela de subgrupos da aplicação. Nesta tela o clube pode visualizar as listas de atletas que faz parte de sua grupagem. É possível também criar um novo subgrupo e criar as pré seleções a partir de subgrupos já existentes. 

<br>

## Modal para criar uma pré-seleção

<br>

<img src="resources/images/mockups/Modal.png">

<br>

### Descrição:
Para um melhor fluxo, o time optou para criar um modal para, através dele, ser feita a criação da pré-seleção a partir de um subgrupo. Esse modal é acionado quando o usuário clica no símbolo "+", como mostra a figura acima. 

## Perfil do atleta

<br>

<img src="resources/images/mockups/PerfilAtleta.png">

<br>

### Descrição:
A tela do perfil do atleta compõem as características do atleta em questão: estilo de jogo, posição, avaliação do mesmo e um botão que leva para uma tela que contém os vídeos do atleta. Essa tela pode ser acessada em ambos fluxos (atleta e clube). 

<br>

## Tela dos vídeos do atleta

<br>


<img src="resources/images/mockups/Videos.png">

<br>

### Descrição:
A tela de vídeos do atleta constam os _links_ com os vídeos respectivos de cada categoria. Essa tela também é acessada por ambos fluxos (atleta e clube).

<br>

## Pré-seleção

<br>

<img src="resources/images/mockups/Preselecao.png">

<br>

### Descrição:
A última tela pensada para completar o fluxo foi a tela de pré-seleção. Nessa tela o clube pode encontrar a lista de cada subgrupo que gerou uma pré seleção com os respectivos atletas listados e, a partir do contato com o Joinfut, atualizar o sistema indicando quais jogadores confirmaram presença na pré-seleção.

<br>

## Protótipos de Alto Nível

<br>

Seguindo a mesma ordem dos protótipos de baixo nível, foram desenvolvidas as seguintes telas:

<br>

## Login

<br>

<img src="resources/images/altonivel/HomePage.png">

<br>

## Escolha do usuário(fluxo)

<br>

<img src="resources/images/altonivel/ClubeOuJogador.png">

<br>

## Pré Cadastro

<br>

<img src="resources/images/altonivel/CadastroDeUsuario.png">

<br>

## Cadastro Atletas/Clubes

<br>

<img src="resources/images/altonivel/AtualizacaoDeDadosAtleta.png">
<img src="resources/images/altonivel/AtualizacaoDeDadosClube.png">

<br>

## Termos de uso

<br>

<img src="resources/images/altonivel/Termos.png">

<br>

## Home Calendário(Atleta) & Menu Lateral

<br>

<img src="resources/images/altonivel/CalendarioDeUsuario.png">
<img src="resources/images/altonivel/MenuDoAtleta.png">

<br>

## Home Filtro(Clube) & Menu Lateral

<br>

<img src="resources/images/altonivel/BuscaDeAtletas.png">
<img src="resources/images/altonivel/MenuClube.png">

<br>

## Subgrupos

<br>

<img src="resources/images/altonivel/TelaDeSubgrupos.png">

<br>

## Modal para criar uma Pré-seleção

<br>

<img src="resources/images/altonivel/Modal.png">

<br>

## Perfil do Atleta

<br>

<img src="resources/images/altonivel/PerfilAtleta.png">

<br>

## Telas dos vídeos do Atleta

<br>

<img src="resources/images/altonivel/VideosDoAtleta.png">

<br>

## Pré-seleção

<br>

<img src="resources/images/altonivel/Peneiras.png">

<br>

Importante ressaltar que até o momento desta edição, a tela de pré-seleção se encontra como débito técnico para a entrega final (25/11) e portanto, haverá uma alteração na wiki após os integrantes realizarem a entrega do relatório final. 

<br>

## Logotipo

<br>

Os _stakeholders_ possuíam um logotipo original porém, ao decorrer do projeto foram realizadas algumas mudanças sugeridas pelo time. A seguir o logitipo original e o atualizado nessa mesma orgem:

<br>

<img src="resources/images/logos/LogoOriginal.png">
<img src="resources/images/logos/LogoAtualizado.png">

<br>

## Paleta de Cores

<br>

A paleta de cores original foi mantida pelo time na execução dos _mockups_ e nas telas desenvolvidas. 

<br>

<img src="resources/images/mockups/PaletaCores.png">

<br>

## Tipografia

<br>

Além da paleta de cores e do logotipo citados anteriormente, os _stakeholders_ também já possuíam uma fonte definida. 

<br>

<img src="resources/images/mockups/Tipografia.png">

<br>

## Elementos Visuais

<br>

Como elementos visuais, foi possível utilizar os seguintes nas telas já desenvolvidas dentro do aplicativo mobile:

<br>

## Subgrupos

<br>

<img src="resources/images/elementosvisuais/SubgruposElemento.png">

<br>

### Descrição:
Foi definido esse elemento para representar o botão de Subgrupos existente no menu lateral do fluxo do Clube, que possibilita o mesmo a acessar a tela que contém seus subgrupos criados.

<br>

## Busca de Jogadores

<br>

<img src="resources/images/elementosvisuais/BuscarJogadorElemento.png">

<br>

### Descrição:
Também no menu lateral do fluxo do Clube, é possível acessar a tela de busca de atletas através do botão representado por esse elemento.

<br>

## Peneiras

<br>

<img src="resources/images/elementosvisuais/PeneirasElemento.png">

<br>

### Descrição:
Como terceira e última opção do menu lateral do fluxo do Clube, pode-se acessar a tela das pré-seleções através do botão representado por esse elemento.

<br>

## Perfil

<br>

<img src="resources/images/elementosvisuais/PerfilElemento.png">

<br>

### Descrição:
Entrando no menu lateral do fluxo do Atleta, a primeira opção disponível permite que o atleta acesse seu perfil através do botão representado por esse elemento.

<br>

## Vídeos

<br>

<img src="resources/images/elementosvisuais/VideosElemento.png">

<br>

### Descrição:
O atleta pode também acessar seus vídeos através do botão representado por esse elemento, sugestivo ao ícone do youtube por conta de ser a plataforma onde os vídeos se encontram.

<br>

## Minha Agenda

<br>

<img src="resources/images/elementosvisuais/AgendaElemento.png">

<br>

### Descrição:
Como última opção no menu lateral do atleta, existe o botão que leva para o seu calendário, ou seja, sua tela home dentro do aplicativo. 

<br>

## Símbolo de +

<br>

<img src="resources/images/elementosvisuais/AdicionarElemento.png">

<br>

### Descrição:
Em várias telas foram utilizadas o elemento de adicção, afim de representar a ação que o usuário pode ter que adicionar/criar algum elemento de acordo com cada feature existente.

<br>

## Youtube símbolo

<br>

<img src="resources/images/elementosvisuais/YoutubeElemento.png">

<br>

### Descrição:
Na tela que consta os vídeos do atleta, também foi utilizado um elemento visual que fizesse analogia a plataforma do Youtube, porém dessa vez com as cores características vermelho e branco.

<br>

## Bola Logotipo

<br>

<img src="resources/images/elementosvisuais/BolaLogoElemento.png">

<br>

### Descrição:
Ao decorrer do projeto, foi sugerido pelo time aos stekeholders uma pequena mudança no logo e, para isso, foi utilizado o elemento visual de uma bola de futebol diferente do logo original.

<br>






