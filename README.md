# Projeto ML - Crédito para Financiamento de Imóveis

Projeto Final do Módulo de Machine Learning
______


## Contextualização

A PyCoders Ltda., cada vez mais especializada no mundo da Inteligência Artificial e Ciência de Dados, foi procurada por uma fintech para desenvolver um projeto de concessão de crédito para imóveis. Nesse projeto, espera-se a criação de valor que **discrimine ao máximo** os **bons pagadores** dos **maus pagadores**. 

Para isso, foi disponibilizada uma base de dados com milhares de casos de **empréstimos do passado** com diversas características dos clientes. 

Entrega: um modelo com a **melhor performance** possível.

Métrica de performance (inicialmente proposta): **ROC-AUC.**


## Base de Dados

Serão utilizadas bases de dados com **informações cadastrais, histórico de crédito e balanços financeiros de diversos clientes**. 

O conjunto de dados está dividido em **treino e teste**, todos no formato csv. 

Toda a modelagem, validação e avaliação deve ser feita em cima do conjunto de **treino**, subdividindo tal base como a squad achar melhor. 

Existe também os das variáveis explicativas, para ajudar no desenvolvimento do projeto. 

Serão necessários diversos cruzamentos e vocês estão livres para usar os dados da maneira que acharem mais conveniente.

[Clique aqui](https://drive.google.com/file/d/17fyteuN2MdGdbP5_Xq_sySN_yH91vTup/view) pra baixar os dados (eles estão disponiveis no arquivo zipado `credito-imoveis.zip`).

## Regras de Entrega

Deve ser entregue um arquivo csv com as **predições** para a base de teste.

Essa base deverá ser um Data Frame com duas colunas: a primeira sendo o **SK_ID_CURR** e a segunda a **probabilidade de inadimplência.**

### IMPORTANTE!

Entregar as predições com a **probabilidade da inadimplência ocorrer**, não a classe predita.

Além do arquivo com as predições, claro, entreugem também o notebook com o código utilizado. É importante que ele tenha:

- (i) a análise exploratória e construção das variáveis explicativas;

- (ii) a análise de modelagem, mostrando o processo das avaliações dos modelos e os motivos das decisões tomadas sobre qual modelo usar.

## Dicas


Explorar o conceito das variáveis: existe risco de imagem uma empresa utilizar variável de sexo para determinar risco de crédito? Vale a pena trazer a variável para o modelo?

Criar novas variáveis usando as variáveis que já estão na base: criatividade!

Qualquer dúvida, só me chamar! ;)


## Observações adicionais

- No arquivo zipado, há todas as bases que foram utilizadas na criação das bases principais (`application_{train|test_student}`). Vocês podem explorar à vontade estas outras bases pra entender como elas se comunicam entre si, e como as informações delas foram agregadas na base principal. No entanto, **não é necessário utilizar estas informações**, basta usar apenas o que tem na base de treino `application_train`. Este trabalho de cruzamento de diversas bases para a construção de uma única base de treinamento é muito importante, mas (embora já saibamos como cruzar bases!), é algo que foge do escopo deste módulo -- no módulo de banco de dados, vcs vão aprender tudo sobre isso! ;)

- Reflitam sobre isso: da forma que está, a base de teste `application_test_student` serve pra quê?

- Reforçando, pq nunca é demais: não esqueçam de fazer uma extensa análise exploratória! **Conheçam o problema com o qual vcs estão trabalhando!** Essa é a hora de botar em prática ao extremo tudo o que vimos no módulo 3 e 4! (e o que vimos no módulo 5 na etapa de modelagem, claro hehe)


## Alguns benchmarks

Pra ter uma ideia da performance máxima esperada do modelo, sugiro dar uma olhada nos [notebooks da competição](https://www.kaggle.com/c/home-credit-default-risk/code?competitionId=9120&sortBy=voteCount) (usem apenas como referência/inspiração! Peço que, na solução de vocês, realmente vcs apliquem as coisas como vimos no curso!!)

Em alguns notebooks, podemos ver que as AUC/ROCs máximas de validação encontradas foram de **0.76** e até mesmo **0.78** (usando modelos de gradient boosting e um pouco de feature engineering). Acredito que esse pode ser o alvo teto pra performance de vocês -- embora, como sempre dizemos: tentem chegar o mais próximo possível, no tempo que vocês têm disponível! Então, se não chegarem exatamente nessa performance, tudo bem! O importante é tentar chegar o mais próximo possível ;)
