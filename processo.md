| [Home](home) | [Escopo e Cronograma](escopo) | [**Processo**](processo) | [Design/Mockups](design_mockups) | [Configuração](configuracao) | [Arquitetura](arquitetura) | [Código](codigo) | [BD](banco_dados) | [Qualidade](qualidade) | [Utilização](utilizacao) |
| :----------: | :---------------------------: | :----------------------: | :--------------: | :--------------------------: | :------------------------: | :--------------: | :---------------: | :--------------------: | :----------------------: |

# Processo de Desenvolvimento

## Descrição

Esta seção é dedicada a apresentar o processo de desenvolvimento do time, junto dela serão apresentados documentos referentes a maneira que o time se organizou e trabalha.

## Sumário

- [Git Workflow](#git-workflow)
- [Matriz de Responsabilidade](#matriz-de-responsabilidade)
- [Plano de Comunicação](#plano-de-comunicação)
- [Plano de Riscos](#plano-de-riscos)

## Git Workflow

### Branches

#### Nomes

Como padrão para nomes de branches, foi decidido o seguinte:

```
<tipoDeItem>-<nomeDoItem>
```

Exemplo de Componentes:

```
component-navBar
component-slider
```

Exemplo de Páginas:

```
page-recipes
page-creations
```

#### Criação

Para garantir que o processo de desenvolvimento esteja sempre atualizado, lembre-se de executar o seguinte comando na branch dev antes de criar uma branch nova:

```
git pull origin dev
```

Depois da execução desse comando é necessário oficialmente criar a Branch, para isso, execute o seguinte comando:

```
git checkout -b <nomeDaBranch>
```

Assim que criar a branch, é necessário fazer um `push`para garantir que a mesma estará remota:

```
git push --set-upstream origin <nomeDaBranch>
```

Pronto! Agora você já pode começar a programar na sua Branch.

### Commits

Para que o código desenvolvido seja salvo em sua branch de maneira remota, é necessário realizar os comandos de `commit` e `push`

#### Salvando Localmente

Para garantir que apenas o código necessário para funcionamento da tarefa lembre-se de realizar o comando `add` apenas nos arquivos **essenciais** para a tarefa:

```
git add <nomeDoArquivo>
```

Depois de adicionar todos os arquivos que deseja salvar, execute o commando de commit com uma mensagem curta que represente o que foi trabalhado nesses arquivos adicionados:

```
git commit -m 'descrição da tarefa em português'
```

Não hesite em realizar vários commits, assim podemos ter docuemntado e salvo vários estados do desenvolvimento

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