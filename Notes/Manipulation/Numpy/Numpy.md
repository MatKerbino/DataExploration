import numpy as np

### np.random.seed()
- **O que faz:** Define a semente para o gerador de números aleatórios, garantindo que os resultados sejam reproduzíveis em execuções subsequentes.
- **Detalhes:** Ao definir uma semente, você pode garantir que a sequência de números aleatórios gerados será a mesma em cada execução do código, o que é útil para testes e depuração.
- **Exemplo Analógico:** Imagine que você está jogando um dado. Se você sempre começar com o mesmo estado (semente), você obterá a mesma sequência de resultados.
- **Parâmetros:** 
  - `seed`: Um número inteiro que inicializa o gerador de números aleatórios.
- **Retorno:** Não retorna nenhum valor, mas afeta a geração de números aleatórios subsequentes.
- **Exemplo de uso:**
  ```python
  import numpy as np
  np.random.seed(42)
  random_numbers = np.random.rand(5)  # Sempre gerará os mesmos 5 números aleatórios.
  ```

### np.random.choice()
- **O que faz:** Gera uma amostra aleatória de um conjunto de dados, permitindo a seleção de elementos com ou sem reposição.
- **Detalhes:** Você pode especificar o tamanho da amostra e se deseja que os elementos sejam escolhidos com ou sem reposição.
- **Exemplo Analógico:** Se você tem uma caixa com bolas de diferentes cores e deseja escolher algumas aleatoriamente, `np.random.choice()` permite que você faça isso de forma controlada.
- **Parâmetros:** 
  - `a`: O array ou lista de onde os elementos serão escolhidos.
  - `size`: O número de amostras a serem retiradas.
  - `replace`: Um booleano que indica se a amostragem deve ser feita com reposição.
- **Retorno:** Um array com os elementos escolhidos aleatoriamente.
- **Exemplo de uso:**
  ```python
  import numpy as np
  sample = np.random.choice([1, 2, 3, 4, 5], size=3, replace=False)  # Seleciona 3 números sem reposição.
  ```