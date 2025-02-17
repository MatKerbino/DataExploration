# import pandas as pd

### pandas.read_csv("X.csv")
  Utilizado para carregar os dados.


## .loc[]
- **O que faz:** O método é utilizado para acessar um grupo de linhas e colunas por rótulos ou uma matriz booleana. Ele permite selecionar dados de forma mais intuitiva e legível.
- **Detalhes:** Você pode usar `.loc[]` para filtrar dados com base em condições específicas, como selecionar todas as linhas onde uma coluna atende a um critério.
- **Exemplo Analógico:** Pense em uma biblioteca onde você pode procurar livros por título ou autor, permitindo que você encontre rapidamente o que precisa.
- **Parâmetros:** 
  - `label`: O rótulo da linha ou coluna que você deseja acessar.
- **Retorno:** Retorna um DataFrame ou uma Série com os dados selecionados.
- **Exemplo de uso:**
  ```python
  import pandas as pd
  df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})
  result = df.loc[df['A'] > 1]  # Seleciona linhas onde a coluna 'A' é maior que 1.
  ```

## .iloc[]
- **O que faz:** O método é utilizado para acessar um grupo de linhas e colunas por índices inteiros. Ele permite selecionar dados de forma baseada na posição, ao invés de rótulos.
- **Detalhes:** Você pode usar `.iloc[]` para filtrar dados com base em posições específicas, como selecionar linhas e colunas em um DataFrame. É especialmente útil quando você não conhece os rótulos das linhas ou colunas.
- **Exemplo Analógico:** Imagine que você está em um cinema e deseja escolher um assento baseado na sua posição na fila, em vez de pelo nome do filme.
- **Parâmetros:** 
  - `index`: O índice da linha ou coluna que você deseja acessar.
- **Retorno:** Retorna um DataFrame ou uma Série com os dados selecionados.
- **Exemplo de uso:**
  ```python
  import pandas as pd
  df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})
  result = df.iloc[0, 1]  # Seleciona o valor da primeira linha e segunda coluna.
  ```

