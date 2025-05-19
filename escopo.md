# Prevenção de fraudes

## Objetivo

O objetivo deste projeto é desenvolver um modelo para identificação de fraudes em transações com cartão de crédito ou débito presenciais, sob o ponto de vista do adquiriente.

## Dataset disponível

O dataset disponibilizado para o desenvolvimento deste modelo possui aproximadamente 5 milhões de transações sintetizadas, simulando alguns padrões de fraude existentes na vida real. Tem-se poucos atributos prontos, o objetivo é que as equipes trabalhem com feature engineering a partir das características das transações. Como é um problema de fraude, é fácil perceber que se trata de um dataset altamente desbalanceado, aproximadamente 1% de fraudes.

### Descrição dos Datasets

#### payers-v1.feather

Este arquivo contém informações sobre todos os portadores de cartão (pagadores) do conjunto de dados.

**Download link:** https://drive.google.com/file/d/1IrwLgQP9upQcUwp_EiGUgqnuwfB3zHwa/view?usp=drive_link

##### Colunas:

card_hash: Identificador único para cada cartão (anonimizado).
card_bin: O BIN (Bank Identification Number) do cartão.
card_first_transaction: Data e hora da primeira transação realizada com este cartão no ambiente do adquirente.

#### seller_terminals-v1.feather

Este arquivo contém informações sobre todos os terminais de venda (pontos de venda) do conjunto de dados.

**Download link:** https://drive.google.com/file/d/1hoLpGW8-9tinekBdd32gLGPeJiUfJq8R/view?usp=drive_link

##### Colunas:

terminal_id: Identificador único de cada terminal.
latitude: Coordenada de latitude do terminal.
longitude: Coordenada de longitude do terminal.
terminal_operation_start: Data de início de operação do terminal.
terminal_soft_descriptor: Descrição ou rótulo textual do terminal, geralmente usada para categorização.

#### transactions_train-v1.feather

Estes arquivos contêm os dados transacionais.

**Download Link:** https://drive.google.com/file/d/1p-TcJUdjZgDHqi_GBsxNiVxksuPGeTTt/view?usp=sharing

##### Colunas:

transaction_id: Identificador único de cada transação.
tx_datetime: Data e hora da transação.
tx_date: Data da transação (sem o horário).
tx_time: Horário da transação (sem a data).
tx_amount: Valor da transação.
card_id: Identificador do cartão utilizado (corresponde ao card_hash em payers).
terminal_id: Identificador do terminal (corresponde ao terminal_id em seller_terminals).
is_transactional_fraud: 1 se a transação é rotulada como fraude transacional, 0 caso contrário.
is_fraud: 1 se a transação é rotulada como qualquer tipo de fraude, 0 caso contrário.
tx_fraud_report_date: Data em que a fraude foi reportada (se aplicável).

## Premissas para o desenvolvimento do projeto

O dataset contem 6 meses de transações. Para o treinamento, iremos utilizar os 5 primeiros meses, ficando o sexto mês para a avaliação final do modelo.

Existirão três (3) padrões de fraudes distintas:

* Desacordo comercial: padrão praticamente impossível de prever, pois e resultado de um desacordo comercial entre comprador e vendedor; 
* Fraude Terminal: o terminal é corrompido e utilizado para phishing ou processamento de pagamentos com cartões roubados; 
* Fraude Cartão: credenciais de cartão vazadas e utilizadas para compras em distintos terminais. O cartão legítimo segue operando durante o período que os dados foram vazados.

Um quarto tipo de fraude seria a fraude de conluio, ou quadrilha, combinando terminais fraudulentos com cartões fraudados. 

Para fins didáticos, vamos assumir que os cartões são passíveis de clonagem. 

Na prática, após o advento do chip, a pratica de clonagem de cartão se tornou praticamente impossível.

Importante enfatizar que estes tipos de fraude não estarão diferenciados no target, as equipes poderão diferenciá-los através de uma análise exploratória.

Uma fase muito importante do projeto é a definição dos cortes do modelo. Esta definição requer uma otimização do(s) corte(s) visando a maximização do lucro final, buscando um equilíbrio entre aprovação de transações (minimizando falsos positivos) e fraudes.

Cada transação aprovada que não se torna uma fraude, o adquirente obtem 3% do valor total da transação. Quando uma transação aprovada se torna fraude, o adquirente assume o prejuízo de 100% do valor da transação.

Para o desenvolvimento deste projeto as equipes deverão entender o problema e o dataset disponibilizados pelo Mercado Livre e desenvolver um modelo para identificação de fraudes. Deverão entender como métricas de modelagem (precision, recall, f1-score, etc) se transladam em métricas de negócio (aprovação, fraude, lucro). Devem entender a necessidade e estratégias de otimização dos cortes do modelo visando otimizar resultados de negócio.

As equipes deverão compreender que trata-se de um cenário de negócio com alto desbalanceamento de classes e devem compreender as suas implicações em: feature selection, métricas de avaliação e estratégias de oversampling / undersampling.

Alguns atributos tem dado do tipo texto, ou seja, eventualmente as equipes deverão desenvolver técnicas de NLP para extração de features. Além disso, o dataset é composto por dados de transações, ou seja, os dados são temporais.

