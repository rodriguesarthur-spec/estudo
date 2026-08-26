# Convergência estatística na precificação de opções

Projeto em Python que usa a precificação de uma opção de compra europeia sobre PETR4 como laboratório para demonstrar, por simulação, resultados fundamentais de probabilidade e finanças quantitativas.

O notebook compara o modelo binomial e a simulação de Monte Carlo com a fórmula de Black–Scholes.

## O que é investigado

| Módulo | Tema |
| --- | --- |
| 1 | Lei Fraca dos Grandes Números: erro do estimador Monte Carlo à medida que o número de simulações cresce |
| 2 | Lei Forte dos Grandes Números: convergência de médias acumuladas em trajetórias independentes |
| 3 | Teorema Central do Limite: distribuição do estimador e cobertura de intervalos de confiança |
| 4 | Convergência do modelo binomial para Black–Scholes |

## Dados e fontes

- Preços históricos de PETR4: [Yahoo Finance](https://finance.yahoo.com/quote/PETR4.SA/)
- Taxa livre de risco: série SGS 11 do [Banco Central do Brasil](https://www.bcb.gov.br/estabilidadefinanceira/historicocotacoes)

Os dados são consultados em tempo de execução; portanto, os valores e gráficos podem mudar conforme o mercado.

## Como executar

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook notebooks/convergencia_opcoes1.ipynb
```

## Tecnologias

Python · NumPy · Pandas · SciPy · Matplotlib · yfinance · API do Banco Central do Brasil

## Limitações

- O modelo considera uma opção europeia e pressupostos simplificadores de Black–Scholes.
- Resultados históricos não são recomendação de investimento.
- As demonstrações são didáticas: convergência observada em simulação não substitui uma prova matemática formal.

## Licença

Este projeto é distribuído sob a [licença MIT](LICENSE).
