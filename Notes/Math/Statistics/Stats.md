# import statistics from sts

## Cálculo de Medidas de Tendência Central

### mean()
- **O que faz:** Calcula a média aritmética de um conjunto de dados.
- **Detalhes:** A média é obtida somando todos os valores e dividindo pelo número total de valores. É uma medida comum de tendência central.
- **Exemplo Analógico:** Imagine que você está calculando a média de notas de uma turma; você soma todas as notas e divide pelo número de alunos.
- **Retorno:** Retorna um número que representa a média dos valores.
- **Exemplo de uso:**
  ```python
  import statistics
  media = statistics.mean([1, 2, 3, 4, 5])  # Retorna 3
  ```

### median()
- **O que faz:** Calcula a mediana, que é o valor central de um conjunto de dados ordenados.
- **Detalhes:** Para calcular a mediana, os dados devem ser ordenados. Se o número de valores for ímpar, a mediana é o valor do meio; se for par, é a média dos dois valores centrais.
- **Exemplo Analógico:** Pense em uma corrida onde você quer saber o tempo do corredor que ficou exatamente no meio; você ordena os tempos e pega o do meio.
- **Retorno:** Retorna um número que representa a mediana dos valores.
- **Exemplo de uso:**
  ```python
  import statistics
  mediana = statistics.median([1, 3, 3, 6, 7, 8, 9])  # Retorna 6
  ```

### mode()
- **O que faz:** Retorna o valor que aparece com mais frequência em um conjunto de dados.
- **Detalhes:** A moda é útil para identificar a tendência mais comum em um conjunto de dados, especialmente em dados categóricos.
- **Exemplo Analógico:** Imagine que você está contando as cores de balas em um pacote; a cor que aparece mais vezes é a moda.
- **Retorno:** Retorna o valor mais frequente no conjunto de dados.
- **Exemplo de uso:**
  ```python
  import statistics
  moda = statistics.mode([1, 1, 2, 3])  # Retorna 1
  ```

## Cálculo de Medidas de Dispersão

### stdev()
- **O que faz:** Calcula o desvio padrão, que mede a quantidade de variação ou dispersão em um conjunto de dados.
- **Detalhes:** O desvio padrão indica o quanto os valores se afastam da média. Um desvio padrão baixo significa que os valores estão próximos da média, enquanto um alto indica que estão mais dispersos.
- **Exemplo Analógico:** Pense em um grupo de pessoas com alturas; se todos têm alturas semelhantes, o desvio padrão é baixo; se as alturas variam muito, o desvio padrão é alto.
- **Retorno:** Retorna um número que representa o desvio padrão dos valores.
- **Exemplo de uso:**
  ```python
  import statistics
  desvio_padrao = statistics.stdev([1, 2, 3, 4, 5])  # Retorna aproximadamente 1.58
  ```

### variance()
- **O que faz:** Calcula a variância, que é o quadrado do desvio padrão e também mede a dispersão dos dados.
- **Detalhes:** A variância fornece uma medida da dispersão dos dados em relação à média. É útil para entender a variabilidade dos dados.
- **Exemplo Analógico:** Imagine que você está avaliando a consistência de um produto; se a variância é baixa, os produtos são muito semelhantes; se é alta, há muita variação.
- **Retorno:** Retorna um número que representa a variância dos valores.
- **Exemplo de uso:**
  ```python
  import statistics
  variancia = statistics.variance([1, 2, 3, 4, 5])  # Retorna 2.5
  ```

### median_low() e median_high()
- **O que fazem:** Retornam a mediana, mas com um comportamento diferente em conjuntos de dados com um número par de elementos.
- **Detalhes:** `median_low()` retorna o menor dos dois valores centrais, enquanto `median_high()` retorna o maior.
- **Retorno:** Retornam números que representam a mediana com base no comportamento especificado.
- **Exemplo de uso:**
  ```python
  import statistics
  mediana_baixa = statistics.median_low([1, 2, 3, 4])  # Retorna 2
  mediana_alta = statistics.median_high([1, 2, 3, 4])  # Retorna 3
  ```
