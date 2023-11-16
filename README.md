## Preço Combustíveis Brasil

### Etapas
* Objetivo/Pergunta
* Busca e importação dos dados
* Limpeza dos dados
* Tratamento e transformação dos dados
* Criação do relatório
* Links do código e do dashboard

#### Tenologias utilizadas:

* Power BI
* Pyspark
* SQL
* DataBricks
* Python


Imagem do Dashboard:
![Imagem Dashboard Preço combustíveis Brasil](https://github.com/matheus908/Pre-o-Combust-veis-Brasil/assets/60456455/b9797a51-8e18-4941-8036-a35f09f98036)

### Objetivo:
#### Criar um relatório que consiga acompanhar o preço médio de revenda dos 6 principais combustíveis utilizados no Brasil:
  * Gasolina
  * Gasolina Aditivada
  * Etanol
  * Diesel
  * Gás Natural
  * Gás de Cozinha

### Busca e importação dos dados:
Foi utilizado um conjunto de dados da Kaggle, que tem como fonte, informações do site da ANP (Agencia Nacional do Petróleo, Gás natural e Biocombustíveis) no período de julho de 2001 a janeiro de 2023.
Dados vieram no formato csv e foi feita a importação através do Databricks, como mostra a imagem abaixo:

![image](https://github.com/matheus908/Pre-o-Combust-veis-Brasil/assets/60456455/65430820-4b3a-47b9-93a9-79e0a429a7cd)

### Limpeza
A parte de limpeza foi feita através da análise do obejtivo dos dados e de qual seria a melhor forma de criar um dashboard interativo
Das tres tabelas acabamos escolhendo uma FatoCombustiveisBrasilEstado, por causa de ser base com mais informações
Foi realizado um filtro para excluir todas as linhas que não tinham uma data, com isso apenas trabalhando com dados que tenham uma data indentificada.

### Tratamento e transformação dos dados
Já que os dados vieram de um arquivo csv, foi feita a conversão dos tipos de dados de todas as colunas, para os tipos mais adequados
* Colunas de preço - tipo Decimal(5,2)
* Colunas de data - tipo Date
* Colunas de região e estado - tipo texto

![image](https://github.com/matheus908/Pre-o-Combust-veis-Brasil/assets/60456455/80fc1af5-d5b6-44f2-b1c6-e4170591def1)


Para uma melhor modelagem, segui a estrutura star schema (modelo estrela)
Então criei uma tabela dimensão de estado e criei uma coluna de Id, para ser a chave que liga as tabela Fato e a tabela dimensão criada.

![image](https://github.com/matheus908/Pre-o-Combust-veis-Brasil/assets/60456455/c267c8a6-925d-40a0-a4cd-726d98fe91f6)


### Criação do relatório

Tabelas Fato e dimensão criadas para serem importadas para o Power B.I

![image](https://github.com/matheus908/Pre-o-Combust-veis-Brasil/assets/60456455/e0c8f3b5-1fb1-423b-92b4-bcb0685de05c)

##### Layout de fundo inicial utilizado

![Fundo Power B I preço combustíveis](https://github.com/matheus908/Pre-o-Combust-veis-Brasil/assets/60456455/6845b7d2-66f2-400d-911d-4edfa6a2af5c)

##### Criação de dica de ferramenta para ver dados por estado no mapa

![image](https://github.com/matheus908/Pre-o-Combust-veis-Brasil/assets/60456455/c76d3ba8-d61f-48d6-a080-2352d6d59450)

##### Filtros de data e análise por combustível

![image](https://github.com/matheus908/Pre-o-Combust-veis-Brasil/assets/60456455/f64cba02-2448-48e0-8651-12ae3ccadcfe)

### Links do código e do dashboard

##### Código: 
https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/3820285923208374/695041861556603/7208511417105602/latest.html

##### Dashboard: 
https://app.powerbi.com/view?r=eyJrIjoiN2JkNWEzMTQtYmM5YS00MDExLWI0NDgtMjZlMTE0ZWIyOGI0IiwidCI6IjU4ZmMyZWZkLTk3MTUtNGQ2MC1hZDE1LTdiMWY0YjlhYjFmZSJ9&pageName=ReportSection










