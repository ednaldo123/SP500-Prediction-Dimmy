# Previsão do Índice S&P 500 Utilizando Modelos de LSTM e Random Forest

## Resumo
A previsão da tendência do mercado de ações pode trazer benefícios significativos, como o aumento da riqueza e a prevenção de perdas financeiras. Este estudo compara dois algoritmos de aprendizado de máquina, LSTM (Long Short-Term Memory) e Random Forest, na previsão do índice S&P 500. Utilizando dados históricos do S&P 500, analisamos a data e o valor de fechamento para prever futuras tendências de preços. Os resultados mostraram que o modelo LSTM teve um desempenho superior ao do Random Forest.

## Introdução
Prever a tendência do mercado de ações pode trazer benefícios significativos para as pessoas, permitindo-lhes potencialmente aumentar sua riqueza ou evitar perdas substanciais. Atualmente, o aprendizado de máquina tornou-se um dos tópicos mais quentes globalmente, com um número crescente de estudos utilizando modelos de aprendizado de máquina para investigação. Este estudo compara o desempenho na previsão entre dois algoritmos de aprendizado de máquina proeminentes: LSTM e Random Forest.

## Metodologia

### LSTM
As redes LSTM são projetadas para capturar dependências de longo prazo em dados sequenciais. Utilizamos a biblioteca TensorFlow e a interface Keras para construir e treinar a rede neural LSTM. A rede foi configurada para usar sequências de 60 dias para prever o valor de fechamento do dia seguinte. 

#### Ferramentas Utilizadas:
- NumPy
- Pandas
- MinMaxScaler
- Matplotlib
- TensorFlow (Keras)
- Sequential, LSTM, Dense, Dropout

#### Treinamento e Construção:
- Dados divididos em 80% para treino e 20% para teste
- Sequências de 60 dias utilizadas como entrada no modelo
- Dropout de 20% para evitar overfitting
- Funções de ativação: Sigmoid e Tanh
- Batch size: 32
- Épocas: 50
- Otimizador: Adam

### Random Forest
O modelo Random Forest combina múltiplas árvores de decisão para melhorar a precisão preditiva. Utilizamos a biblioteca Scikit-learn para construir e treinar o modelo Random Forest.

#### Ferramentas Utilizadas:
- Pandas
- NumPy
- Scikit-learn (train_test_split, RandomizedSearchCV, RandomForestRegressor)
- SciPy (randint)
- Matplotlib

#### Treinamento e Construção:
- Dados divididos em 80% para treino e 20% para teste
- Random Search para otimização de hiperparâmetros
- Hiperparâmetros otimizados: max_depth, max_features, n_estimators, min_samples_leaf, min_samples_split

## Resultados
Os treinos foram realizados em um Apple Macbook Pro, Chip M2, 8gb Ram, 256gb Ssd, 2022.

### LSTM
- MAE: 37.18
- MSE: 2278.24
- RMSE: 47.73
- R²: 0.83

### Random Forest
- MAE: 48.48
- MSE: 3819.25
- RMSE: 61.80
- R²: 0.98

### Gráficos
#### LSTM
- Gráfico de Previsões: Plota as previsões do modelo contra os valores reais
  <p align="center">
  <img src="https://github.com/ednaldo123/SP500-Prediction-Dimmy/blob/main/plots/lstm/plotlstm2.png">
  </p>

- Gráfico de Perda: Plota a perda do treinamento e da validação ao longo das épocas
  <p align="center">
  <img src="https://github.com/ednaldo123/SP500-Prediction-Dimmy/blob/main/plots/lstm/plotlstm.png">
  </p>

#### Random Forest
- Gráfico de Previsões vs Valores Reais: Plota as previsões do modelo contra os valores reais
  <p align="center">
  <img src="https://github.com/ednaldo123/SP500-Prediction-Dimmy/blob/main/plots/RandomForest/plotrandomforest2.png">
  </p>

- Gráfico de Loss: Plota o MSE em função do número de árvores
  <p align="center">
  <img src="https://github.com/ednaldo123/SP500-Prediction-Dimmy/blob/main/plots/RandomForest/plotrandomforest1.png">
  </p>

## Instruções de Uso

### Requisitos
- Python 3.8+
- Bibliotecas: NumPy, Pandas, TensorFlow, Scikit-learn, Matplotlib, SciPy

### Instalação
Clone o repositório e instale as dependências:

```bash
git clone https://github.com/ednaldo123/SP500-Prediction-Dimmy.git
cd SP500-Prediction-Dimmy
pip install -r requirements.txt
