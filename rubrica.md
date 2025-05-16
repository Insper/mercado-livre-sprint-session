# Rubrica

A rubrica deste projeto é dividida por grupos apresentados abaixo. 

## Setup do projeto

| Grupo | Requisito | Data de entrega | Conceito | 
|-------|-----------|-----------------|----------|
| Estrutura da Equipe | [Definição da estrutura da equipe](./requisitos.md#estrutura-da-equipe) | 19/05 | D |
| Compreensão do problema | [Entrega do documento de compreensão do problema em markdown no repositório do projeto](./requisitos.md#compreensão-do-problema) | 21/05 | D |
| Análise exploratória de dados | [Entrega do relatório de análise exploratória de dados](./requisitos.md#análise-exploratória-de-dados) | 23/05 | D |
| Estrutura dos repositórios | [Cada equipe deve ter dois repositórios: um para o desenvolvimento do modelo e outro para o desenvolvimento das aplicações](./requisitos.md#estrutura-dos-repositórios) | 20/05 | D |

## Aquisição e pré-processamento dos dados

| Grupo | Requisito | Data de entrega | Conceito | 
|-------|-----------|-----------------|----------|
| Pré-processamento e armazenamento dos dados | [Garantir que os dados estejam disponíveis e acessíveis para a equipe de MLEng](./requisitos.md#pré-processamento-e-armazenamento-dos-dados) | 21/05 | C |
| Pré-processamento e armazenamento dos dados | [Automatizar o pipeline de pré-processamento dos dados](./requisitos.md#pré-processamento-e-armazenamento-dos-dados) | 26/05 | B |
| Pré-processamento e armazenamento dos dados | [Definir um sistema de versionamento dos dados e modelos](./requisitos.md#pré-processamento-e-armazenamento-dos-dados) | 26/05 | A |
| Modelagem | [Automatizar todo o pipeline end-to-end para criação e avaliação de modelos](./requisitos.md#pré-processamento-e-armazenamento-dos-dados) | 30/05 | A |

## Engenharia de atributos

| Grupo | Requisito | Data de entrega | Conceito | 
|-------|-----------|-----------------|----------|
| Engenharia de atributos | [Experimentar diversos métodos para engenharia de atributos](./requisitos.md#engenharia-de-atributos) | 28/05 | B |
| Engenharia de atributos | [Propor modificações que realmente agregam valor](./requisitos.md#engenharia-de-atributos) | 03/06 | A |


## Desenvolvimento e avaliação dos modelos

| Grupo | Requisito | Data de entrega | Conceito | 
|-------|-----------|-----------------|----------|
| Modelagem | [Definir a correta separação do dataset em treinamento, teste e validação](./requisitos.md#modelagem) | 23/05 | C | 
| Modelagem | [Implementação de um pipeline para geração modelos](./requisitos.md#modelagem) | 26/05 | C |
| Modelagem | [Implementação de modelos e avaliação dos mesmos](./requisitos.md#modelagem) | 03/06 | A |

## Apresentação dos resultados

| Grupo | Requisito | Data de entrega | Conceito | 
|-------|-----------|-----------------|----------|
| Apresentação dos resultados | [Identificar as melhores métricas para avaliação dos modelos](./requisitos.md#avaliação-e-apresentação-dos-resultados) | 23/05 | C |
| Apresentação dos resultados | [Definir um pipeline correto para avaliação dos modelos](./requisitos.md#avaliação-e-apresentação-dos-resultados) | 27/05 | C |
| Apresentação dos resultados | [Apresentar os resultados obtidos com os modelos desenvolvidos](./requisitos.md#avaliação-e-apresentação-dos-resultados) | 05/06 | B |
| Apresentação dos resultados | [Apresentar os modelos resultados obtidos com os modelos do ponto de vista de negócio](./requisitos.md#avaliação-e-apresentação-dos-resultados) | 05/06 | A |
| Apresentação dos resultados | [Entregar um relatório técnico em markdown no repositório do projeto](./requisitos.md#avaliação-e-apresentação-dos-resultados) | 05/06 | A |

## Deploy dos sistemas e modelos

| Grupo | Requisito | Data de entrega | Conceito | 
|-------|-----------|-----------------|----------|
| Deploy | [Armazenar as versões dos modelos usando uma ferramenta específica para isto](./requisitos.md#deploy) | 23/05 | C |
| Deploy | [Implementar um site web que demonstra o modelo treinado](./requisitos.md#deploy) | 30/05 | B |
| Deploy | [Implementar uma rotina para análise de transações em lote](./requisitos.md#deploy) | 30/05 | B |
| Deploy | [Implementar uma infra-estrutura de log para monitoramento do modelo](./requisitos.md#deploy) | 30/05 | B |
| Deploy | [Deploy automático da aplicação ao atualizar o branch main](./requisitos.md#deploy) | 05/06 | A |
| Deploy | [Rotinas de testes automatizados para o site web e para a rotina em lote](./requisitos.md#deploy) | 05/06 | A |


## Organização da equipe

| Grupo | Requisito | Data de entrega | Conceito | 
|-------|-----------|-----------------|----------|
| Gestão de projetos | [Manter um kanban atualizado diariamente](./requisitos.md#gestão-de-projetos) | Diário | {OK, NOK} |
| Organização dos repositórios | [Todos os códigos devem ser salvos em arquivos `.py` e todos os relatórios (incluindo apresentação) devem ser escritos em Markdown](./requisitos.md#entregáveis-e-estrutura-dos-repositórios) | 05/06 | {OK, NOK} |
| Documentação | [Documentação adequada nos repositórios e artefatos do projeto](./requisitos.md#documentação) | 05/06 | {OK, NOK} |
| Compreensão do problema | [Participação na primeira reunião com a equipe do Mercado Livre](./requisitos.md#compreensão-do-problema) | 19/05 | {OK, NOK} |
| Gestão de projetos | [Commits diários e relevantes por parte de todos os integrantes da equipe](./requisitos.md#gestão-de-projetos) | Diário | {OK, NOK} |
| Gestão de projetos | [Commits organizados e claros](./requisitos.md#gestão-de-projetos). Por favor, considerem este [documento](https://bit.ly/insper_commits) de recomendações. | Diário | {OK, NOK} |

## Regras gerais

Se a equipe ficar com conceito D então todos os membros estão automaticamente reprovados. 

Para as equipes que tiverem conceito C ou superior, os itens de organização da equipe serão utilizados para definir o sinal do conceito (positivo, neutro ou negativo). As regras a serem aplicadas são:

* Se todos os itens de organização da equipe estiverem OK então o conceito será positivo. 
* Se algum item estiver NOK então o conceito será neutro. 
* Se dois itens estiverem NOK então o conceito será negativo. 
* Se três ou quatro itens estiverem NOK então a equipe receberá um conceito a menos do que o conceito obtido na rubrica. 
* Se cinco ou seis itens estiverem NOK então a equipe receberá dois conceitos a menos do que o conceito obtido na rubrica.

## Validação final do modelo

A equipe do Mercado Livre irá validar o modelo desenvolvido pelas equipes do Insper. A validação será feita com um dataset separado para este fim. O dataset de validação não será disponibilizado para a equipe do Insper durante o desenvolvimento, apenas no momento da validação. Esta validação irá ocorrer entre os dias 04/06 e 06/06 - a data exata ainda será definida. 

Todas as equipes irão executar o seu melhor modelo no dataset de validação. O resultado desta validação irá alterar o conceito final da equipe. O conceito final será definido da seguinte forma:

* Para o modelo como melhor desempenho a equipe terá o seu conceito increentado em 2 níveis. Por exemplo, se a equipe tinha A então o conceito final será A+. Se a equipe tinha B então o conceito final será A. Se a equipe tinha B+ então o conceito final será A+.
* Para o modelo com o pior desempenho a equipe terá o seu conceito decrementado em 2 níveis. Por exemplo, se a equipe tinha A então o conceito final será B. Se a equipe tinha B+ então o conceito final será C+. 
* Para o modelo com o segundo melhor desempenho a equipe terá o seu conceito incrementado em 1 nível. Por exemplo, se a equipe tinha A então o conceito final será A+. Se a equipe tinha B então o conceito final será B+. Se a equipe tinha C+ então o conceito final será B.
* Para o modelo com o segundo pior desempenho a equipe terá o seu conceito decrementado em 1 nível. Por exemplo, se a equipe tinha A então o conceito final será B+. Se a equipe tinha B+ então o conceito final será B. Se a equipe tinha C+ então o conceito final será C.
* Para os demais modelos e equipe o conceito permanecerá o mesmo.

## Faltas

Se o estudante faltar mais que 4 aulas durante a sprint então o seu conceito será no máximo B. Se o estudante faltar mais que 6 aulas durante a sprint então o seu conceito será no máximo C. Se o estudante faltar mais que 8 aulas então estará automaticamente reprovado. 

Esta regra pode ser resumida pela equação abaixo: 

$$
f(faltas)=
\begin{cases}
Reprovado & \quad \text{if $faltas \geq 9$}\\ 
C & \quad \text{if $faltas \geq 6$}\\
B & \quad \text{if $faltas \geq 4$}\\
\text{Sem limite de conceito} & \quad \text{if $faltas < 4$}
\end{cases}
$$

## Atividades extra projeto

Eventualmente, ao longo do sprint, o professor poderá solicitar que os alunos respondam algum tipo de questionário. Se o aluno não entregar a reposta deste questionário então o aluno receberá um conceito a menos do que o conceito obtido na rubrica, podendo até ser reprovado. 