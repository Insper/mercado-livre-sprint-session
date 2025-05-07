# Requisitos do projeto

Este documento descreve os requisitos funcionais e não funcionais do projeto, além de requisitos de estrutura da equipe. Os requisitos deste projeto estão divididos em algumas categorias: 

## Estrutura da equipe

Todas as equipes serão formadas por 4 estudantes. 

* Todas as equipes devem ser divididas em duas sub-equipes: MLEng e MLOps. Neste projeto vamos usar estas duas definições: 

    * **MLEng**: Equipe de Machine Learning Engineering. Esta equipe será responsável pelo entendimento dos dados e desenvolvimento do modelo de machine learning. Em algumas organizações, esta equipe também é chamada de equipe de *Data Science*.
    * **MLOps**: Equipe de Machine Learning Operations. Esta equipe será responsável por todos procedimentos relacionados a leitura e atualização de dados e modelos. Em algumas organizações, esta equipe também é chamada de equipe de *Data Engineering*.

As entregas de cada equipe são descritas em maiores detalhes logo abaixo.

Todas as entregas devem ser feitas via GitHub. Inclusive relatórios ou questionários. Estes devem ser escritos em [Markdown](https://www.markdownguide.org/). 

## Compreensão do problema

* Todos os membros da equipe precisam participar da reunião inicial do projeto com a equipe do Mercado Livre. O dia e horário deste curso estão na [agenda do projeto](./agenda.md).

* A equipe precisa entregar um documento respondendo as seguintes perguntas:  
    
    - qual é o problema que é necessário resolver? 
    - qual é a relação deste projeto com o resultado financeiro da empresa? 
    - por que este problema é relevante? 

## Análise exploratória de dados

A equipe de MLEng precisa entregar um relatório com a análise exploratória dos dados, respondendo as seguintes perguntas:

* Qual o tamanho do dataset?
* Quais são as variáveis disponíveis?
* Quais os tipos de dados disponíveis?
* Quais são as variáveis de entrada e saída do modelo?
* Fazer uma análise descritiva univaria e bivariada das variáveis mostrando os principais achados. 

## Pré-processamento e armazenamento dos dados

A equipe do Mercado Livre irá disponibilizar o dataset para treinamento e validação em algum serviço de armazenamento de dados privado.

* A equipe de MLOps precisa garantir que os dados estejam disponíveis e acessíveis para a equipe de MLEng. Todo o processo de cópia do dataset para o ambiente de treinamento deve ser automatizado. A equipe de MLOps deve garantir que os dados estejam disponíveis em um ambiente seguro e privado, e que estejam sempre atualizados para a equipe de MLEng. O script de cópia do dataset deve ser parametrizável considerando os cenários de treinamento e validação do modelo. 

* Todo pipeline de pré-processamento dos dados deve ser automatizado e documentado.

* Assim como o código, os dados também precisam fazer uso de um sistema de versionamento. É de responsabilidade da equipe de MLOps definir o sistema de versionamente. Mas, é de responsabilidade de ambas as equipes, MLOps e MLEng, o correto uso do mesmo.

## Engenharia de atributos

A equipe de MLEng precisa compreender o significado de todos os atributos do dataset e propor modificações nos mesmos: criação de novos atributos, transformação de atributos existentes, entre outras atividades com o objetivo de criar uma representação mais rica dos exemplos (transações). 

Todo o pipeline de engenharia de atributos precisa estar automatizado e no controle de versão adotado pela equipe. 

## Modelagem

* A equipe de MLEng deve implementar e testar diversos modelos visando otimizar resultados de negócio. 

* Os modelos devem ser salvos no repositório de modelos do projeto. A equipe de MLOps deve providenciar um repositório de modelos e ferramentas para versionamento dos modelos. Este respositório deve permitir a recuperação de qualquer modelo e sua respecitva versão em qualquer momento.

* A equipe de MLEng deve comparar os modelos desenvolvidos com o modelo *baseline* fornecido pela equipe do Mercado Livre. 

* O pipeline end-to-end para criação do modelo e avaliação precisa estar automatizado e documentado. 

## Avaliação e apresentação dos resultados

* A equipe de MLEng deve ser capaz de identificar quais são as melhores métricas para avaliação dos modelos.

* A equipe de MLEng deve apresentar os resultados obtidos com os modelos desenvolvidos, considerando as métricas escolhidas.

* A equipe do Insper deve ser capaz de apresentar o modelo desenvolvido e comparar os resultados obtidos com o modelo *baseline*.

## Deploy do modelo

* Os modelos desenvolvidos pela equipe do Insper devem ser armazenados em algum serviço de armazenamento e devem ter um controle de versão. Este controle de versão deve permitir recuperar qualquer versão do modelo pré-existente. 

* A equipe do Insper deve desenvolver um site web para demonstrar o uso do modelo. Um site que recebe uma transação e apresentar a tomada de decisão sobre a mesma. A equipe do Insper deve se organizar para decidir quem será responsável por este componente. 

* A equipe de MLOps deve criar uma infra-estrutura de *log* para registrar o uso do modelo. Todas as classificações precisam ser armazenadas, os atributos utilizados e os resultados relacionados, assim como outras informações, tais como, data, hora e versão do modelo utilizado. 

* A equipe do Insper deve desenvolver uma forma de uso do modelo em lote, ou seja, a partir de um arquivo com várias transações, o modelo deve ser capaz de analisar todos as transações e retornar um arquivo com os resultados.

* O mesmo serviço de *log* utilizado para o site web também deve ser utilizado para o uso em lote.

## Entregáveis e estrutura dos repositórios

* Cada equipe deve organizar os entregáveis do projeto em dois repositórios. Este repositório para os dados, scripts e modelos, e um segundo repositório para as aplicações que irão usar o modelo. 

* Os dados utilizados neste projeto não poderão ser armazenados no repositório do GitHub. As ferramentas para armazenamento e controle de versão dos dados deverão ser outras. 

* Todos os relatórios precisam ser escritos em Markdown e armazenados no repositório do projeto, inclusive a apresentação final. 

* Os scripts para pré-processamento dos dados, treinamento dos modelos e avaliação dos modelos precisam estar escritos em Python de preferência. Por favor, tentem utilizar o mínimo possível Jupyter Notebook para estas tarefas. O controle de versão dos scripts em Jupyter Notebook é muito difícil de ser feito. Talvez, o único momento onde será necessário usar Jupyter notebook é no pré-processamento dos dados e na análise exploratório. Mesmo assim, recomenda-se salvar um arquivo `.py` com a versão final.

## Gestão do projeto

* A equipe do Insper deve manter um kanban do projeto atualizado diariamente. A ferramenta de kanban deve ser a do GitHub Projects. 

* Os commits feitos nos repositórios devem ser feitos de forma organizada e com mensagens claras. 

* Os commits devem ser feitos regularmente. Em média, um commit por dia por membro da equipe é o esperado a partir do terceiro dia de projeto.

* Todos os membros de todas as equipes devem estar preparados para trabalhar entre 6 até 8 horas por dia no projeto.

## Documentação

* Ambos os repositórios precisam ter arquivos `README.md` com instruções claras de como instalar e executar os códigos.

* Todos os códigos devem ser salvos em arquivos `.py` e todos os relatórios (incluindo apresentação) devem ser escritos em Markdown.

* Todos os códigos devem ser documentados: (i) forneça nomes claros para as variáveis e funções; (ii) não documente coisas óbvias; (iii) criei documentação de alto nível para funções mais complexas. 