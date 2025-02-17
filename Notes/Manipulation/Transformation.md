### Funções de Transformação (por exemplo, `invboxcox`)
- **O que fazem:** Alteram os dados de uma forma para outra e, em alguns casos, retornam os dados à sua forma original.
- **Detalhes:** Essas funções são úteis quando os dados passam por uma transformação (como ajuste de escala) para melhorar o desempenho de um modelo, e depois precisam ser convertidos de volta para facilitar a interpretação.
- **Exemplo Analógico:** Pense em converter uma receita de medição internacional para o sistema local e, depois, voltar para as medidas originais.

### `pd.concat()`
- **O que faz:** Junta (concatena) dois ou mais conjuntos de dados (DataFrames) em um único conjunto.
- **Detalhes:** É útil para unir dados que possam estar espalhados em diferentes estruturas, formando uma base de dados completa.
- **Exemplo Analógico:** Imagine colar várias páginas de anotações para formar um único caderno com todas as suas informações.

### .fillna()
- **O que faz:** A função `fillna()` é utilizada para preencher valores ausentes (NaN) em um DataFrame com um valor específico, como a média, mediana ou um valor constante.
- **Detalhes:**  
  Essa função é útil para evitar problemas em análises e modelagens que não aceitam dados ausentes.
- **Exemplo Analógico:**  
  Imagine que você está completando um formulário e decide preencher os campos em branco com "N/A" para indicar que não se aplica.

