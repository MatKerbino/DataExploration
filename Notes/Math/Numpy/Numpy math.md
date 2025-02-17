# Import numpy as np

### np.mean()
- **O que faz:** Calcula a média aritmética de um conjunto de dados.
- **Detalhes:** A média é obtida somando todos os valores e dividindo pelo número total de valores. É uma medida comum de tendência central.
- **Exemplo Analógico:** Imagine que você está calculando a média de notas de uma turma; você soma todas as notas e divide pelo número de alunos.
- **Retorno:** Retorna um número que representa a média dos valores.
- **Exemplo de uso:**
  ```python
  import numpy as np
  media = np.mean([1, 2, 3, 4, 5])  # Retorna 3
  ```

### np.median()
- **O que faz:** Calcula a mediana, que é o valor central de um conjunto de dados ordenados.
- **Detalhes:** Para calcular a mediana, os dados devem ser ordenados. Se o número de valores for ímpar, a mediana é o valor do meio; se for par, é a média dos dois valores centrais.
- **Exemplo Analógico:** Pense em uma corrida onde você quer saber o tempo do corredor que ficou exatamente no meio; você ordena os tempos e pega o do meio.
- **Retorno:** Retorna um número que representa a mediana dos valores.
- **Exemplo de uso:**
  ```python
  import numpy as np
  mediana = np.median([1, 3, 3, 6, 7, 8, 9])  # Retorna 6
  ```

### np.quantile()
- **O que faz:** Calcula os quantis de um conjunto de dados, permitindo a análise de percentis.
- **Detalhes:** Os quantis dividem os dados em partes iguais, permitindo entender a distribuição dos dados em diferentes intervalos.
- **Exemplo Analógico:** Imagine que você está avaliando a distribuição de notas em uma turma; os quantis ajudam a entender como as notas estão distribuídas.
- **Retorno:** Retorna um número que representa o quantil especificado.
- **Exemplo de uso:**
  ```python
  import numpy as np
  quantis = np.quantile([1, 2, 3, 4, 5], 0.5)  # Retorna 3 (mediana)
  ```

### np.std()
- **O que faz:** Calcula o desvio padrão, que mede a quantidade de variação ou dispersão em um conjunto de dados.
- **Detalhes:** O desvio padrão indica o quanto os valores se afastam da média. Um desvio padrão baixo significa que os valores estão próximos da média, enquanto um alto indica que estão mais dispersos.
- **Exemplo Analógico:** Pense em um grupo de pessoas com alturas; se todos têm alturas semelhantes, o desvio padrão é baixo; se as alturas variam muito, o desvio padrão é alto.
- **Retorno:** Retorna um número que representa o desvio padrão dos valores.
- **Exemplo de uso:**
  ```python
  import numpy as np
  desvio_padrao = np.std([1, 2, 3, 4, 5])  # Retorna aproximadamente 1.41
  ```

