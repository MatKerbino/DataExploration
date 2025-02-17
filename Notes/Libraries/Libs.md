- **Pandas**: Manipulação de dados.
  - **O que é:** Pandas é uma biblioteca de Python que fornece estruturas de dados e ferramentas de análise de dados de alta performance e fáceis de usar.
  - **Funcionalidades:** Inclui DataFrames e Series, que permitem manipulação e análise de dados de forma eficiente.
  - **Exemplo de uso:** Para criar um DataFrame, você pode usar:
    ```python
    import pandas as pd
    df = pd.DataFrame({'coluna1': [1, 2], 'coluna2': [3, 4]})
    ```

- **NumPy**: Operações numéricas.
  - **O que é:** NumPy é uma biblioteca fundamental para computação científica em Python, oferecendo suporte para arrays multidimensionais e funções matemáticas.
  - **Funcionalidades:** Permite operações eficientes em arrays e matrizes, além de funções matemáticas de alto nível.
  - **Exemplo de uso:** Para criar um array, você pode usar:
    ```python
    import numpy as np
    array = np.array([1, 2, 3])
    ```

- **Seaborn**: Visualizações estatísticas.
  - **O que é:** Seaborn é uma biblioteca de visualização de dados baseada no Matplotlib, que fornece uma interface de alto nível para desenhar gráficos estatísticos.
  - **Funcionalidades:** Facilita a criação de gráficos complexos com menos código e melhor estética.
  - **Exemplo de uso:** Para criar um gráfico de dispersão, você pode usar:
    ```python
    import seaborn as sns
    sns.scatterplot(x='coluna1', y='coluna2', data=df)
    ```

- **Matplotlib.pyplot**: Criação e customização de gráficos.
  - **O que é:** Matplotlib é uma biblioteca de plotagem em Python que fornece uma interface para criar gráficos de qualidade em 2D.
  - **Funcionalidades:** Permite a criação de uma ampla variedade de gráficos, desde simples até complexos.
  - **Exemplo de uso:** Para criar um gráfico de linha, você pode usar:
    ```python
    import matplotlib.pyplot as plt
    plt.plot([1, 2, 3], [4, 5, 6])
    plt.show()
    ```

- **Scikit-Learn**: Funções para divisão dos dados, métricas e modelos de regressão, pré-processamento, divisão do dataset e codificação.

- **XGBoost**: Modelagem com boosting.
  - **O que é:** XGBoost é uma biblioteca de aprendizado de máquina que implementa algoritmos de boosting de gradiente.
  - **Funcionalidades:** É conhecida por sua eficiência e desempenho em competições de ciência de dados.
  - **Exemplo de uso:** Para treinar um modelo, você pode usar:
    ```python
    import xgboost as xgb
    model = xgb.XGBClassifier()
    model.fit(X_train, y_train)
    ```

- **PyTorch (torch, torch.nn, torch.optim):** Para construção e treinamento da rede neural.
  - **O que é:** PyTorch é uma biblioteca de aprendizado profundo que fornece uma interface flexível e dinâmica para construir redes neurais.
  - **Funcionalidades:** Permite a criação de modelos complexos e a execução de cálculos em GPUs.
  - **Exemplo de uso:** Para criar um tensor, você pode usar:
    ```python
    import torch
    tensor = torch.tensor([1, 2, 3])
    ```

- **statistics**: A biblioteca `statistics` é uma biblioteca padrão do Python que fornece funções para realizar cálculos estatísticos básicos.
  - **O que é:** A biblioteca `statistics` oferece funções para calcular medidas estatísticas como média, mediana e moda.
  - **Funcionalidades:** É especialmente útil para análises de dados simples e para obter insights a partir de conjuntos de dados.
  - **Exemplo de uso:** Para calcular a média, você pode usar:
    ```python
    import statistics
    media = statistics.mean([1, 2, 3, 4, 5])
    ```

- **Sklearn**: Funções para divisão dos dados, métricas e modelos de regressão, pré-processamento, divisão do dataset e codificação.
  - **O que é:** Scikit-Learn é uma biblioteca de aprendizado de máquina em Python que fornece ferramentas simples e eficientes para análise preditiva e modelagem de dados.
  - **Funcionalidades:** A biblioteca inclui uma ampla gama de algoritmos de aprendizado supervisionado e não supervisionado, como regressão, classificação, agrupamento e redução de dimensionalidade. Além disso, oferece ferramentas para pré-processamento de dados, seleção de modelos e avaliação de desempenho.
  - **Exemplo de uso:** Para treinar um modelo de regressão linear, você pode usar:
    ```python
    from sklearn.linear_model import LinearRegression
    model = LinearRegression()
    model.fit(X_train, y_train)
    predictions = model.predict(X_test)
    ```

- **Scipy**: Biblioteca para computação científica.
  - **O que é:** Scipy é uma biblioteca de Python que fornece funções e algoritmos para matemática, ciência e engenharia, construindo sobre a biblioteca NumPy.
  - **Funcionalidades:** Inclui módulos para otimização, integração, interpolação, álgebra linear, estatísticas e muito mais.
  - **Exemplo de uso:** Para calcular a integral de uma função, você pode usar:
    ```python
    from scipy.integrate import quad
    result, error = quad(lambda x: x**2, 0, 1)  # Integra x^2 de 0 a 1.
    ```
    
  - **Exemplo de uso com distribuição normal:** Para trabalhar com distribuições normais, você pode usar:
    ```python
    from scipy.stats import norm
    distribution = norm(loc=0, scale=1)  # Cria uma distribuição normal padrão.
    ```

 