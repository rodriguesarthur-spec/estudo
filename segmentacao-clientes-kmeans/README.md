# Segmentação de clientes com K-means

Projeto de ciência de dados que aplica K-means para identificar perfis de clientes de um shopping center a partir de idade, renda anual e *spending score*.

> O conjunto de dados é pequeno e os resultados são exploratórios; não devem ser usados para inferir comportamento de clientes reais sem validação adicional.

## Pergunta de negócio

É possível identificar segmentos de clientes que ajudem a orientar estratégias de marketing e fidelização?

## Pipeline

1. Análise exploratória: distribuições, boxplots, dispersão e correlação.
2. Preparação: codificação de variáveis categóricas e padronização Z-score.
3. Seleção de `k`: método do cotovelo.
4. Agrupamento: treinamento do K-means com cinco clusters.
5. Visualização: gráficos 2D e 3D interativo.
6. Interpretação: perfis e recomendações de negócio por segmento.

## Fonte dos dados

O projeto usa o dataset [Mall Customer Segmentation Data](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python), disponibilizado no Kaggle.

Baixe o arquivo na fonte e salve-o como `archive/dados.csv`. O CSV não é versionado neste repositório para respeitar os termos de distribuição da fonte.

## Como executar

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook main.ipynb
```

## Estrutura

```text
.
├── archive/              # crie esta pasta e coloque dados.csv aqui
├── main.ipynb            # análise, agrupamento e visualizações
├── requirements.txt
└── README.md
```

## Tecnologias

Python · Pandas · NumPy · Matplotlib · Seaborn · Scikit-learn · Statsmodels · Plotly

## Licença

Este projeto é distribuído sob a [licença MIT](LICENSE).
