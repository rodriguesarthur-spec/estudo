# Convergencia Estatistica Aplicada a Precificacao de Opcoes

Projeto que usa a precificacao de uma **opcao de compra europeia** (acao PETR4) como laboratorio pratico para demonstrar empiricamente tres teoremas fundamentais da probabilidade, combinando o **modelo binomial** com **simulacao de Monte Carlo**.

## Dados reais utilizados

- **Preco e volatilidade** da PETR4 — historico de 2 anos via Yahoo Finance
- **Taxa livre de risco (Selic)** — via API do Banco Central do Brasil (serie SGS 11)

## Modulos

| Modulo | Conteudo |
|---|---|
| 0 | Coleta de dados de mercado, calculo de parametros ($u$, $d$, $p$) e funcoes base |
| 1 | **Lei Fraca dos Grandes Numeros (LFGN)** — convergencia em probabilidade do estimador Monte Carlo |
| 2 | **Lei Forte dos Grandes Numeros** — convergencia quase certa via media acumulada de multiplas trajetorias |
| 3 | **Teorema Central do Limite (TLC)** — Teorema de De Moivre-Laplace, normalidade do estimador e validacao de intervalos de confianca |
| 4 | **Convergencia Binomial para Black-Scholes** — o modelo discreto reproduz o continuo no limite |

## Principais resultados

- A probabilidade de erro do estimador Monte Carlo decai com N, tendendo a zero — confirmando a LFGN
- Multiplas trajetorias independentes convergem suavemente para o preco teorico C (Lei Forte)
- A distribuicao das estimativas se aproxima da Normal mesmo com payoffs nao-normais (TLC)
- Intervalos de confianca de 95% capturam o valor real com cobertura empirica proxima de 95%
- O preco do modelo binomial converge para a formula de Black-Scholes conforme o numero de passos cresce

## Estrutura

```
projeto-convergencia-opcoes/
├── notebooks/
│   └── convergencia_opcoes1.ipynb
└── requirements.txt
```

## Como executar

```bash
cd projeto-convergencia-opcoes
pip install -r requirements.txt
jupyter notebook notebooks/convergencia_opcoes1.ipynb
```

## Tecnologias

`Python` · `NumPy` · `SciPy` · `Matplotlib` · `Pandas` · `yfinance` · `API BCB`
