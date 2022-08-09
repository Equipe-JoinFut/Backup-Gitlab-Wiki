| [Home](home) | [Escopo e Cronograma](escopo) | [**Processo**](processo) | [Design/Mockups](design_mockups) | [Configuração](configuracao) | [Arquitetura](arquitetura) | [Código](codigo) | [BD](banco_dados) | [Qualidade](qualidade) | [Utilização](utilizacao) |
| :----------: | :---------------------------: | :----------------------: | :--------------: | :--------------------------: | :------------------------: | :--------------: | :---------------: | :--------------------: | :----------------------: |

# Processo de Desenvolvimento

## Descrição

Os processos implementados são processos utilizados no mercado de trabalho em projetos de larga escala, para auxiliar os alunos a entenderem como se desenvolve em equipes de alto padrão e costumes para auxiliar na organização de novas demandas

## Sumário

- [Nomenclaturas](#nomenclatura)
- [Git Workflow](#git-workflow)
- [Matriz de Responsabilidade](#matriz-de-responsabilidade)
- [Plano de Comunicação](#plano-de-comunicação)
- [Plano de Riscos](#plano-de-riscos)

## Nomenclaturas

---

Quando utilizamos o Gitlab/Github e queremos que o colega desenvolva um tópico específico, criamos algo chamado **Issue** no site de armazenamento de repositório, abaixo irei apresentar nomes e as nomenclaturas que iremos utilizar:

1. **Branch** = Local de trabalho do desenvolvedor, onde é uma cópia feita do diretório de desenvolvimento chamado _Master_ onde o desenvolvedor pode trabalhar tranquilo sem prejudicar o projeto, após finalizado a melhoria ou desenvolvimento feito nela, ele deve pedir para os supervisores verificarem se não vai prejudicar o projeto como um todo.
2. **Demanda** = Demanda é a nomenclatura na industria para definir a **Issue**, é um tópico de desenvolvimento que será desenvolvido por um programador e entregue para ser revisado.
3. **PR** = abreviação para **Pull Request** ou **Merge Request**, é uma requisição feita a partir de uma Branch para ser vinculado a Branch principal chamada _Master_.
4. **GIT** = Git é o software que utilizamos para gerenciar as alterações feitas no projeto, ele nos ajuda a desenvolver em equipe sem quebrar ou prejudicar o projeto do colega que está desenvolvendo junto ao mesmo tempo.

## Demandas

---

Uma demanda é um pedaço de tarefa que o desenvolvedor, é um pedaço de uma User Stories (US), onde deve ser apresentado o que o desenvolvedor deve fazer e entregar, tem que ser o mais direto e descritivo possível.

Para acessar as Demandas do projeto você tem que ir na aba **Issues** como mostra o vídeo abaixo:

<img src="resources\images\processo\Acessando_Issues.gif">

Temos uma estrutura de Issue específica, onde ela tem um template como esse abaixo:

<img src="resources\images\processo\Template Issue.png">

Quando é criado a Issue ela tem as seguintes informações:

<img src="resources\images\processo\Template Issue2.png">

O mais importante, além das informações da Issue e quem é o responsável, é o **Código** dela, que iremos utilizar diariamente e direto em nosso projeto, como você vai ver na nomenclatura da Branch e na mensagem do Commit.
 


## Git Workflow

---

### Nomes

---

#### Branches

Como padrão para nomes de branches, foi decidido o seguinte:

```
<nomeColega>/<tipoDemanda>/<codigoDemanda>
```

Exemplo de branchs:

```
fanto/feature/#1
fanto/bugFix/#346
fanto/architecture/#1230
```

#### Componentes

Exemplo de Componentes:

```
component-navBar
component-slider
```

#### Páginas

Exemplo de Páginas:

```
page-recipes
page-creations
```

---

#### Criação de Branches

---

##### Criação pelo Gitlab

* Uma forma simples de criar uma Branch é direto no Gitlab, onde acesse a página inicial do repositório e siga as instruções do GIF abaixo:

<img src="resources\images\processo\Criando_Branch_Gitlab.gif">

* A branch principal se chama **Main** e ela é bloqueada para não receber commits direto nela, por ser a Branch ativa que o cliente utiliza.

* Branches ativas são Branches que precisam estar 100% funcionando e que não devem ser mexidas se não foi validado e testado as modificações, podendo quebrar o projeto e ficar fora do ar para o cliente.

##### Criação pelo Console

* A forma mais comum de criação de uma Branch é pelo console (ou terminal) quando o repositório está clonado em sua maquina (mais informações em [Git]())

* Abaixo um video completo de criação de uma branch

<img src="resources\images\processo\Criando_Branch_Console.gif">

* Os comando utilizados são:

```
git pull
```
Git pull serve para trazer as atualizações que estão no repositório remoto (Gitlab)

```
git branch
```
Git branch serve para vermos qual é a Branch que estamos nesse momento, no vídeo tem uma extensão para powershell que mostra o nome da branch sempre que for um repositório GIT

```
git checkout -b fanto/architecure/#2
```
Git checkout -b serve para criar uma nova Branch e acessar ela automaticamente, onde ele espera que seja colocado o nome da branch depois do -b, essa Branch está seguindo o padrão definido no tópico nome de branches

```
git log
```
Git log serve para ver os Commits já feitos, onde mostra em qual Branch eles foram criados.

### Commits

---

#### Salvando Localmente

Para garantir que apenas o código necessário para funcionamento da tarefa lembre-se de realizar o comando `add` apenas nos arquivos **essenciais** para a tarefa:

```
git add <nomeDoArquivo>
```

Caso todos os arquivos modificados da Branch são essenciais, pode utilizar o ponto `.` para salvar todos os arquivos localmente, mas tenha muito cuidado para não salvar os arquivos que não são essenciais:

```
git add .
```

#### Padrão de Commits

Todos os commits devem começar com o **código da Issue** e uma mensagem direta do que foi feito naquele commit:

Exemplo de Issue:

<img src="resources\images\processo\Codigo_Issue.png">

Esse código marcado é o que deve vir antes da mensagem em português do que foi feito:

```
git commit -m "#1 Atualizando os nomes dos colegas"
```

Com isso, vai vincular automaticamente a Issue ao commit, facilitando o trabalho dos revisores e colegas para saber de onde veio as alterações e o que foi feito



**ATENÇÃO** se o commit não estiver nessa estrutura, o commit vai ser invalidado e deverá ser feito um SQUASH de commits com a estrutura correta.

Não hesite em realizar vários commits, assim podemos ter documentado e salvo vários estados do desenvolvimento

#### Salvando Remotamente

Depois de finalizar o desenvolvimento, envie todos os commits da sua máquina para o servidor remoto. Para isso depois de realizar as etapas de salvamento local, salve remotamente com o comando `push`:

```
git push
```

### Merge Requests

Depois de uma task ter sido desenvolvida e estiver pronta de acordo com os critérios de aceitação, é necessário que a mesma seja enviada para a branch de desenvolvimento. Para isso é necessário abrir um Merge Request pela platafora GitLab:

#### Criando o Merge Request

A criação pode ser realizada na seção Merge Requests do repositório em que a branch foi criada. Clicando no botão `New Merge Request` siga os seguintes passos:

1. Selecionar a branch de origem (sua branch de desenvolvimento);
2. Selecionar a branch de destino (branch dev);
3. Selecione `Compare branches and continue`
4. Em `Title`, escreva um título que descreva a funcionalidade adicionada ou bug corrigido;
5. Em `Description`, escreva uma descrição com uma breve justificativa nos arquivos que foram alterados;
6. Caso a tarefa seja visual (criação de componente/tela, correção de bug) adicione um gif exemplificando o uso (se considerar necessário);
7. Na seção `Assignee`, selecione `Assign to me` para que fique registrado quem foi o responsável pelo desenvolvimento daquela tarefa (a pessoa selecionada será chamada caso o revisor tenha dúvidas sobre a tarefa);
8. Em `Milestone` selecione a Sprint em que a tarefa foi realizada;
9. Em `Labels`selecione qual é o tipo de tarefa que foi realizada;
10. Por último, revise se os arquivos que estão sendo enviados estão corretos e clique em `Submit Merge Request`.

#### Revisando o Merge Request

A revisão de merge request pode ser realizada por qualquer desenvolvedor, mas é preciso da aprovação de pelo menos um AGES III ou AGES IV para que a mesma seja incorporada na dev.

Na hora de revisar o Merge Request, entre na branch em sua máquina e teste a funcionalidade/bug/componente/tela de acordo com os critérios de aceitação apresentados no [Airtable](https://airtable.com/tblV0c8w2YX9PZAAC/viw4mJkZmd28WlplE?blocks=hide).

Caso haja pendências, relacionadas a documentação do código, padronização ou arquivos enviados, não exite em realizar um novo commit na branch com as mudanças necessárias antes de realizar a integração.

## Matriz de Responsabilidade

Essa matriz foi desenvolvida para ajudar os membros do time a saberem seus papéis na dentro do processo de desenvolvimento.

| **Atividades**             | **AGES I** | **AGES II** | **AGES III** | **AGES IV** |
| -------------------------- | :--------: | :---------: | :----------: | :---------: |
| Alimentar a wiki           |            |             |              |             |
| Definir squads             |            |             |              |             |
| Definir marcos da sprint   |            |             |              |             |
| Quebra de tasks            |            |             |              |             |
| Desenvolvimento            |            |             |              |             |
| Code review                |            |             |              |             |
| Executar testes funcionais |            |             |              |             |
| Deploy da aplicação        |            |             |              |             |
| Apresentação da review     |            |             |              |             |

- I: Deve ser informado
- C: Deve ser consultado
- R: Responsável
- A: Aprova


## Plano de Comunicação

|           **Evento**           |                                                                                                                                                                                                                                **Descrição**                                                                                                                                                                                                                                | **Responsável** |          **Envolvidos**          |                                   **Frequência**                                    |               **Duração**               |
| :----------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-------------: | :------------------------------: | :---------------------------------------------------------------------------------: | :-------------------------------------: |
| Kick Off (Exemplo) | Primeiro encontro entre o time e os stakeholders do projeto. Nesse encontro são apresentados os principais itens do projeto e a ideia geral. Também são realizados questionamentos sobre o que foi apresentado, com a finalidade de ajudar nas definições dos requisitos do projeto em conjunto com o cliente. (Exemplo) | Cliente(s) (Exemplo) | AGES I, II, III, IV e Cliente(s) (Exemplo) | Uma vez (início do projeto) (Exemplo) |      1 hora - 1 hora e 30 minutos (Exemplo) |
| TBD... | TBD... | TBD... | TBD... | TBD... | TBD... |

---

## Plano de Riscos

| Risco                                                 | Prevenção                                                                                  | Contingência                                                                                  | Estratégia |
| ----------------------------------------------------- | ------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------- | ---------- |
| Atingir limite de uso gratuito da AWS (Exemplo) | Utilizar servidores apenas para validação, desligando-os quando não utilizados (Exemplo) | Alterar ambiente para outra conta de usuário (Exemplo) | Transferir (Exemplo) |
| TBD... | TBD... | TBD... | TBD... |