# Prevenção de fraudes

## Objetivo

O objetivo deste projeto é desenvolver um modelo para identificação de fraudes em transações com cartão de crédito ou débito. 

## Dataset disponível

O dataset disponibilizado para o desenvolvimento deste modelo possui aproximadamente 5 milhões de transações. Tem-se poucos atributos prontos, o objetivo é que as equipes trabalhem com feature engineering a partir das características das transações. Como é um problema de fraude, é fácil perceber que se trata de um dataset altamente desbalanceado, aproximadamente 1% de fraudes. 

## Premissas para o desenvolvimento do projeto

O dataset conterá o conjunto de transações. As equipes deverão desenvolver um modelo que identifica fraudes em transações com o objetivo de melhorar o modelo financeiro da empresa parceira. 

Normalmente, quando o assunto é fraude, existem três (3) padrões de fraudes distintas:

* desacordo comercial: padrão praticamente impossível de prever, pois e resultado de um desacordo comercial entre comprador e vendedor; 
* fraude Terminal: o terminal é corrompido e utilizado para phishing ou processamento de pagamentos com cartões roubados; 
* fraude Cartão: credenciais de cartão vazadas e utilizadas para compras em distintos terminais. O cartão legítimo segue operando durante o período que os dados foram vazados.

Importante enfatizar que estes tipos de fraude não estarão diferenciados no target, as equipes poderão diferenciá-los através de uma análise exploratória.

Para o desenvolvimento deste projeto as equipes deverão entender o problema e o dataset disponibilizados pelo Mercado Livre e desenvolver um modelo para identificação de fraudes. Deverão entender como métricas de modelagem (precision, recall, f1-score, etc) se transladam em métricas de negócio (aprovação, fraude, lucro). Devem entender a necessidade e estratégias de otimização dos cortes do modelo visando otimizar resultados de negócio.

As equipes deverão compreender que trata-se de um cenário de negócio com alto desbalanceamento de classes e devem compreender as suas implicações em: feature selection, métricas de avaliação e estratégias de oversampling / undersampling.

Alguns atributos tem dado do tipo texto, ou seja, eventualmente as equipes deverão desenvolver técnicas de NLP para extração de features. Além disso, o dataset é composto por dados de transações, ou seja, os dados são temporais.

