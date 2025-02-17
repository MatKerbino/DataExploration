## scipy.stats.poisson
- **O que é:** `scipy.stats.poisson` representa a distribuição de Poisson, que descreve o número de eventos que ocorrem em um intervalo fixo de tempo ou espaço, dado que esses eventos ocorrem com uma taxa média constante e independentemente do tempo desde o último evento.
- **Detalhes:** A distribuição de Poisson é caracterizada por um único parâmetro, λ (lambda), que representa a taxa média de ocorrência de eventos. É amplamente utilizada em estatísticas para modelar eventos discretos que ocorrem em um intervalo fixo.
- **Exemplo Analógico:** Pense em contar o número de chamadas recebidas em um call center em uma hora; a distribuição de Poisson pode ser usada para modelar essa contagem.

### scipy.stats.poisson.pmf()
- **O que faz:** Calcula a função de massa de probabilidade (PMF) para a distribuição de Poisson.
- **Detalhes:** A PMF fornece a probabilidade de observar exatamente k eventos em um intervalo fixo, dado um valor médio λ. É útil para determinar a probabilidade de um número específico de eventos ocorrer.
- **Exemplo Analógico:** Imagine que você está contando o número de chamadas recebidas em um call center em uma hora e quer saber a probabilidade de receber exatamente 3 chamadas; a PMF ajuda a calcular essa probabilidade.
- **Parâmetros:** 
  - `k`: O número de eventos desejados.
  - `mu`: A taxa média de eventos (λ).
- **Retorno:** Retorna a probabilidade de observar exatamente k eventos.
- **Exemplo de uso:**
  ```python
  from scipy.stats import poisson
  probability = poisson.pmf(k=3, mu=5)  # Calcula a probabilidade de receber exatamente 3 chamadas quando a média é 5.
  ```

### scipy.stats.poisson.cdf()
- **O que faz:** Calcula a função de distribuição acumulada (CDF) para a distribuição de Poisson.
- **Detalhes:** A CDF fornece a probabilidade de observar k ou menos eventos em um intervalo fixo, dado um valor médio λ. É útil para determinar a probabilidade acumulada em relação a um número crítico de eventos.
- **Exemplo Analógico:** Imagine que você está contando o número de chamadas recebidas em um call center em uma hora e quer saber a probabilidade de receber 3 ou menos chamadas; a CDF ajuda a calcular essa probabilidade.
- **Parâmetros:** 
  - `k`: O número máximo de eventos desejados.
  - `mu`: A taxa média de eventos (λ).
- **Retorno:** Retorna a probabilidade de observar k ou menos eventos.
- **Exemplo de uso:**
  ```python
  from scipy.stats import poisson
  probability = poisson.cdf(k=3, mu=5)  # Calcula a probabilidade de receber 3 ou menos chamadas quando a média é 5.
  ```

### scipy.stats.poisson.sf()
- **O que faz:** Calcula a função de sobrevivência (SF) para a distribuição de Poisson.
- **Detalhes:** A SF fornece a probabilidade de observar mais do que k eventos em um intervalo fixo, dado um valor médio λ. É o complemento da CDF.
- **Exemplo Analógico:** Imagine que você está contando o número de chamadas recebidas em um call center em uma hora e quer saber a probabilidade de receber mais de 3 chamadas; a SF ajuda a calcular essa probabilidade.
- **Parâmetros:** 
  - `k`: O número de eventos desejados.
  - `mu`: A taxa média de eventos (λ).
- **Retorno:** Retorna a probabilidade de observar mais do que k eventos.
- **Exemplo de uso:**
  ```python
  from scipy.stats import poisson
  probability = poisson.sf(k=3, mu=5)  # Calcula a probabilidade de receber mais de 3 chamadas quando a média é 5.
  ```
