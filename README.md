# Propensão à Recompra de Clientes

## Sobre o projeto

Projeto de Machine Learning para estimar a propensão de clientes a realizar uma nova compra, apoiando estratégias de retenção e priorização comercial.

## Dataset

Utiliza o dataset [Online Retail II](https://archive.ics.uci.edu/dataset/502/online+retail+ii), do UCI Machine Learning Repository, com dados de transações de um varejista online.

## Metodologia

- Análise e preparação dos dados.
- Engenharia de variáveis: recência, frequência, quantidade e gasto total.
- Definição do target com base em compras futuras.
- Treinamento e comparação de Regressão Logística e Random Forest.

## Resultados

A Regressão Logística apresentou o melhor resultado geral na avaliação inicial.

## Limitações

A avaliação utilizou uma divisão aleatória entre treino e teste. É necessária validação temporal para verificar o desempenho em períodos futuros. As previsões representam propensão à recompra, não impacto causal de campanhas.

## Tecnologias

Python, Pandas, NumPy, Matplotlib, Scikit-learn e Jupyter Notebook.

## Como executar

1. Instale as dependências com `pip install -r requirements.txt`.
2. Coloque o dataset em `data/raw/`.
3. Execute os notebooks em ordem, começando por `01_initial_analysis.ipynb`.


# Customer Repurchase Propensity

## Project Overview

Machine Learning project to estimate customers' propensity to make another purchase, supporting customer retention and commercial prioritization.

## Dataset

Uses the [Online Retail II](https://archive.ics.uci.edu/dataset/502/online+retail+ii) dataset from the UCI Machine Learning Repository, containing online retail transaction data.

## Methodology

- Data analysis and preparation.
- Feature engineering: recency, purchase frequency, quantity, and total spending.
- Target definition based on future purchases.
- Training and comparison of Logistic Regression and Random Forest.

## Results


Logistic Regression achieved the best overall results in the initial evaluation.

## Limitations

The evaluation used a random train-test split. Temporal validation is needed to assess performance on future periods. Predictions represent repurchase propensity, not the causal impact of marketing campaigns.

## Technologies

Python, Pandas, NumPy, Matplotlib, Scikit-learn, and Jupyter Notebook.

## How to Run

1. Install dependencies using `pip install -r requirements.txt`.
2. Place the dataset in `data/raw/`.
3. Run the notebooks in order, starting with `01_initial_analysis.ipynb`.