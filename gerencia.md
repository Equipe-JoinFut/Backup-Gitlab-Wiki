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
[![](https://img.shields.io/badge/Markdown-323330?style=for-the-badge)](markdown)
[![](https://img.shields.io/badge/ger%C3%AAncia-FF4500?style=for-the-badge)](gerencia)
[![](https://img.shields.io/badge/squads-323330?style=for-the-badge)](squads)
[![](https://img.shields.io/badge/retrospectivas-323330?style=for-the-badge)](Retro)
[![](https://img.shields.io/badge/estudos-323330?style=for-the-badge)](estudos)

---

# Área da Gerência do projeto

## Acesso rápido

- [**Termo de Abertura do Projeto**](#Termo)
- [**Estrutura Analítica do Projeto**](#EAP)
- [**Matriz de responsabilidade**](#Responsabilidade)
- [**Plano de Comunicação**](#Comunicação)
- [**Plano de Riscos**](#Riscos)
- [**Sprints**](#Sprints)
- [**User Story do projeto**](#US)

---

<a name="Termo"></a>

## Termo de Abertura do Projeto

<img src="resources\images\home\termo_abertura_joinfut.png">

---

<a name="EAP"></a>

## Estrutura Analítica do Projeto

<img src="resources\images\gerencia\EAP.jpg">

---

<a name="Responsabilidade"></a>

## Matriz de responsabilidade

Essa matriz foi desenvolvida para ajudar os membros do time a saberem seus papéis na dentro do processo de desenvolvimento.

| **Atividades**             | **AGES I** | **AGES II** | **AGES III** | **AGES IV** |
| -------------------------- | :--------: | :---------: | :----------: | :---------: |
| Alimentar a wiki           |      R     |      R      |       C      |      A      |
| Definir squads             |      I     |      I      |       I      |      A      |
| Definir marcos da sprint   |      I     |      I      |       I      |      A      |
| Quebra de tasks            |      I     |      I      |       C      |      A      |
| Desenvolvimento            |      R     |      R      |       A      |      A      |
| Code review                |      I     |      I      |       A      |      C      |
| Executar testes funcionais |      I     |      R      |       C      |      A      |
| Deploy da aplicação        |      I     |      I      |       A      |      R      |
| Apresentação da review     |      I     |      I      |       I      |      A      |

- I: Deve ser informado
- C: Deve ser consultado
- R: Responsável
- A: Aprova

---

<a name="Comunicação"></a>

## Plano de Comunicação

|           **Evento**           |                                                                                                                                                                                                                                **Descrição**                                                                                                                                                                                                                                | **Responsável** |          **Envolvidos**          |                                   **Frequência**                                    |               **Duração**               |
| :----------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-------------: | :------------------------------: | :---------------------------------------------------------------------------------: | :-------------------------------------: |
| Kick Off (Exemplo) | Primeiro encontro entre o time e os stakeholders do projeto. Nesse encontro são apresentados os principais itens do projeto e a ideia geral. Também são realizados questionamentos sobre o que foi apresentado, com a finalidade de ajudar nas definições dos requisitos do projeto em conjunto com o cliente. (Exemplo) | Cliente(s) (Exemplo) | AGES I, II, III, IV e Cliente(s) (Exemplo) | Uma vez (início do projeto) (Exemplo) |      1 hora - 1 hora e 30 minutos (Exemplo) |
| TBD... | TBD... | TBD... | TBD... | TBD... | TBD... |

---

<a name="Riscos"></a>

## Plano de Riscos

| Risco                                                 | Prevenção                                                                                  | Contingência                                                                                  | Estratégia |
| ----------------------------------------------------- | ------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------- | ---------- |
| Atingir limite de uso gratuito da AWS (Exemplo) | Utilizar servidores apenas para validação, desligando-os quando não utilizados (Exemplo) | Alterar ambiente para outra conta de usuário (Exemplo) | Transferir (Exemplo) |
| TBD... | TBD... | TBD... | TBD... |

<img src="resources\images\gerencia\plano de riscos.jpg">
---

<a name="Sprints"></a>

## Sprints

---

<a name="US"></a>

## User Storyes do projeto

<details>

<summary> US-01: Cadastro de atleta </summary>

**Como** usuário atleta, **gostaria** de cadastrar meu perfil no aplicativo, **para** que o mesmo esta disponível para visualização dos clubes.

* Campos utilizados para o cadastro:
    * Nome
    * Idade
    * Data de nascimento: 
    * Endereço (Rua, número da casa, bairro, cidade, estado, país)
    * CONTATO (e-mail, telefone, contatos dos responsáveis etc) – campo obrigatório
    * Altura
    * Peso
    * IMC (calculado automaticamente com dados de altura e peso)
    * Perna dominante
    * Posição 
    * Código do BID da CBF: (caso atleta tenha) – **CAMPO NÃO OBRIGATÓRIO**
    * Clubes por onde passou – Campo obrigatório
    * Doenças pré-existentes? Se sim, quais.
    * VIDEOS (Velocidade, força, resistência, passe, chute, domínio de bola, cabeceio, jogo “jogado”)
    * Estilo de jogo (ofensivo, defensivo)
    * Termo de consentimento de concessão de dados **(deixar apenas um modelo, não temos o documento redigido no momento)**

    <details>
    <summary> US-01.01: Tela de cadastro de atleta </summary>

    Construir a tela para colocar os dados do atleta para poder cadastrar.    

    </details>
    <details>
    <summary> US-01.02: Criar entidade atleta </summary>

    Construir a entidade no springboot com os dados necessários para o atleta e tendo as devidas validações, fazer o cálculo do IMC e verificar o envio desses dados para o banco de dados.   

    </details>
    <details>
    <summary> US-01.03: Integração </summary>

    Realizar a integração das funcionalidade do backend com o frontend, persistindo as informações no banco de dados quando fornecidas pela tela do aplicativo.  

    </details>
    <details>
    <summary> US-01.04: Verificar estrutura do banco de dados e inserir atletas </summary>

    Criar usuários no banco de dados.
    Averiguar se os dados criados correspondem com a geração do Springboot, salvamento das estruturas bases dos dados do jogador/atleta, ocultação de senhas e backups de SQL do que foi criado no projeto. 

    </details>
    


</details>