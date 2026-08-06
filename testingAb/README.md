# Segmentacao de Clientes com K-means

Projeto de Ciencia de Dados aplicando **clustering (K-means)** para segmentar clientes de um shopping center com base em idade, renda anual, spending score e genero.

**Pergunta de negocio:** E possivel identificar grupos distintos de clientes que ajudem a direcionar estrategias de marketing e fidelizacao?

## Dataset

[Mall Customer Segmentation Data](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python) (Kaggle) — 200 clientes, 5 variaveis.

O arquivo `dados.csv` esta na pasta `archive/`.

## Pipeline

1. **Analise exploratoria (EDA)** — distribuicoes, boxplots, grafico de dispersao, matriz de correlacao
2. **Preparacao dos dados** — codificacao de genero (`LabelEncoder`) e padronizacao Z-score (`StandardScaler`)
3. **Metodo do Cotovelo** — selecao do numero ideal de clusters (K=5) via analise de inercia
4. **Treinamento e rotulacao** — K-means com K=5 clusters
5. **Visualizacao** — scatter 2D (Renda x Score) e 3D interativo (Idade x Renda x Score)
6. **Interpretacao de negocios** — perfis e recomendacoes por segmento

## Perfis identificados

| Cluster | Perfil | Idade media | Renda media | Score medio |
|---|---|---|---|---|
| 0 | Cliente Maduro — Consumo Moderado | 56.5 | $46.1k | 39.3 |
| 1 | Renda Alta — Baixo Engajamento | 39.5 | $85.2k | 14.1 |
| 2 | Jovem — Alto Consumo | 28.7 | $60.9k | 70.2 |
| 3 | Renda Alta — Bom Consumidor | 37.9 | $82.1k | 54.4 |
| 4 | Jovem — Renda Baixa — Consumo Alto | 27.3 | $38.8k | 56.2 |

## Recomendacoes de negocio

- **Cluster 1** (renda alta + baixo consumo) representa uma oportunidade perdida — investigar por que nao estao gastando
- **Cluster 3** (renda alta + bom consumo) e o segmento mais valioso — programa de fidelizacao recomendado
- **Cluster 4** (jovens + renda baixa + consumo alto) sugere sensibilidade a preco — promocoes e parcelamento podem ser eficazes

## Limitacoes

- Dataset pequeno (200 clientes) e sintetico — resultados nao devem ser generalizados sem validacao com dados reais
- Variavel Genero nao e visualizada diretamente nos graficos 3D

## Estrutura

```
testingAb/
├── archive/
│   └── dados.csv
├── main.ipynb
└── requirements.txt
```

## Como executar

```bash
cd testingAb
pip install -r requirements.txt
jupyter notebook main.ipynb
```

## Tecnologias

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `Scikit-learn` · `Plotly`
