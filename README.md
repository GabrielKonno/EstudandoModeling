# Comparação de Modelos de Regressão e Otimização com GridSearchCV

Este projeto aplica técnicas de machine learning para resolver um problema de regressão utilizando diferentes modelos e otimização de hiperparâmetros. As etapas incluem o treinamento, avaliação e otimização de modelos de regressão para prever preços de casas com base em características do dataset.

---

## Estrutura do Projeto

### 1. Dataset
- O dataset contém características relacionadas a preços de casas, como:
  - Renda mediana (MedInc)
  - Idade média das casas (HouseAge)
  - Número médio de quartos e ocupantes (AveRooms, AveOccup)
  - Localização geográfica (Latitude e Longitude)
- Os dados são divididos em 80% para treinamento e 20% para teste.

---

### 2. Modelos Treinados
1. **Regressão Linear (LinearRegression)**
   - Simples e eficiente para problemas lineares.
   - Avaliado com MSE e RMSE:
     - MSE: `0.5559`
     - RMSE: `0.7456`

2. **Support Vector Regressor (SVR)**
   - Adequado para problemas não-lineares.
   - Avaliado com MSE e RMSE:
     - MSE: `1.3320`
     - RMSE: `1.1541`

3. **XGBoost Regressor**
   - Modelo baseado em árvores de decisão, eficiente para grandes volumes de dados.
   - Avaliado com MSE e RMSE:
     - MSE: `0.2226`
     - RMSE: `0.4718`

---

### 3. Otimização de Hiperparâmetros
- Foi utilizada a técnica **GridSearchCV** para encontrar os melhores parâmetros para o modelo XGBoost.
- Hiperparâmetros otimizados:
  - `max_depth`: 7
  - `learning_rate`: 0.2
  - `gamma`: 0
  - `subsample`: 1
- Resultado após otimização:
  - MSE: `0.2164`
  - RMSE: `0.4652`

---

## Comparação de Resultados

| Modelo                  | MSE    | RMSE   |
|-------------------------|--------|--------|
| Regressão Linear        | 0.5559 | 0.7456 |
| SVR                    | 1.3320 | 1.1541 |
| XGBoost (padrão)       | 0.2226 | 0.4718 |
| XGBoost (otimizado)    | 0.2164 | 0.4652 |

### Conclusão:
- O **XGBoost com hiperparâmetros otimizados** apresentou o melhor desempenho, com o menor erro médio e maior precisão.

---

## Tecnologias Utilizadas
- Linguagem: **Python**
- Bibliotecas:
  - `scikit-learn` para modelos e métricas.
  - `xgboost` para regressão baseada em árvores de decisão.
  - `GridSearchCV` para otimização de hiperparâmetros.

---

## Como Executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
   ```
2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```
3. Execute o notebook no Jupyter ou Google Colab para reproduzir os resultados.
