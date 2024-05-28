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

## 3.1 Premissas Assumidas:
- Nos dados cada transação era única por tipo do produto, então assumi a premissa de que transações feitas no mesmo dia e mesmo horário e na mesma loja equivaliam a um mesmo pedido e agrupei para análises posteriores.
 
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
![image](https://github.com/TiagoTBarreto/analise_cafeteria/assets/137197787/f89d4ebc-822b-4291-90bd-5412c68454c2)

### H3. Quanto maior o número de itens comprados maior o faturamento.
**Aceita: O número de itens e o faturamento tem um comportamento quase intrínseco.** 
![image](https://github.com/TiagoTBarreto/analise_cafeteria/assets/137197787/1f7c1d6c-8367-4d00-957a-7c531b02c48b)

### H4. Quanto maior o basket size maior o faturamento.
**Rejeitada: O comportamento do Faturamento se mostra indiferente ao Basket Size das compras.**
![image](https://github.com/TiagoTBarreto/analise_cafeteria/assets/137197787/3e89f6ca-74ca-490b-8df9-98ba55d1259e)

### H5. A loja de Hell's Kitchen teve um crescimento de faturamento superior ao das outras lojas.
**Rejeitada: Todas tiveram um crescimento acumulado praticamente igual e um comportamento parecido ao longo dos 6 meses.**
![image](https://github.com/TiagoTBarreto/analise_cafeteria/assets/137197787/6d3c258c-c2d0-4527-9c1b-852ebd8e33af)

## 6.2 Resultado
- O faturamento da empresa é altamente relacionada com o número de pedidos realizados e itens comprados. 
- O faturamento das 3 diferentes lojas se comportaram de forma semelhante nesses 6 meses.
- O crescimento acumulado do Ticket Médio e Basket Size ao longo dos 6 meses foi praticamente nulo e não tiveram relação com o crescimento do faturamento da empresa.

# 7. Análise Preditiva
Para construir o modelo de Série Temporal, realizei os seguintes passos:

## 7.1 Encontrar a Sazonalidade + Erro
1. A granularidade utilizada foi por dia - DD/MM/YYYY (01/01/2023).
2. Utilizei uma média móvel centralizada com uma janela de 30 dias para suavizar a curva de faturamento.
3. Dividi o faturamento pela média móvel para encontrar a Sazonalidade com Erro embutido.
4. Depois realizei a média do Erro por dia do ciclo (30 dias).

## 7.2 Encontrar a Tendência
1. Desazonalizar o faturamento: Faturamento Real / Erro Embutido
2. Treinar uma Regressão Linear e encontrar a tendência.
![image](https://github.com/TiagoTBarreto/analise_cafeteria/assets/137197787/94951778-af77-4c43-95b5-05a89c427350)

## 7.3 Resultado Final
Previsão = Sazonalidade * Erro * Tendência
Previsão para o mês de Julho: R$ 189.053,81 
### 7.3.1 Erro do Modelo
- MAPE: 8.66%
- Então a previsão do faturamento vendas tem um erro embutido de 8.66% para mais ou menos. Então as vendas vão ser entre o intervalo de R$ 172.677,56 e R$ 205.430,06.

 


### 


 



