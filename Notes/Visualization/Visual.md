### DataFrame.head()
  - A função permite ver as primeiras linhas do DataFrame, o que é análogo a abrir as primeiras páginas de um relatório para entender sua estrutura.

### pandas.DataFrame(dictionary)
- **O que faz:** Cria uma tabela (DataFrame) a partir de um dicionário de dados.
- **Detalhes:** Cada chave do dicionário se torna uma coluna na tabela e seus respectivos valores formam as linhas, organizando os dados de forma estruturada.
- **Exemplo Analógico:** Imagine preencher uma planilha de Excel, onde cada coluna tem um título e os dados são arranjados em linhas correspondentes.

### data.isnull().sum()
A função é fundamental para identificar a quantidade de dados ausentes em cada coluna. Esse passo é análogo a revisar um formulário em busca de campos não preenchidos.

### groupby().size()
Utilizado para contar a quantidade de dados diferentes.

### describe()
- **O que faz:** A função fornece um resumo estatístico das colunas numéricas de um DataFrame, incluindo contagem, média, desvio padrão, valores mínimo e máximo, e os quartis (25%, 50%, 75%).
- **Detalhes:**  
  Essa função é útil para obter uma visão geral rápida da distribuição dos dados e identificar possíveis anomalias ou padrões.
- **Exemplo Analógico:**  
  Imagine que você está revisando um relatório financeiro que resume os principais indicadores de desempenho, como receita, lucro e despesas, permitindo uma análise rápida da saúde financeira da empresa.

### .shape
  Fornece as dimensões do dataframe

### .value_counts()
- **O que faz:** Conta a frequência de valores únicos em uma coluna de um DataFrame.
- **Detalhes:** Retorna uma série com os valores únicos como índice e suas respectivas contagens como valores. É útil para entender a distribuição de dados categóricos.
- **Exemplo:** Se você tiver uma coluna com os valores `['A', 'B', 'A', 'C', 'B', 'A']`, `data['coluna'].value_counts()` retornará: