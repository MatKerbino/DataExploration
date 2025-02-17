import statistics from sts

### 1. Cálculo de Medidas de Tendência Central
- **mean()**: Calcula a média aritmética de um conjunto de dados.
  - **Exemplo:** `statistics.mean([1, 2, 3, 4, 5])` retorna `3`.
  
- **median()**: Calcula a mediana, que é o valor central de um conjunto de dados ordenados.
  - **Exemplo:** `statistics.median([1, 3, 3, 6, 7, 8, 9])` retorna `6`.

- **mode()**: Retorna o valor que aparece com mais frequência em um conjunto de dados.
  - **Exemplo:** `statistics.mode([1, 1, 2, 3])` retorna `1`.

### 2. Cálculo de Medidas de Dispersão
- **stdev()**: Calcula o desvio padrão, que mede a quantidade de variação ou dispersão em um conjunto de dados.
  - **Exemplo:** `statistics.stdev([1, 2, 3, 4, 5])` retorna aproximadamente `1.58`.

- **variance()**: Calcula a variância, que é o quadrado do desvio padrão e também mede a dispersão dos dados.
  - **Exemplo:** `statistics.variance([1, 2, 3, 4, 5])` retorna `2.5`.

### 3. Cálculos Adicionais
- **median_low()** e **median_high()**: Retornam a mediana, mas com um comportamento diferente em conjuntos de dados com um número par de elementos.
- **quantiles()**: Calcula os quantis de um conjunto de dados, permitindo a análise de percentis.