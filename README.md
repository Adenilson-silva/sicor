# Ciência de Dados
<div align="center">
  <img src="https://drive.google.com/uc?export=view&id=1Wb9pCh6cjtt2v9GO8HBFeja6_uJtHW9m" width="500">
</div>

https://drive.google.com/file/d/1kdtnyRey4lzfT0XN3rWQCv1GQwSRFJT5/view?usp=sharing
https://app.powerbi.com/view?r=eyJrIjoiZDlhYTliODgtMzY0NS00ZDUzLWI3YzQtMzRlZmM0MGU2YTY1IiwidCI6ImQ4YmRlNjVhLTNkZWQtNDM0Ni05NTE4LTY3MDIwNGU2ZTE4NCIsImMiOjR9

## Sobre este Projeto 
Os dados utilizados neste projeto são oficiais e foram obtidos no <a href='https://basedosdados.org/dataset/544c9d22-97b7-479a-8eca-94762840b465?table=e2d5dcc5-270e-4a8b-8d55-0227fd46c10f' target="_blank">Portal Base dos Dados</a>.



## Contextualização
Este projeto é constituído de três etapas:

#### 1ª Etapa - ETL dos dados
Nesta etapa do projeto, foi realizado o processo de ETL a partir dos dados armazenados no _Google BigQuery_, disponibilizados pelo Portal Base dos Dados. A seguir, detalham-se as etapas do processo:

- **_Extract_**: Extração dos dados diretamente da base no _Google BigQuery_.
- **_Transform_**: Tratamento de valores ausentes e indevidamente negativos. Para a imputação de dados ausentes, foi utilizado arquivo no formato _shapefile_ contendo os biomas brasileiros, disponibilizado pelo IBGE.
- **_Load_**: Os dados tratados foram salvos nos formatos <a href='https://www.databricks.com/br/glossary/what-is-parquet' target="_blank"> Parquet </a> e CSV para uso em análises futuras.


#### 2ª Etapa - Análise dos Dados 
A segunda etapa do projeto consistiu na análise dos dados, com o objetivo de atender aos seguintes pontos:

1 - Quantidade de queimadas por ano

2 - Quantidade de Registros de Queimadas por Bioma

3 - Quantidade de Registros de Queimadas por Unidade Federativa

4 - Quantidade de Registros de Queimadas por <a href='https://dataserver-coids.inpe.br/queimadas/queimadas/riscofogo_meteorologia/anuario_risco_de_fogo/anuario_risco_de_fogo_2023.pdf' target="_blank"> Classificação de Risco </a>


5 - Quantidade de Registros de Queimadas por Estação do Ano

6 - Quantidade de Registros de Queimadas por Mês

7 - Os 10 Municípios com maior quantidade de queimadas

8 - Os 10 Municípios com maior quantidade de queimadas críticas


#### 3ª Etapa - Visualização dos Dados
Na terceira etapa do projeto, foi desenvolvido um painel para apresentar os dados referentes às queimadas ocorridas no bioma com maior quantidade de focos. Para a elaboração dos painéis, utilizou-se a ferramenta _Tableau_.

## Tecnologias utilizadas
- Python
- Tableau

## Quem é o Autor?
Leia meu resumo e me envie uma mensagem: https://www.linkedin.com/in/adenilson-silva/

Vamos conversar...

