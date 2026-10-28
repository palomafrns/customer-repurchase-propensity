# Previsão de Recompra de Clientes

## Sobre o projeto

Este projeto tem como objetivo analisar o comportamento de compra dos clientes e desenvolver modelos de machine learning para prever quais clientes têm maior probabilidade de realizar uma nova compra.

A análise utiliza dados do **Online Retail II** e considera informações como recência, quantidade de notas fiscais, quantidade de produtos comprados e valor total gasto.

## Objetivos

- Explorar e entender os dados de vendas.
- Preparar os dados para a análise.
- Criar variáveis que representem o comportamento de compra dos clientes.
- Treinar e avaliar modelos de machine learning.
- Comparar os resultados e identificar oportunidades para ações de marketing.

## Estrutura do projeto

```text
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
│   ├── 01_exploratory_analysis.ipynb
│   ├── 02_features_and_target.ipynb
│   └── 03_modeling_and_evaluation.ipynb
├── reports/
│   └── model_results.csv
├── README.md
└── README_EN.md
```

## Etapas da análise

### 1. Análise exploratória

Análise inicial dos dados, identificação de padrões de compra e verificação da qualidade dos dados.

### 2. Preparação dos dados

Limpeza dos dados e criação de uma base por cliente, com informações sobre seu histórico de compras.

### 3. Criação das variáveis e do target

Foram utilizadas as seguintes variáveis:

- `recency_days`: dias desde a última compra.
- `invoice_count`: quantidade de notas fiscais.
- `total_quantity`: quantidade total de produtos comprados.
- `total_spend`: valor total gasto.

O target indica se o cliente realizou uma nova compra dentro da janela de tempo definida para a análise.

### 4. Modelagem

Foram comparados três métodos:

- Baseline baseado na quantidade de notas fiscais.
- Regressão Logística.
- Random Forest.

### 5. Avaliação

Os modelos foram avaliados usando ROC-AUC e PR-AUC.

| Modelo | ROC-AUC | PR-AUC |
|---|---:|---:|
| Baseline - Invoice Count | 0.713 | 0.758 |
| Logistic Regression | 0.729 | 0.793 |
| Random Forest | 0.715 | 0.791 |

A Regressão Logística apresentou os melhores resultados entre os modelos avaliados. No entanto, a diferença em relação ao baseline foi pequena em ROC-AUC, então os resultados devem ser interpretados com cautela.

## Como executar

1. Clone ou baixe este repositório.
2. Instale as bibliotecas necessárias para executar os notebooks.
3. Abra a pasta `notebooks`.
4. Execute os notebooks na seguinte ordem:

   1. `01_exploratory_analysis.ipynb`
   2. `02_features_and_target.ipynb`
   3. `03_modeling_and_evaluation.ipynb`

Confira os caminhos dos arquivos e a instalação das dependências antes de executar o projeto em outro ambiente.

## Limitações e próximos passos

- A análise utiliza dados de um único conjunto de dados de varejo.
- O desempenho dos modelos pode variar em outros períodos.
- A validação em novos períodos é importante para avaliar a capacidade de generalização.
- Os resultados não garantem que um cliente realizará uma nova compra.

## Fonte dos dados

Online Retail II — UCI Machine Learning Repository.

https://archive.ics.uci.edu/
