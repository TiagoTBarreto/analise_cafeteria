# Análise de Dados - Rede de Cafeterias
<p align="center">
  <img src="https://github.com/TiagoTBarreto/analise_cafeteria/assets/137197787/75e918bb-6d64-4599-b3fb-b85a28fbbd6f" width="100%" height="500">
</p>

# 1. Problema de Negócio

A Aroma Café é uma rede de cafeteria que está no mercado há dez anos, preenchendo uma lacuna no mercado local por cafeterias de alta qualidade. A loja no centro da cidade tem sido uma fonte de orgulho, com uma clientela fiel e uma equipe dedicada. No entanto, nos últimos meses, houve flutuações nas vendas e no fluxo de clientes, causando preocupação sobre possíveis desafios operacionais.

Para entender melhor a situação, o CEO Sr. Oliveira solicitou uma análise detalhada da operação das lojas para responder as seguintes perguntas:

1. Como está a saúde da rede de cafeterias, no geral?
2. Existe algum motivo do porque a rede está indo bem ou mal? 
3. Previsão de faturamento para os próximos 30 dias (Julho de 2023).
4. Recomendações para alavancar ainda mais o negócio.

# 2. Ferramentas Utilizadas

**Ferramentas para Análise de Dados**
- Excel
- Estatística Descritiva
- Análise de Regressão
- Previsão de Série Temporal

**Habilidades e Abordagem:**
- Pensamento Crítico e Resolução de Problemas: Habilidades fundamentais aplicadas para analisar, solucionar problemas e tomar decisões ao longo do projeto.

# 3. Descrição dos Dados 
| Campo            | Descrição                                                                 |
|---------------------|---------------------------------------------------------------------------|
| transaction_id      | Identificador único da transação                                          |
| transaction_date    | Data em que a transação foi realizada                                     |
| transaction_time    | Hora em que a transação foi realizada                                     |
| store_id            | Identificador único da loja onde a transação ocorreu                      |
| store_location      | Localização da loja onde a transação ocorreu                              |
| product_id          | Identificador único do produto                                            |
| transaction_qty     | Quantidade de itens comprados na transação                                |
| unit_price          | Preço unitário do produto                                                 |
| Total_Bill          | Valor total da conta da transação                                         |
| product_category    | Categoria do produto (ex.: Café, Chá,)                     |
| product_type        | Tipo de produto (ex.: Chocolate Quente, Expresso)                               |
| product_detail      | Detalhes específicos do produto (ex.: latte, cappuccino)                |
| size                | Tamanho do produto (ex.: pequeno, médio, grande)                          |

 
# 4. Descrição da solução
Para atender às demandas do CEO, foram realizadas quatro tipos distintas de análise: Descritiva, Diagnóstica, Preditiva e Prescritiva. Cada uma dessas etapas foi cuidadosamente planejada e executada utilizando o método SAPE (Situação, Análise, Plano e Execução). A seguir, descrevemos cada uma das análises realizadas:

## Método SAPE:
1. Saída: Definição clara do resultado desejado da análise.
2. Processo: Etapas específicas para coletar, processar e analisar os dados.
3. Entrada: Recursos necessários, como dados, habilidades da equipe e ferramentas.

O método SAPE garante uma abordagem organizada e eficiente para realizar análises, garantindo que as informações sejam obtidas e processadas de forma adequada para atender aos objetivos definidos.


# 5. Análise Descritiva
## 5.1 Ao longo do tempo 
- A tendência do faturamento é positiva. A empresa está crescendo.
![image](https://github.com/TiagoTBarreto/analise_cafeteria/assets/137197787/61562d69-c8c7-4083-ac1d-fe1c475e32ad)
![image](https://github.com/TiagoTBarreto/analise_cafeteria/assets/137197787/28aca5bd-6392-43aa-8942-8fe393911bad)

## 5.2 Categoria
- As 3 categorias (33%) que representam 78% do faturamento são: Coffee, Tea, Bakery e 5 categorias(55%) representam 94% do faturamento.
![image](https://github.com/TiagoTBarreto/analise_cafeteria/assets/137197787/964373d4-864a-4e95-adbc-678393abeef0)


- Todas categorias mantiveram sua participação constante ao longo dos meses.
![image](https://github.com/TiagoTBarreto/analise_cafeteria/assets/137197787/5ba94df4-feb7-4da1-8620-e3112f8bb5a0)


## 5.3 Produto
- Os 4 produtos que mais contribuem no faturamento são: Barista Expresso, Brewed Chai Tea, Hot Chocolate e Gourmet Brewed Coffee.
- Por outro lado, Green Beans, Green Tea e Organic Chocolate são os 3 produtos que menos contribuem.
![image](https://github.com/TiagoTBarreto/analise_cafeteria/assets/137197787/0a6d6f96-fd70-4b04-9a04-613dfff38724)

## 5.4 Loja
- As 3 lojas tem uma participação semelhante na receita da rede e manteram sua participação constante ao longo dos meses.
![image](https://github.com/TiagoTBarreto/analise_cafeteria/assets/137197787/784b14d4-12e9-4753-b94c-322fd235d43e)

## 5.5 Sazonalidade
- O faturamento aos finais de semana tem uma leve redução e os dias de semana tem uma contribuição semelhante.
![image](https://github.com/TiagoTBarreto/analise_cafeteria/assets/137197787/ebeb435b-6acc-455e-a19d-0f8e839ac5a8)

- O maior volume ocorre entre as 7:00 às 11:00, depois das 11:00 até as 18:00 se mantém costante um volume médio, após as 19:00 começa a cair e depois das 20:00 tem pouquíssimos pedidos.
![image](https://github.com/TiagoTBarreto/analise_cafeteria/assets/137197787/24a24551-4d2a-4d8a-a17e-4d60b8038f98)





## 5.1 PCA
![image](https://github.com/TiagoTBarreto/Insiders/assets/137197787/cd006cb1-fd38-4756-a483-a49aacf8009b)

## 5.2 t-SNE
![image](https://github.com/TiagoTBarreto/Insiders/assets/137197787/2f00501e-9e83-4091-bffc-3a6d0bd3be0d)

## 5.3 UMAP
![image](https://github.com/TiagoTBarreto/Insiders/assets/137197787/6341a3a4-43d6-40e5-ab67-525b62a2c6ea)

## 5.4 Tree-Based-Embedding
### 5.4.1 Feature Selection
Uma Random Forest composta por 250 árvores foi treinada e apenas as features que demonstraram mais de 1% de importância na separação das folhas foram selecionadas.
### 5.4.2 Treino
Posteriormente, o modelo foi novamente treinado utilizando a mesma Random Forest de 250 árvores, porém agora empregando apenas as features selecionadas. Em seguida, foi aplicado o comando "apply" para gerar 250 features adicionais, baseadas nas folhas das árvores.
### 5.4.3 Redução de Dimensionalidade
O algoritmo UMAP foi empregado para reduzir a dimensionalidade das 250 features obtidas anteriormente. Após testar diversos valores, a redução que resultou em uma melhor separação dos dados e um aumento na métrica foi de 250 para 10 dimensões. A imagem a seguir representa a combinação de duas dessas 10 dimensões.

![image](https://github.com/TiagoTBarreto/Insiders/assets/137197787/ff86467a-12d6-4d1a-be3d-3825716b93f7)
### 5.5 Escolha do Espaço
Nas imagens é possível observar claramente como o método Tree-Based-Embedding, combinando Random Forest + UMAP proporcionou uma organização mais eficiente dos dados em comparação com outras técnicas. Essa escolha foi respaldada pela clara separação e estruturação dos clusters, evidenciando a eficácia dessa abordagem na redução da dimensionalidade e na representação dos dados.

# 6. Machine Learning
- KMeans
- Hierarchical-Clustering
- Gaussian Mixture Model
- DBSCAN

## 6.1 Treinamento
**A métrica utilizada para comparação dos modelos foi a Silhouette Score.**

![image](https://github.com/TiagoTBarreto/Insiders/assets/137197787/d3b15b8e-13f8-42a6-a5e0-d0c1ad51ddae)

![image](https://github.com/TiagoTBarreto/Insiders/assets/137197787/af4769ba-2475-4261-80a1-7c19cf296811)

## 6.2 Escolha do Modelo
Apesar de o melhor valor de Silhouette ter sido obtido com 14 clusters, optei por selecionar o valor de **10 clusters**. Essa decisão foi tomada para facilitar a ação do time de negócio, reduzindo o número de grupos em 4, enquanto a métrica de Silhouette apresentou uma redução mínima.

Embora o DBSCAN tenha mostrado melhorias em alguns casos com 10 clusters, ele se revelou inconsistente durante os testes. Isso se deve, em parte, à complexidade dos ajustes necessários para seus parâmetros, como o epsilon e o número mínimo de pontos. Por outro lado, o H-Clustering é mais simples, exigindo apenas um parâmetro para ajuste, então optei por prosseguir com o **Hierarchical-Clustering**.

## 6.3 Análise do Modelo Final
### 6.3.1 Análise de Silhoueta
Podemos observar que, apesar de alguns clusters apresentarem um formato de "faca", indicando uma proximidade entre eles, a maioria dos clusters ainda obteve uma boa pontuação de silhueta. 

![image](https://github.com/TiagoTBarreto/Insiders/assets/137197787/1f6a53e7-edb1-4aa5-9f7d-18a11a67b9ae)

### 6.3.2 Espaço de Dados
Ao utilizar as mesmas dimensões selecionadas para comparação anterior do Espaço de Embedding, é possível observar uma excelente separação dos clusters.

![image](https://github.com/TiagoTBarreto/Insiders/assets/137197787/62b9522e-7357-43dc-9b26-9b4e94d0ff08)

# 7. Relatório
## 1- Quantos clientes farão parte do grupo?
O grupo Insiders será composto por 291 clientes, que correspondem a 9.81% do total.
## 2- Quais as principais características desses clientes?
### 2.1- Na média:
- Receita: $14,985
- Última Compra: 21 dias atrás
- Itens Comprados: 9,055
- Ordens de Retorno: 4
- Ticket Médio: $775
### 2.2- Na mediana:
- Receita: $6,924
- Última Compra: 9 dias atrás
- Itens Comprados: 4428
- Ordens de Retorno: 3
- Ticket Médio: $494.58
## 3- Qual a % de contribuição do faturamento, vinda do Insiders?
O Insiders representa 54.85% do faturamento total e 56.33% do volume de itens comprados na empresa.
## 4- Quais as condições para uma pessoa ser elegível ou remevida do Insiders?
Com a utilização do Espaço de Embedding, a explicabilidade do modelo é comprometida, tornando-se mais desafiador identificar as condições específicas para a elegibilidade ou não elegibilidade ao grupo Insiders. 
## 5- Qual a garantia que o programa Insiders é melhor que o restante da base?
### 5.1 Definição do tipo de Teste Estatístico
Após verificar a distribuição das variáveis utilizando o teste de Shapiro, constatei que nenhuma delas apresentava distribuição normal. Diante disso, optei por utilizar o teste de Mann-Whitney U para comparar o grupo de Insiders com o segundo melhor grupo, Top Consumers.
#### 5.1.2 Métrica Receita:
**Resultados do Teste de Mann-Whitney U:**

- Estatística Mann-Whitney U: 43987.0
- Valor p: 1.52e-39 (p < 0.05)
- Interpretação: O valor-p extremamente baixo indica evidências fortes para rejeitar a hipótese nula de que as duas amostras vêm da mesma distribuição, sugerindo que há diferenças estatisticamente significativas entre os grupos.
  
**Intervalos de Confiança:**
- Com 95% de confiança, a média de insiders está entre 11599.73 e 18370.56.
- Com 95% de confiança, a média de top consumers está entre 3693.69 e 4110.26.
  
#### 5.1.1 Métrica Ticket Médio:
**Resultados do Teste de Mann-Whitney U:**

- Estatística Mann-Whitney U: 31261.0
- Valor p: 3.81e-05 (p < 0.05)
- Interpretação: O valor-p extremamente baixo indica evidências fortes para rejeitar a hipótese nula de que as duas amostras vêm da mesma distribuição, sugerindo que há diferenças estatisticamente significativas entre os grupos.
  
**Intervalos de Confiança:**
- Com 95% de confiança, a média de insiders está entre 739.98 e 957.97.
- Com 95% de confiança, a média de top consumers está entre 493.68 e 621.43.

#### 5.1.3 Métrica Dias da Última Compra:
**Resultados do Teste de Mann-Whitney U:**

- Estatística Mann-Whitney U: 20638.0
- Valor p: 6.03e-04 (p < 0.05)
- Interpretação: O valor-p extremamente baixo indica evidências fortes para rejeitar a hipótese nula de que as duas amostras vêm da mesma distribuição, sugerindo que há diferenças estatisticamente significativas entre os grupos.
  
**Intervalos de Confiança:**
- Com 95% de confiança, a média de insiders está entre 16.70 e 25.56.
- Com 95% de confiança, a média de top consumers está entre 21.99 e 32.27.
  
  
## 6- Qual a perspectiva de faturamento do grupo?
### Após explorar várias abordagens para prever séries temporais, incluindo modelos como ARIMA, SARIMA e até mesmo técnicas de AutoML, enfrentei desafios significativos na redução do erro médio. Apesar disso, um modelo de rede neural de 7 camadas destacou-se como o mais promissor.

Com um conjunto de dados de um ano, onde reservei 11 meses para treinamento e validação e 1 mês para testes, os resultados foram os seguintes:

- Soma das previsões no 1º mês de teste: $460,855.1
- Soma dos valores reais no 1º mês de teste: $525,803.19
- Diferença percentual entre previsão e valor real: 12.35% menor que o valor real.

Enfrentei uma grande dificuldade em reduzir o erro médio individual, então optei por focar na minimização do erro total acumulado. Com isso, determinei um intervalo de faturamento para o próximo mês proveniente dos Insiders, levando em consideração o erro observado:

- Previsão de faturamento para o próximo mês: $521,493.0
- Intervalo: Entre $457,077.30 e $585,908.69.

# 8. O produto final do projeto
Montei uma infraestrutura utilizando serviços AWS:
![infra](https://github.com/TiagoTBarreto/Insiders/assets/137197787/eeb89d1c-9e56-4d65-a376-473f823e2f2f)
### 8.1 Armazenamento de Artefatos e Dados:
- O notebook salva os artefatos, como o modelo treinado, transformações no Amazon S3.
- Os conjuntos de dados também são armazenados no Amazon S3 para fácil acesso.

### 8.2 Controle de Versão e Colaboração:
- O código do projeto é mantido no GitHub, garantindo controle de versão, colaboração eficiente e rastreabilidade das alterações ao longo do tempo.

### 8.3 Processamento Automatizado na EC2:
- Uma instância EC2 é configurada para clonar o repositório do GitHub contendo o notebook.
- Um Cronjob scheduler é usado para automatizar a execução periódica do notebook na instância EC2.
### 8.4 Integração de Dados e Resultados:
- A instância EC2 lê os conjuntos de dados do Amazon S3 durante a execução do notebook.
- Os resultados finais, como métricas de desempenho do modelo ou resultados analíticos, são armazenados no Banco de Dados Postgres.
### 8.5 Papermill para Rastreabilidade:
- Utilizei o Papermill para executar o notebook de forma programática e guardar as execuções como registros.
- O Papermill gera uma cópia do notebook após cada execução, permitindo acompanhar as iterações e revisar os resultados anteriores conforme necessário.
### 8.6 Alimentação do Dashboard:
- O Banco de Dados Postgres sustenta um Dashboard, fornecendo informações atualizadas e insights em tempo real para os usuários.


