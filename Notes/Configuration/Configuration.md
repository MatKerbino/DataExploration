### `plt.figure(figsize=(width, height))`
- **O que faz:** Cria uma "área em branco" (figura) onde os gráficos serão desenhados.
- **Detalhes:** O parâmetro `figsize` define as dimensões da figura, especificando a largura e a altura em polegadas.  
- **Exemplo Analógico:** É como escolher o tamanho de uma folha de papel para desenhar seus gráficos.

### `plt.subplot(nrows, ncols, index)`
- **O que faz:** Divide a figura em uma grade e seleciona uma seção (subárea) para a plotagem.
- **Detalhes:** 
  - `nrows` define o número de linhas na grade.
  - `ncols` define o número de colunas na grade.
  - `index` seleciona qual célula (posição) da grade será utilizada.
- **Exemplo Analógico:** Imagine dividir uma folha em vários quadrantes para colocar diferentes desenhos em cada área.

### `plt.tight_layout()`
- **O que faz:** Organiza automaticamente os elementos do gráfico para evitar que se sobreponham.
- **Detalhes:** Garante que títulos, rótulos e demais anotações fiquem bem posicionados e legíveis.
- **Exemplo Analógico:** É como ajustar quadros em uma parede para que fiquem arrumados e sem se tocar.

### `plt.ylabel('texto')`
- **O que faz:** Define um rótulo para o eixo Y (vertical) do gráfico.
- **Detalhes:** Isso ajuda quem está vendo o gráfico a entender qual informação está sendo representada naquele eixo.
- **Exemplo Analógico:** Imagine escrever uma legenda na lateral de um gráfico para descrever o que os números representam, como "Temperatura (°C)".

### `plt.title('texto')`
- **O que faz:** Adiciona um título ao gráfico.
- **Detalhes:** O título oferece uma visão rápida do conteúdo ou propósito do gráfico.
- **Exemplo Analógico:** Como colocar um título em um desenho ou pintura para indicar qual o tema principal do trabalho.

### `plt.legend()`
- **O que faz:** Exibe uma legenda que identifica diferentes elementos ou séries de dados no gráfico.
- **Detalhes:** A legenda ajuda a distinguir, por exemplo, dados reais de dados previstos ou categorias diferentes.
- **Exemplo Analógico:** Imagine um rótulo de cores em um mapa, explicando o que cada cor significa.

### `plt.show()`
- **O que faz:** Exibe o gráfico na tela.
- **Detalhes:** Após definir e desenhar todos os elementos do gráfico, este comando torna a figura visível para o usuário.
- **Exemplo Analógico:** Funciona como dar o "play" em um filme, para que você possa ver o resultado final do seu trabalho.