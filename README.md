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
| product_category    | Categoria do produto (ex.: coffee, tea)                     |
| product_type        | Tipo de produto (ex.: hot chocolate, expresso)                               |
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
![image](https://github.com/TiagoTBarreto/analise_cafeteria/assets/137197787/ccb6ed6b-6431-4927-b63b-6c5c9db169ef)

- Todas categorias mantiveram sua participação constante ao longo dos meses.
![image](https://github.com/TiagoTBarreto/analise_cafeteria/assets/137197787/964373d4-864a-4e95-adbc-678393abeef0)


## 5.3 Produto
- Os 4 produtos que mais contribuem no faturamento são: Barista Expresso, Brewed Chai Tea, Hot Chocolate e Gourmet Brewed Coffee.
- Por outro lado, Green Beans, Green Tea e Organic Chocolate são os 3 produtos que menos contribuem.
![image](https://github.com/TiagoTBarreto/analise_cafeteria/assets/137197787/0a6d6f96-fd70-4b04-9a04-613dfff38724)

## 5.4 Loja
- As 3 lojas tem uma participação semelhante na receita da rede e manteram sua participação constante ao longo dos meses.
![image](https://github.com/TiagoTBarreto/analise_cafeteria/assets/137197787/784b14d4-12e9-4753-b94c-322fd235d43e)

## 5.5 Sazonalidade
- O faturamento aos finais de semana tem uma leve redução e os dias de semana tem uma contribuição semelhante.
![image](https://github.com/TiagoTBarreto/analise_cafeteria/assets/137197787/10d8360d-c0ae-4305-ad76-ec3d6489a17f)


- O maior volume ocorre entre as 7:00 às 11:00, depois das 11:00 até as 18:00 se mantém costante um volume médio, após as 19:00 começa a cair e depois das 20:00 tem pouquíssimos pedidos.
![image](https://github.com/TiagoTBarreto/analise_cafeteria/assets/137197787/24a24551-4d2a-4d8a-a17e-4d60b8038f98)


# 6. Análise Diagnóstica
## 6.1 Hipóteses

### H1. Quanto maior o número de pedidos maior o faturamento.
**Aceita: O número de pedidos e o faturamento tem um comportamento quase intrínseco.** 
![image](https://github.com/TiagoTBarreto/analise_cafeteria/assets/137197787/d34a66be-c294-473e-a23f-6a5bc73a070c)

### H2. Quanto menor o ticket médio das compras menor o faturamento.
**Rejeitada: O comportamento do Faturamento se mostra indiferente ao Ticket Médio das compras.**



