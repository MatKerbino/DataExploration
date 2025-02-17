## scipy.stats.t
- **O que é:** `scipy.stats.t` representa a distribuição t de Student, que é uma distribuição de probabilidade utilizada em estatísticas, especialmente em testes de hipóteses e intervalos de confiança para médias quando a amostra é pequena e a variância populacional é desconhecida.
- **Detalhes:** A distribuição t é semelhante à distribuição normal, mas tem caudas mais pesadas, o que a torna mais adequada para amostras pequenas. O número de graus de liberdade (df) é um parâmetro importante que afeta a forma da distribuição.
- **Exemplo Analógico:** Pense na distribuição t como uma versão "mais cautelosa" da distribuição normal; ela leva em conta a incerteza adicional que vem de trabalhar com amostras pequenas.

### scipy.stats.t.cdf()
- **O que faz:** Calcula a função de distribuição acumulada (CDF) para a distribuição t de Student.
- **Detalhes:** A CDF fornece a probabilidade de que uma variável aleatória t seja menor ou igual a um determinado valor. É útil para determinar a probabilidade acumulada em relação a um valor crítico em testes de hipóteses.
- **Exemplo Analógico:** Imagine que você está avaliando a probabilidade de um estudante obter uma pontuação menor ou igual a 2.5 em um teste t; a CDF ajuda a determinar essa probabilidade.
- **Parâmetros:** 
  - `x`: O valor para o qual a CDF deve ser calculada.
  - `df`: O número de graus de liberdade.
- **Retorno:** Retorna a probabilidade acumulada até o valor `x`.
- **Exemplo de uso:**
  ```python
  from scipy.stats import t
  probability = t.cdf(2.5, df=10)  # Calcula a probabilidade de ser menor ou igual a 2.5 com 10 graus de liberdade.
  ```

### scipy.stats.t.sf()
- **O que faz:** Calcula a função de sobrevivência (SF) para a distribuição t de Student.
- **Detalhes:** A SF fornece a probabilidade de que uma variável aleatória t seja maior do que um determinado valor. É o complemento da CDF.
- **Exemplo Analógico:** Imagine que você está avaliando a probabilidade de um estudante obter uma pontuação maior que 2.5 em um teste t; a SF ajuda a determinar essa probabilidade.
- **Parâmetros:** 
  - `x`: O valor para o qual a SF deve ser calculada.
  - `df`: O número de graus de liberdade.
- **Retorno:** Retorna a probabilidade de ser maior que o valor `x`.
- **Exemplo de uso:**
  ```python
  from scipy.stats import t
  probability = t.sf(2.5, df=10)  # Calcula a probabilidade de ser maior que 2.5 com 10 graus de liberdade.
  ```
