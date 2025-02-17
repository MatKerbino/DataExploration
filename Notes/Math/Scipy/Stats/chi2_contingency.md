## scipy.stats.chi2_contingency
- **O que é:** `scipy.stats.chi2_contingency` é uma função que realiza o teste do qui-quadrado de independência. Este teste é utilizado para determinar se existe uma associação significativa entre duas variáveis categóricas em uma tabela de contingência.
- **Detalhes:** O teste do qui-quadrado avalia se a distribuição observada dos dados difere significativamente da distribuição esperada sob a hipótese nula de que as variáveis são independentes. O resultado do teste inclui o valor do qui-quadrado, o valor de p e os graus de liberdade.
- **Exemplo Analógico:** Imagine que você está analisando se a preferência por um tipo de produto (A ou B) varia de acordo com a faixa etária dos consumidores (jovens, adultos, idosos). O teste do qui-quadrado pode ser usado para verificar se a preferência é independente da faixa etária.
- **Parâmetros:**
  - `observed`: Uma matriz (ou tabela) que contém as contagens observadas para cada combinação de categorias.
  - `correction`: Um booleano que indica se a correção de Yates deve ser aplicada (opcional, padrão é False).
- **Retorno:** Retorna uma tupla contendo o valor do qui-quadrado, o valor de p, os graus de liberdade e as frequências esperadas.
- **Exemplo de uso:**
  ```python
  from scipy.stats import chi2_contingency
  # Tabela de contingência
  data = [[10, 20, 30], [6, 9, 17]]
  chi2, p, dof, expected = chi2_contingency(data)  # Realiza o teste do qui-quadrado.
  ```
