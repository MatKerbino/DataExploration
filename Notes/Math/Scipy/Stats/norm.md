## scipy.stats.norm
- **O que faz:** Representa a distribuição normal (gaussiana) e fornece funções para calcular propriedades dessa distribuição.
- **Detalhes:** A distribuição normal é caracterizada por sua média (mu) e desvio padrão (sigma). É amplamente utilizada em estatísticas e ciências sociais.
- **Exemplo Analógico:** Pense em uma distribuição de alturas em uma população; a maioria das pessoas terá alturas próximas à média, com menos pessoas em alturas extremas.
- **Parâmetros:** 
  - `loc`: A média da distribuição (mu).
  - `scale`: O desvio padrão da distribuição (sigma).
- **Retorno:** Retorna um objeto que representa a distribuição normal com os parâmetros especificados.
- **Exemplo de uso:**
  ```python
  from scipy.stats import norm
  distribution = norm(loc=0, scale=1)  # Cria uma distribuição normal padrão.
  ```

### norm.cdf()
- **O que faz:** Calcula a função de distribuição acumulada (CDF) para a distribuição normal.
- **Detalhes:** A CDF fornece a probabilidade de que uma variável aleatória normalmente distribuída seja menor ou igual a um determinado valor.
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

### norm.sf()
- **O que faz:** Calcula a função de sobrevivência (SF) para a distribuição normal.
- **Detalhes:** A SF fornece a probabilidade de que uma variável aleatória normalmente distribuída seja maior do que um determinado valor.
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

### norm.rvs()
- **O que faz:** Gera variáveis aleatórias a partir de uma distribuição normal.
- **Detalhes:** A função `rvs` (random variates) permite amostrar valores aleatórios de uma distribuição normal especificada por sua média (loc) e desvio padrão (scale).
- **Exemplo Analógico:** Imagine que você está simulando a altura de um grupo de pessoas, onde a altura segue uma distribuição normal; `norm.rvs()` ajuda a gerar essas alturas aleatórias.
- **Parâmetros:** 
  - `size`: O número de amostras a serem geradas (opcional).
  - `loc`: A média da distribuição (opcional, padrão é 0).
  - `scale`: O desvio padrão da distribuição (opcional, padrão é 1).
- **Retorno:** Retorna um array de variáveis aleatórias amostradas da distribuição normal especificada.
- **Exemplo de uso:**
  ```python
  from scipy.stats import norm
  random_samples = norm.rvs(loc=65, scale=10, size=100)  # Gera 100 amostras de uma distribuição normal com média 65 e desvio padrão 10.
  ```
