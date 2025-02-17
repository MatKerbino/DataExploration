import sklearn.model_selection import train_test_split

### train_test_split
- **O que faz:** A função `train_test_split` é utilizada para dividir um conjunto de dados em dois subconjuntos: um para treinamento e outro para teste. Isso é fundamental para avaliar o desempenho de um modelo de aprendizado de máquina.
- **Detalhes:** 
  - **Parâmetros:** A função aceita vários parâmetros, incluindo:
    - `X`: As características (features) do conjunto de dados.
    - `y`: Os rótulos (labels) correspondentes.
    - `test_size`: A proporção do conjunto de dados a ser usada para teste (por exemplo, 0.2 para 20%).
    - `random_state`: Um número inteiro que garante a reprodutibilidade da divisão.
    - `shuffle`: Um booleano que indica se os dados devem ser embaralhados antes da divisão.
  - **Retorno:** A função retorna quatro conjuntos: `X_train`, `X_test`, `y_train`, `y_test`, que podem ser usados para treinar e testar o modelo.
- **Exemplo de uso:** Para dividir um conjunto de dados em 80% para treinamento e 20% para teste, você pode usar:
  ```python
  from sklearn.model_selection import train_test_split
  X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
  ```

