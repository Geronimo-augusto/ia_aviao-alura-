#  Projeto de Previsão de Atrasos de Voos com Python

Este projeto tem como objetivo prever atrasos de voos utilizando técnicas de aprendizado de máquina. A seguir, estão os detalhes sobre a preparação dos dados, construção de modelos, avaliação e salvamento do modelo final.

## Requisitos
- Python 3.6 ou superior
- Bibliotecas: `pandas`, `numpy`, `matplotlib`, `seaborn`, `pickle`, `sklearn`, `yellowbrick`

## Instalação
1- Clone o repositório.
2- Instale as bibliotecas necessárias:
```bash 
pip install pandas numpy matplotlib seaborn pickle-mixin scikit-learn yellowbrick
```

## Dados Utilizados
Os dados são provenientes de um arquivo CSV chamado `flights.csv`.

## Fluxo do Projeto
1- Carregamento e Análise Inicial dos Dados:

   - Carregar os dados utilizando `pandas`.
   - Análise exploratória dos dados com visualizações utilizando `seaborn` e `matplotlib`.

2- Preparação dos Dados:

   - Criação de novas colunas, como `date_time`,`is_weekend` e `day_name`.
   - Transformação de variáveis categóricas em variáveis dummy (one-hot encoding).
   - Separação dos dados em variáveis independentes (X) e dependentes (y).

3- Divisão dos Dados:

   - Divisão dos dados em conjuntos de treinamento e teste utilizando `train_test_split`.

4- Treinamento e Avaliação de Modelos:

   - Treinamento de um modelo baseline utilizando `DummyRegressor`.
   - Treinamento de um modelo `RandomForestRegressor`.
   - Avaliação dos modelos utilizando métricas como RMSE, MAE e R².
   - Visualização dos erros de predição e resíduos com `yellowbrick`.

5- Validação Cruzada:

   - Utilização de KFold para validação cruzada dos modelos.
   - Avaliação das métricas em cada divisão da validação cruzada.

6- Seleção de Features:

   - Identificação das features mais importantes utilizando `FeatureImportances` do `yellowbrick`.
   - Avaliação do desempenho do modelo com diferentes quantidades de features.

7- Otimização de Hiperparâmetros:

   - Utilização de `GridSearchCV` para encontrar os melhores hiperparâmetros para o modelo `RandomForestRegressor`.

8- Salvamento do Modelo:

   - Salvamento do modelo otimizado utilizando `pickle`.

## Execução
Para executar o projeto, siga as etapas descritas no fluxo do projeto. Certifique-se de que o arquivo `flights.csv` esteja no diretório correto.












https://iaaumentada.s3.us-east-2.amazonaws.com/base-dados/flights.csv