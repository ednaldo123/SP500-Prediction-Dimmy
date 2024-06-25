# Previsão de Séries Temporais do S&P 500
Previsor de Movimentação do Índice de Ações S&amp;P500 com diversos Modelos de Machine Learning

## Introdução
O S&P 500 é um índice do mercado de ações que mede o desempenho das ações de 500 grandes empresas listadas nas bolsas de valores dos Estados Unidos. É considerado uma das melhores representações do mercado de ações dos EUA.


## Pré-processamento dos Dados

Pré-processamos os dados para torná-los adequados ao modelo LSTM:

1. **Escalonamento:** Usamos MinMaxScaler de `sklearn.preprocessing` para escalonar os dados para o intervalo [0, 1].
2. **Redimensionamento:** Os dados são redimensionados para atender aos requisitos de entrada do LSTM, que é tipicamente (amostras, etapas de tempo, características).
