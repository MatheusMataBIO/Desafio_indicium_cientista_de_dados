# 🎬 Predição de Notas de Filmes (IMDB Rating)

Este projeto tem como objetivo prever as notas de filmes no IMDB a partir de informações como ano de lançamento, certificado, duração, gênero, diretores, estrelas, votos e bilheteria.  
O pipeline foi desenvolvido em **Python** dentro do **Databricks**, utilizando técnicas de Machine Learning com **RandomForest**, **XGBoost**.

---

## 🚀 Tecnologias utilizadas
- **Python 3.12** (Databricks Runtime)
- [scikit-learn](https://scikit-learn.org/stable/)
- [Randomforest](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html)
- [XGBoost](https://xgboost.readthedocs.io/)

## 📂 Estrutura do projeto

- `filmes_tratado.csv` : Dataset tratado com informações dos filmes.  
- `Ingestão_dados_ETL.ipynb` : Notebook responsável pela leitura e preparação dos dados.  
- `EDA.ipynb` : Notebook para análise exploratória dos dados.  
- `Construção e treinamento dos modelos.ipynb` : Notebook para treino e avaliação dos modelos de machine learning.  
- `modelo_randomforest.pkl` : Modelo Random Forest treinado e salvo para uso em predições.
- 
## Pré-requisitos

- Conta no [Databricks Free Edition](https://databricks.com/try-databricks)  
- Dependências Python instaladas no Workspace:
  

## Instalar as dependências 
  - No ambiente do Databricks, vá em **Compute > Libraries > Install New > PyPI** e instale as dependências do arquivo requeriments.txt
 
## Como Executar

Faça upload do projeto inteiro no Databricks Workspace.

Abra o notebook Ingestão_dados_ETL.ipynb e execute as células para carregar e tratar os dados.

Abra o notebook EDA.ipynb e execute as células para realizar a análise exploratória, verificar estatísticas e entender o comportamento dos dados.

Abra o notebook Construção e treinamento dos modelos.ipynb:

Crie as colunas derivadas (primary_genre, log_No_of_Votes, log_Gross) conforme o notebook.

Treine os modelos de machine learning (Random Forest, XGBoost, etc.).

Avalie os modelos com métricas de desempenho (MAE, RMSE, R²).

Salve o modelo treinado como modelo_randomforest.pkl.

O modelo salvo pode ser carregado posteriormente para fazer previsões em novos dados usando:

**import joblib**

**modelo = joblib.load("modelo_randomforest.pkl")**
**predicoes = modelo.predict(novos_dados)**

