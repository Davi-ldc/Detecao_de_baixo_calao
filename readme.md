
---
## 1. Overview
Esse modelo tem como objetivo identificar palavrões ultilizando tecnicas de machine learning


## 2. Motivation
praticar

## 3. Success metrics
O modelo acertou 98 porcento das frases de teste (ultilizando 20 porcento do dataset com 14 mil frases)

## 4. Requirements & Constraints
re
sklearn
lightgbm
pandas
numpy 
string 
spacy
pickle


## 5. Methodology
Foi ultilizado a metodologia cientifica. Tentei achar um padrão em no dataset antes de decidir o que passar para o modelo. 
Tentei montar o melhor modelo com o menor custo computacional possivel. Por isso antes de usar tf-idf 14k de frases tentei cauntvectorinizer e menos dados porem
o modelo não foi capaz de identifcar certos padrões de palavras com duplo sentido. 



### 5.3. Techniques

Tf-idf
remover pontuação e stop words 
vies nos dados
### 5.4. Experimentation & Validation
para validar modelo ultilizei f1, recall, acc, macro avg entre outros.


### 5.5. Human-in-the-loop

Para maximizar a pontuação do modelo é importante adicionar erros do algoritimo ao seu dataset.

## 6. Implementation

### 6.1. High-level design

![](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2e/Data-flow-diagram-example.svg/1280px-Data-flow-diagram-example.svg.png)

### 6.2. Infra

O sistema roda em atravez de uma api feita com flask



### 6.4. Security

A api conta com varias camadas de segurança 

### 6.6. Monitoring & Alarms

O monitoramento do modelo é feito pela api 

### 6.7. Cost
Por ultilizar tecnicas de ML e proprocessamento simples o modelo tem um baixo custo computacional 

### 6.9. Risks & Uncertainties

Como o modelo foi treinado com dados de um regex ele não identifica palavras de duplo sentido. Nesse caso para evitar falsos positivos ele tende a prever "0"
Para se resolver isso basta ultilizar o feedback de usuarios


### 7.1. Alternatives

Deve-se considerar a ultilização de um regex, mas não pega duplo sentido

### 7.2. Experiment Results

Com base numa ineferencia com 50 frases e testes em 5 redações podemos dizer que é MUITO dificil dele errar





### 7.6. References
Felipe Da unica
