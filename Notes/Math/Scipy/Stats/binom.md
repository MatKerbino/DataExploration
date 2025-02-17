## scipy.stats.binom
- **O que é:** `scipy.stats.binom` representa a distribuição binomial, que descreve o número de sucessos em uma sequência de experimentos de Bernoulli independentes e identicamente distribuídos (iid), onde cada experimento tem dois resultados possíveis (sucesso ou fracasso).
- **Detalhes:** A distribuição binomial é caracterizada por dois parâmetros: o número de experimentos (n) e a probabilidade de sucesso em cada experimento (p). É amplamente utilizada em estatísticas para modelar eventos discretos.
- **Exemplo Analógico:** Pense em lançar uma moeda várias vezes; a distribuição binomial pode ser usada para calcular a probabilidade de obter um certo número de caras em um número fixo de lançamentos.

### scipy.stats.binom.pmf()
- **O que faz:** Calcula a função de massa de probabilidade (PMF) para a distribuição binomial.
- **Detalhes:** A PMF fornece a probabilidade de obter exatamente k sucessos em n experimentos. É útil para determinar a probabilidade de um número específico de sucessos em um experimento binomial.
- **Exemplo Analógico:** Imagine que você está lançando uma moeda 10 vezes e quer saber a probabilidade de obter exatamente 6 caras; a PMF ajuda a calcular essa probabilidade.
- **Parâmetros:** 
  - `k`: O número de sucessos desejados.
  - `n`: O número total de experimentos.
  - `p`: A probabilidade de sucesso em cada experimento.
- **Retorno:** Retorna a probabilidade de obter exatamente k sucessos em n experimentos.
- **Exemplo de uso:**
  ```python
  from scipy.stats import binom
  probability = binom.pmf(k=6, n=10, p=0.5)  # Calcula a probabilidade de obter exatamente 6 caras em 10 lançamentos de moeda.
  ```

### scipy.stats.binom.cdf()
- **O que faz:** Calcula a função de distribuição acumulada (CDF) para a distribuição binomial.
- **Detalhes:** A CDF fornece a probabilidade de obter k ou menos sucessos em n experimentos. É útil para determinar a probabilidade acumulada em relação a um número crítico de sucessos em testes de hipóteses.
- **Exemplo Analógico:** Imagine que você está lançando uma moeda 10 vezes e quer saber a probabilidade de obter 6 ou menos caras; a CDF ajuda a calcular essa probabilidade.
- **Parâmetros:** 
  - `k`: O número máximo de sucessos desejados.
  - `n`: O número total de experimentos.
  - `p`: A probabilidade de sucesso em cada experimento.
- **Retorno:** Retorna a probabilidade de obter k ou menos sucessos em n experimentos.
- **Exemplo de uso:**
  ```python
  from scipy.stats import binom
  probability = binom.cdf(k=6, n=10, p=0.5)  # Calcula a probabilidade de obter 6 ou menos caras em 10 lançamentos de moeda.
  ```
