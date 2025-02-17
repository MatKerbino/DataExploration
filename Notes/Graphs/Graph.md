### `Dataframe.plot()`
- **O que faz:** Desenha um gráfico de linhas conectando os pontos de dados.
- **Detalhes:** É usado para representar visualmente informações que variam de maneira contínua, como a evolução de um valor ao longo do tempo.
- **Exemplo Analógico:** Semelhante a unir pontos em um gráfico feito à mão para formar uma linha contínua.

### Dataframe.boxplot()
- **O que faz:** O método `.boxplot()` gera um gráfico de caixa (boxplot) a partir dos dados de um DataFrame do Pandas.
- **Detalhes:** O boxplot exibe a mediana, os quartis e os valores atípicos de um conjunto de dados. É uma ferramenta útil para visualizar a dispersão e a simetria dos dados, além de identificar outliers.
- **Exemplo Analógico:** Imagine que você está analisando as notas de uma turma; um boxplot pode mostrar a mediana das notas, a variação e se há alunos com notas muito acima ou abaixo da média.
- **Parâmetros:**
  - `column`: O nome da coluna a ser plotada (opcional).
  - `by`: O nome de uma coluna para agrupar os dados (opcional).
  - `vert`: Um booleano que indica se o boxplot deve ser vertical (padrão é True).
  - `patch_artist`: Um booleano que indica se as caixas devem ser preenchidas com cor (padrão é False).
- **Retorno:** Retorna um objeto de artista que representa o boxplot.
- **Exemplo de uso:**
  ```python
  import pandas as pd
  import matplotlib.pyplot as plt

  # Criando um DataFrame de exemplo
  data = {'Notas': [1, 2, 5, 6, 7, 8, 9, 10, 12, 13, 14, 15]}
  df = pd.DataFrame(data)

  # Cria um boxplot para a coluna 'Notas'
  df.boxplot(column='Notas')  
  plt.title('Boxplot de Notas')
  plt.ylabel('Notas')
  plt.show()  # Exibe o gráfico.
  ```

#### Variações de plot
- **bar:** Desenha um gráfico de barras
- **scatter:** Desenha um gráfico de dispersão, mostrando a relação entre duas variáveis.

### `sm.graphics.tsa.plot_acf()`
- **O que faz:** Cria um gráfico de autocorrelação, que mostra como os dados estão correlacionados com eles mesmos em diferentes intervalos.
- **Detalhes:** É amplamente utilizado para analisar séries temporais, ajudando a identificar padrões e repetições nos dados.
- **Exemplo Analógico:** É como observar se há uma regularidade nos episódios de uma série, onde certos comportamentos se repetem ao longo do tempo.






