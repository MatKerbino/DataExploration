## scipy.stats
- **O que é:** `scipy.stats` é um módulo da biblioteca SciPy que fornece uma ampla gama de funções estatísticas e distribuições de probabilidade.
- **Detalhes:** Este módulo inclui funções para calcular estatísticas descritivas, realizar testes de hipóteses, gerar variáveis aleatórias de várias distribuições e criar gráficos de probabilidade.
- **Exemplo Analógico:** Pense no `scipy.stats` como uma caixa de ferramentas para estatísticos; ele contém todas as ferramentas necessárias para realizar análises estatísticas e modelagem de dados.
- **Funcionalidades:** Inclui distribuições como normal, binomial, Poisson, e funções para calcular quantis, médias, variâncias, e muito mais.
- **Exemplo de uso:**
  ```python
  from scipy import stats
  mean = stats.norm.mean(loc=0, scale=1)  # Calcula a média da distribuição normal padrão.
  ```

### stats.cdf()
- **O que faz:** Calcula a função de distribuição acumulada (CDF) para uma distribuição específica.
- **Detalhes:** A CDF fornece a probabilidade de que uma variável aleatória seja menor ou igual a um determinado valor. É uma ferramenta importante para entender a distribuição de dados.
- **Exemplo Analógico:** Imagine que você está avaliando a probabilidade de um aluno obter uma nota menor ou igual a 70 em um teste; a CDF ajuda a determinar essa probabilidade.
- **Parâmetros:** 
  - `x`: O valor para o qual a CDF deve ser calculada.
  - `loc`: A média da distribuição (opcional).
  - `scale`: O desvio padrão da distribuição (opcional).
- **Retorno:** Retorna a probabilidade acumulada até o valor `x`.
- **Exemplo de uso:**
  ```python
  from scipy.stats import norm
  probability = norm.cdf(70, loc=65, scale=10)  # Calcula a probabilidade de ser menor ou igual a 70.
  ```

### stats.sf()
- **O que faz:** Calcula a função de sobrevivência (SF) para uma distribuição específica.
- **Detalhes:** A SF fornece a probabilidade de que uma variável aleatória seja maior do que um determinado valor. É o complemento da CDF.
- **Exemplo Analógico:** Imagine que você está avaliando a probabilidade de um aluno obter uma nota maior que 70 em um teste; a SF ajuda a determinar essa probabilidade.
- **Parâmetros:** 
  - `x`: O valor para o qual a SF deve ser calculada.
  - `loc`: A média da distribuição (opcional).
  - `scale`: O desvio padrão da distribuição (opcional).
- **Retorno:** Retorna a probabilidade de ser maior que o valor `x`.
- **Exemplo de uso:**
  ```python
  from scipy.stats import norm
  probability = norm.sf(70, loc=65, scale=10)  # Calcula a probabilidade de ser maior que 70.
  ```

### scipy.stats.shapiro()
- **O que faz:** Realiza o teste de Shapiro-Wilk para verificar a normalidade de um conjunto de dados.
- **Detalhes:** O teste de Shapiro-Wilk avalia se uma amostra de dados é proveniente de uma distribuição normal. Um valor de p menor que um nível de significância (geralmente 0.05) indica que a hipótese nula de normalidade pode ser rejeitada.
- **Exemplo Analógico:** Imagine que você está testando se as alturas de um grupo de pessoas seguem uma distribuição normal; o teste de Shapiro-Wilk ajuda a determinar isso.
- **Parâmetros:** 
  - `x`: O conjunto de dados a ser testado.
- **Retorno:** Retorna uma tupla contendo o estatístico do teste e o valor de p.
- **Exemplo de uso:**
  ```python
  from scipy import stats
  data = [1.2, 2.3, 2.1, 1.8, 2.5]
  stat, p_value = stats.shapiro(data)  # Realiza o teste de Shapiro-Wilk.
  ```

### scipy.stats.probplot()
- **O que faz:** Gera um gráfico de probabilidade (Q-Q plot) para comparar a distribuição de um conjunto de dados com uma distribuição teórica.
- **Detalhes:** O gráfico de probabilidade ajuda a visualizar se os dados seguem uma distribuição específica, como a normal. Os pontos no gráfico representam os quantis dos dados em comparação com os quantis da distribuição teórica.
- **Exemplo Analógico:** Pense em um gráfico que mostra se as notas de um teste seguem uma distribuição normal; o Q-Q plot ajuda a visualizar isso.
- **Parâmetros:** 
  - `x`: O conjunto de dados a ser comparado.
  - `dist`: A distribuição teórica a ser usada (por exemplo, `norm` para normal).
  - `plot`: Um objeto de gráfico onde o Q-Q plot será desenhado (opcional).
- **Retorno:** Retorna uma tupla contendo os quantis teóricos e os quantis amostrais.
- **Exemplo de uso:**
  ```python
  import matplotlib.pyplot as plt
  from scipy import stats
  data = [1.2, 2.3, 2.1, 1.8, 2.5]
  stats.probplot(data, dist="norm", plot=plt)  # Gera um gráfico de probabilidade.
  plt.show()  # Exibe o gráfico.
  ```