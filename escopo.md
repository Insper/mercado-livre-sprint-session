# Prevenção de fraudes

## Objetivo

O objetivo deste projeto é desenvolver um modelo para identificação de fraudes em transações com cartão de crédito ou débito presenciais. 

## Dataset disponível

O dataset disponibilizado para o desenvolvimento deste modelo possui aproximadamente 2 milhões de transações. Tem-se poucos atributos prontos, o objetivo é que as equipes trabalhem com feature engineering a partir das características das transações. Como é um problema de fraude, é fácil perceber que se trata de um dataset altamente desbalanceado, aproximadamente 1% de fraudes. 

## Premissas para o desenvolvimento do projeto

O dataset conterá o conjunto de transações com o resultado de um modelo existente (score e decisão). As equipes deverão desenvolver um novo modelo que melhore o resultado financeiro do modelo existente. 

Do total de transações, o modelo atual aprova 90% das transações. Para estas transações tem-se a classificação: 0 para não fraude e 1 para fraude. Para os 10% de transações rejeitadas pelo modelo atual, as equipes deverão desenvolver alguma estratégica de inferência de negados - o objetivo desta inferência é separar os true-positives dos false-positives. 

Existirão três (3) padrões de fraudes distintas:

* desacordo comercial: padrão praticamente impossível de prever, pois e resultado de um desacordo comercial entre comprador e vendedor; 
* fraude Terminal: o terminal é corrompido e utilizado para phishing ou processamento de pagamentos com cartões roubados; 
* fraude Cartão: credenciais de cartão vazadas e utilizadas para compras em distintos terminais. O cartão legítimo segue operando durante o período que os dados foram vazados.

Importante enfatizar que estes tipos de fraude não estarão diferenciados no target, as equipes poderão diferenciá-los através de uma análise exploratória.

Para o desenvolvimento deste projeto as equipes deverão entender o modelo atual (modelo baseline) e desenvolver um modelo melhor. Deverão entender como métricas de modelagem (precision, recall, f1-score, etc) se transladam em métricas de negócio (aprovação, fraude, lucro). Devem entender a necessidade e estratégias de otimização dos cortes do modelo visando otimizar resultados de negócio.

As equipes deverão compreender que trata-se de um cenário de negócio com alto desbalanceamento de classes e devem compreender as suas implicações em: feature selection, métricas de avaliação e estratégias de oversampling / undersampling.
