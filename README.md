# Ciência de Dados
<div align="center">
  <img src="https://drive.google.com/uc?export=view&id=1Wb9pCh6cjtt2v9GO8HBFeja6_uJtHW9m" width="300">
</div>


## Sobre este Projeto 
Os dados utilizados neste projeto são oficiais e foram obtidos no <a href='https://basedosdados.org/dataset/544c9d22-97b7-479a-8eca-94762840b465?table=e2d5dcc5-270e-4a8b-8d55-0227fd46c10f' target="_blank">Portal Base dos Dados</a>.



## Contextualização
Este projeto é constituído de quatro etapas:

#### <a href='https://github.com/Adenilson-silva/sicor/blob/main/A%20-%20Extract%2C%20Transform%2C%20Load%20-%20ETL.ipynb' target="_blank">1ª Etapa - ETL dos dados</a>
Nesta etapa do projeto, foi realizado o processo de ETL a partir dos dados armazenados no _Google BigQuery_, disponibilizados pelo Portal Base dos Dados. A seguir, detalham-se as etapas do processo:

- **_Extract_**: Extração dos dados diretamente da base no _Google BigQuery_.
- **_Transform_**: Neste procedimento, foram realizados a junção de tabelas, exclusão de colunas, conversão dos dados e a criação das colunas "Ano de Criação da Empresa" e "Categoria da Empresa". A classificação da categoria foi definida com base no tempo de existência da empresa, sendo: Nova, para empresas com menos de 5 anos; Em crescimento, para aquelas com 5 a 14 anos; Consolidada, para empresas com 15 a 29 anos; e Tradicional, para aquelas com 30 anos ou mais.
- **_Load_**: Os dados tratados foram salvos nos formatos <a href='https://www.databricks.com/br/glossary/what-is-parquet' target="_blank"> Parquet </a> e CSV para uso em análises futuras.


#### <a href='https://github.com/Adenilson-silva/sicor/blob/main/B%20-%20An%C3%A1lise%20dos%20Dados.ipynb' target="_blank">2ª Etapa - Análise dos Dados</a> 
A segunda etapa do projeto consistiu na análise dos dados, com o objetivo de atender aos seguintes pontos:

1 - Quantidade de operações de crédito por Finalidade

2 - Quantidade de operações de crédito por Atividade

3 - Quantidade de operações de crédito por Ano

4 - Quantidade de operações de crédito por Unidade Federativa

5 - Quantidade de operações de crédito por Categoria de Empresa

6 - Top 10 - Quantidade de operações de crédito por Modalidade (Geral)

7 - Top 10 - Quantidade de operações de crédito por Modalidade (Agrícola)

8 - Top 10 - Quantidade de operaçãoes de crédito por Modalidade (Pecuário)

9 - Top 10 - Quantidade de operações de crédito por Produto (Geral)

10 - Top 10 - Quantidade de operações de crédito por Produto (Agrícola)

11 - Top 10 - Quantidade de operaçãoes de crédito por Produto (Pecuário)

12 - Distribuição da Taxa de Juro


#### <a href='https://app.powerbi.com/view?r=eyJrIjoiZDlhYTliODgtMzY0NS00ZDUzLWI3YzQtMzRlZmM0MGU2YTY1IiwidCI6ImQ4YmRlNjVhLTNkZWQtNDM0Ni05NTE4LTY3MDIwNGU2ZTE4NCIsImMiOjR9' target="_blank">3ª Etapa - Visualização dos Dados</a>
Na terceira etapa do projeto, foi desenvolvido um painel para apresentar os dados referentes às operações de crédito, bem como a média, mínima e máxima taxas de juro. Para a elaboração dos painéis, utilizou-se a ferramenta _PowerBI_. O painel pode ser visualizado por este <a href='https://app.powerbi.com/view?r=eyJrIjoiZDlhYTliODgtMzY0NS00ZDUzLWI3YzQtMzRlZmM0MGU2YTY1IiwidCI6ImQ4YmRlNjVhLTNkZWQtNDM0Ni05NTE4LTY3MDIwNGU2ZTE4NCIsImMiOjR9' target="_blank">link</a>.

#### <a href='https://github.com/Adenilson-silva/sicor/blob/main/C%20-%20Cria%C3%A7%C3%A3o%20do%20r%C3%B3tulo%20priorizacao%20e%20aplica%C3%A7%C3%A3o%20da%20T%C3%A9cnica%20Upsampling%20para%20uso%20no%20Modelo%20Preditivo.ipynb' target="_blank">4ª Etapa - Criação da variável "priorizacao", Aplicação da Técnica de _Upsampling_</a> e <a href='https://github.com/Adenilson-silva/sicor/blob/main/D%20-%20Cria%C3%A7%C3%A3o%20de%20Modelos%20de%20Machine%20Learning.ipynb' target="_blank">Criação de Modelos de _Machine Learning_</a> 

Nesta etapa do projeto, foi realizada inicialmente a classificação de combinações de variáveis categóricas (atividade, finalidade, categoria da empresa, modalidade e produto) com base em suas frequências relativas no conjunto de dados. Assumindo independência entre as variáveis, estimou-se a probabilidade conjunta de cada combinação, atribuindo-se um nível de priorização para recebimento de crédito (“Alto” ou “Normal”), com base no percentil 90. Em seguida, aplicou-se a técnica de _Upsampling_ para equilibrar as classes de priorização. O objetivo dessa etapa foi gerar uma base classificada e balanceada para ser utilizada nos modelos preditivos.

A partir da base classificada foram aplicados 4 modelos de _Machine Learning_:
* Nayve Bayes (_CategoricalNB_)
* Árvore de Decisão (_DecisionTreeClassifier_)
* Floresta Aleatória (_RandomForestClassifier)
* Gradient Boosting (_XGBClassifier_)

Todos os modelos apresentaram bom desempenho. No entanto, considerando as métricas de avaliação, o tempo de treinamento e a aplicação da técnica de _Upsampling_ no conjunto de dados, o modelo de Árvore de Decisão se destacou, sendo considerado o mais adequado entre os modelos avalidados.


#### <a href='https://drive.google.com/file/d/1kdtnyRey4lzfT0XN3rWQCv1GQwSRFJT5/view?usp=sharing' target="_blank"> Arquivo com os dados brutos e tratados</a>.


## Tecnologias utilizadas
- Python
- Power BI

## Quem é o Autor?
Leia meu resumo e me envie uma mensagem: https://www.linkedin.com/in/adenilson-silva/

Vamos conversar...

