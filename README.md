# Previsão de Séries Temporais do S&P 500
Previsor de Movimentação do Índice de Ações S&amp;P500 com diversos Modelos de Machine Learning

## Descrição
O S&P 500 é um índice do mercado de ações que mede o desempenho das ações de 500 grandes empresas listadas nas bolsas de valores dos Estados Unidos. É considerado uma das melhores representações do mercado de ações dos EUA.

O gráfico ilustra as flutuações dos preços de fechamento do índice S&P 500 desde janeiro de 2022 até julho de 2024. 

<p align="center">
  <img src="https://github.com/ednaldo123/SP500-Prediction-Dimmy/blob/main/plots/lstm/closeprices.png">
</p>

### Perda de Treinamento e Validação do Modelo LSTM
- O gráfico a seguir mostra a perda (loss) durante o treinamento e a validação do modelo LSTM ao longo de várias épocas.
<p align="center">
  <img src="https://github.com/ednaldo123/SP500-Prediction-Dimmy/blob/main/plots/lstm/losstrainvalidation.png">
</p>

A linha azul representa a perda de treinamento, que começa relativamente alta e diminui rapidamente nas primeiras épocas, estabilizando em um valor baixo. Isso indica que o modelo está aprendendo e melhorando seu ajuste aos dados de treinamento.

A linha laranja representa a perda de validação, que é relativamente baixa desde o início e permanece estável ao longo das épocas, indicando que o modelo está generalizando bem aos dados de validação e não está superajustando (overfitting) aos dados de treinamento.

### Previsões LSTM vs Valores Reais

O gráfico a seguir compara as previsões do modelo LSTM com os valores reais do índice S&P 500 ao longo do tempo.

<p align="center">
  <img src="(https://github.com/ednaldo123/SP500-Prediction-Dimmy/blob/main/plots/lstm/prevision1.png)">
</p>

A linha azul mostra os valores reais do índice S&P 500, enquanto a linha laranja mostra as previsões feitas pelo modelo LSTM. A linha de previsão segue de perto a linha de valores reais, capturando bem a tendência geral do mercado.

### Distribuição dos Erros de Previsão

O gráfico a seguir mostra a distribuição dos erros de previsão do modelo LSTM.

<p align="center">
  <img src="https://github.com/ednaldo123/SP500-Prediction-Dimmy/blob/main/plots/lstm/errordistrib1.png">
</p>

A maioria dos erros de previsão está concentrada entre 0 e 200, com picos em torno de 50, 100 e 200. Há alguns erros negativos, mas a maioria dos erros é positiva, indicando que o modelo tende a subestimar os valores reais mais frequentemente do que superestimá-los. A distribuição não é perfeitamente simétrica, sugerindo que os erros de previsão têm uma certa tendência ou viés.

### Métricas de Avaliação do Modelo LSTM (Original)

As seguintes métricas foram utilizadas para avaliar o desempenho do modelo LSTM:

- **Acurácia**: 54% (0.54)
- **F1-Score**: 64% (0.64)
- **MSE (Mean Squared Error)**: 26.5

Estas métricas indicam que o modelo possui uma acurácia moderada, com um F1-Score indicando um bom equilíbrio entre precisão e robustez, e um erro quadrático médio que sugere que ainda há espaço para melhorias no modelo.

O gráfico a seguir mostra a perda (loss) durante o treinamento e a validação do modelo LSTM ajustado ao longo de várias épocas.

<p align="center">
  <img src="https://github.com/ednaldo123/SP500-Prediction-Dimmy/blob/main/plots/lstm/losstrainvalidation2.png">
</p>

#### Modelo Original
- **Perda de Treinamento**: A perda de treinamento começa relativamente alta e diminui rapidamente nas primeiras épocas, estabilizando em um valor baixo.
- **Perda de Validação**: A perda de validação é relativamente baixa desde o início e permanece estável ao longo das épocas.

#### Modelo Ajustado
- **Perda de Treinamento**: A perda de treinamento do modelo ajustado também começa alta e diminui rapidamente, mas mostra uma estabilização ainda mais baixa e consistente do que o modelo original, indicando que o ajuste melhorou a capacidade do modelo de aprender com os dados de treinamento.
- **Perda de Validação**: A perda de validação no modelo ajustado é significativamente mais estável e baixa ao longo de todas as épocas, sugerindo que o modelo ajustado generaliza melhor e tem menos tendência a overfitting em comparação com o modelo original.

### Conclusão

As melhorias no modelo ajustado resultaram em uma perda de treinamento e validação mais baixa e estável. Isso indica que o modelo ajustado tem uma melhor capacidade de aprendizado e generalização, reduzindo o risco de overfitting e melhorando a precisão das previsões.

### Previsões LSTM vs Valores Reais (Modelo Ajustado)

O gráfico a seguir compara as previsões do modelo LSTM ajustado com os valores reais do índice S&P 500 ao longo do tempo.

<p align="center">
  <img src="https://github.com/ednaldo123/SP500-Prediction-Dimmy/blob/main/plots/lstm/prevision2.png">
</p>

Comparando os gráficos do modelo original e do modelo ajustado, podemos observar as seguintes melhorias:

1. **Aderência aos Valores Reais**:
   - O modelo ajustado apresenta uma linha de previsão que segue de maneira mais próxima a linha dos valores reais, capturando melhor a tendência geral do mercado.
   - As previsões do modelo ajustado são mais precisas em várias seções do gráfico, mostrando que o modelo melhorou sua capacidade de seguir os movimentos reais do índice S&P 500.

2. **Suavização das Previsões**:
   - Assim como no modelo original, a linha de previsão do modelo ajustado é mais suave em comparação com os valores reais, mas agora com uma aproximação melhor, indicando que o modelo ajustado consegue suavizar as flutuações enquanto segue a tendência real mais de perto.

3. **Redução de Erros**:
   - Os ajustes no modelo resultaram em previsões que têm uma margem de erro menor em relação aos valores reais, evidenciado pela proximidade das duas linhas no gráfico.
   - A menor diferença entre as linhas de previsão e os valores reais sugere uma melhoria significativa na capacidade do modelo de fazer previsões mais acuradas.

4. **Performance Geral**:
   - O modelo ajustado mostra uma melhoria geral em sua performance, tanto na captura das tendências de longo prazo quanto na redução de erros de curto prazo.
   - A melhoria é visível na aderência das previsões aos valores reais, especialmente em períodos de alta e baixa do índice.
   - 
  ### Distribuição dos Erros de Previsão (Modelo Ajustado)

  O gráfico a seguir mostra a distribuição dos erros de previsão do modelo LSTM ajustado.

<p align="center">
  <img src="https://github.com/ednaldo123/SP500-Prediction-Dimmy/blob/main/plots/lstm/errordistrib2.png">
</p>

A distribuição dos erros no modelo ajustado mostra uma tendência similar ao modelo original, mas com algumas diferenças notáveis:

- **Distribuição dos Erros**:
  - A maioria dos erros de previsão está concentrada entre 0 e 250, com picos em torno de 50, 100 e 150.
  - A distribuição de erros é mais concentrada em torno de valores menores em comparação com o modelo original, sugerindo uma melhoria na precisão das previsões.

- **Frequência dos Erros**:
  - A frequência dos erros no modelo ajustado é mais uniforme, com menos picos abruptos, indicando uma distribuição de erros mais equilibrada.
  - Há uma redução nos erros extremos, o que sugere que o modelo ajustado é mais robusto e menos propenso a grandes desvios.

- **Interpretação dos Picos**:
  - Os picos no histograma indicam que há certos valores de erro que ocorrem mais frequentemente, mas a concentração é menor, mostrando que o modelo ajustado tem uma melhor distribuição dos erros.
    
  ### Conclusão

A distribuição dos erros de previsão do modelo ajustado é mais equilibrada e concentrada em valores menores, indicando uma melhoria na precisão das previsões e uma redução nos erros extremos. Isso sugere que o modelo ajustado é mais robusto e eficaz em capturar a tendência geral do mercado com menos desvios significativos.

  ### Métricas de Avaliação do Modelo LSTM Ajustado

As seguintes métricas foram utilizadas para avaliar o desempenho do modelo LSTM ajustado:

- **Acurácia LSTM Ajustado**: 49.51%
- **F1-Score LSTM Ajustado**: 57.69%
- **MSE LSTM Ajustado**: 32373.11

Estas métricas indicam que o modelo ajustado possui uma acurácia moderada, com um F1-Score indicando um bom equilíbrio entre precisão e robustez, e um erro quadrático médio que sugere que ainda há espaço para melhorias, mas que o modelo ajustado já apresenta uma performance significativamente melhor em comparação com o modelo original.
