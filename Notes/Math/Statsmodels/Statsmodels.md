## statsmodels
- **O que é:** `statsmodels` é uma biblioteca em Python que fornece classes e funções para a estimativa de modelos estatísticos, realização de testes estatísticos e exploração de dados. É amplamente utilizada para análise estatística e econometria.

#### 2. statsmodels.formula.api.ols()
- **O que faz:** Ajusta um modelo de regressão linear usando a abordagem de Mínimos Quadrados Ordinários (OLS).
- **Detalhes:** Permite especificar um modelo de regressão linear usando uma fórmula, facilitando a inclusão de variáveis independentes e interações. A função retorna um objeto que contém informações sobre o modelo ajustado.
- **Exemplo de uso:**
  ```python
  from statsmodels.formula.api import ols
  model = ols('y ~ x1 + x2', data=df).fit()  # Ajusta um modelo de regressão linear.
  ```

#### statsmodels.tukeyhsd
- **O que faz:** Realiza o teste de Tukey para comparações múltiplas entre grupos.
- **Detalhes:** O teste de Tukey é usado após a ANOVA para identificar quais grupos são significativamente diferentes entre si. Ele fornece intervalos de confiança para as diferenças de médias entre todos os pares de grupos.
- **Exemplo de uso:**
  ```python
  from statsmodels.stats.multicomp import pairwise_tukeyhsd

  tukey_results = pairwise_tukeyhsd(data['value'], data['group'])  # Realiza o teste de Tukey.
  print(tukey_results)  # Exibe os resultados do teste de Tukey.
  ```


