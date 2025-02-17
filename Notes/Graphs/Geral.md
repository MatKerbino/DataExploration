# Introdução à Criação de Gráficos em Python

Este documento apresenta os principais comandos utilizados para criar gráficos e organizar dados em Python. 

---

## Categoria 1: Configuração da Figura

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

---

## Categoria 2: Plotagem e Personalização dos Dados

### `plot()`
- **O que faz:** Desenha um gráfico de linhas conectando os pontos de dados.
- **Detalhes:** É usado para representar visualmente informações que variam de maneira contínua, como a evolução de um valor ao longo do tempo.
- **Exemplo Analógico:** Semelhante a unir pontos em um gráfico feito à mão para formar uma linha contínua.

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

---

## Categoria 3: Ajuste e Exibição do Gráfico

### `plt.tight_layout()`
- **O que faz:** Organiza automaticamente os elementos do gráfico para evitar que se sobreponham.
- **Detalhes:** Garante que títulos, rótulos e demais anotações fiquem bem posicionados e legíveis.
- **Exemplo Analógico:** É como ajustar quadros em uma parede para que fiquem arrumados e sem se tocar.

### `plt.show()`
- **O que faz:** Exibe o gráfico na tela.
- **Detalhes:** Após definir e desenhar todos os elementos do gráfico, este comando torna a figura visível para o usuário.
- **Exemplo Analógico:** Funciona como dar o "play" em um filme, para que você possa ver o resultado final do seu trabalho.

---

## Categoria 4: Funções de Transformação e Análise

### `pd.concat()`
- **O que faz:** Junta (concatena) dois ou mais conjuntos de dados (DataFrames) em um único conjunto.
- **Detalhes:** É útil para unir dados que possam estar espalhados em diferentes estruturas, formando uma base de dados completa.
- **Exemplo Analógico:** Imagine colar várias páginas de anotações para formar um único caderno com todas as suas informações.

### Funções de Transformação (por exemplo, `invboxcox`)
- **O que fazem:** Alteram os dados de uma forma para outra e, em alguns casos, retornam os dados à sua forma original.
- **Detalhes:** Essas funções são úteis quando os dados passam por uma transformação (como ajuste de escala) para melhorar o desempenho de um modelo, e depois precisam ser convertidos de volta para facilitar a interpretação.
- **Exemplo Analógico:** Pense em converter uma receita de medição internacional para o sistema local e, depois, voltar para as medidas originais.

### `sm.graphics.tsa.plot_acf()`
- **O que faz:** Cria um gráfico de autocorrelação, que mostra como os dados estão correlacionados com eles mesmos em diferentes intervalos.
- **Detalhes:** É amplamente utilizado para analisar séries temporais, ajudando a identificar padrões e repetições nos dados.
- **Exemplo Analógico:** É como observar se há uma regularidade nos episódios de uma série, onde certos comportamentos se repetem ao longo do tempo.

---

## Categoria 5: Criação e Visualização de Tabelas

### `pd.DataFrame(dictionary)`
- **O que faz:** Cria uma tabela (DataFrame) a partir de um dicionário de dados.
- **Detalhes:** Cada chave do dicionário se torna uma coluna na tabela e seus respectivos valores formam as linhas, organizando os dados de forma estruturada.
- **Exemplo Analógico:** Imagine preencher uma planilha de Excel, onde cada coluna tem um título e os dados são arranjados em linhas correspondentes.

# Gráficos e Visualizações Utilizados

A seguir, estão os códigos explicados, organizados em categorias de gráficos, com detalhes para facilitar o entendimento.

---

## Categoria 1: Análise dos Resíduos e Função de Autocorrelação (ACF)

Este código plota dois gráficos relacionados à análise dos resíduos gerados por um modelo. A ideia é identificar padrões ou dependências temporais que possam indicar problemas no modelo.

```python
plt.figure(figsize=(15,7))

# Parte superior: exibe os resíduos (a partir do índice 13 para ignorar os valores iniciais possivelmente instáveis)
plt.subplot(211)
best_model.resid[13:].plot()
plt.ylabel('Residuals')

# Parte inferior: plota a função de autocorrelação (ACF) dos resíduos para 48 defasagens (lags)
ax = plt.subplot(212)
sm.graphics.tsa.plot_acf(best_model.resid[13:].values.squeeze(), lags=48, ax=ax)

# Imprime o p-value do teste de Dickey-Fuller para verificar a estacionariedade dos resíduos
print("Dickey–Fuller test:: p=%f" % sm.tsa.stattools.adfuller(best_model.resid[13:])[1])

plt.tight_layout()
plt.show()
```

**Detalhes:**
- **Resíduos a partir do índice 13:** Essa fatia exclui os resíduos iniciais, que podem possuir comportamentos anômalos devido à inicialização do modelo.
- **Plot da ACF:** Ajuda a visualizar se há autocorrelação significativa nos resíduos. A ausência desta sinaliza que os erros são, em sua maior parte, ruído branco.
- **Teste Dickey-Fuller:** Imprimir o p-value auxilia na confirmação de que os resíduos são estacionários, um pressuposto importante para a validade do modelo.

---

## Categoria 2: Previsão da Série Temporal

Neste trecho, o código gera uma visualização que compara a série histórica dos valores reais com as previsões de um modelo. As previsões passam por uma transformação inversa para serem plotadas na escala original dos dados.

```python
# Prepara o DataFrame com os valores reais e adiciona datas futuras para incluir as previsões
df_month2 = df_month[['Weighted_Price']]
date_list = [
    datetime(2017, 6, 30), datetime(2017, 7, 31), datetime(2017, 8, 31), 
    datetime(2017, 9, 30), datetime(2017, 10, 31), datetime(2017, 11, 30), 
    datetime(2017, 12, 31), datetime(2018, 1, 31), datetime(2018, 1, 28)
]
future = pd.DataFrame(index=date_list, columns=df_month.columns)
df_month2 = pd.concat([df_month2, future])

# Calcula as previsões e aplica a transformação inversa Box-Cox, convertendo os valores para a escala original
df_month2['forecast'] = invboxcox(best_model.predict(start=0, end=75), lmbda)

# Plota a série temporal dos valores reais e das previsões
plt.figure(figsize=(15,7))
df_month2.Weighted_Price.plot()  # Série real
df_month2.forecast.plot(color='r', ls='--', label='Predicted Weighted_Price')  # Previsões
plt.legend()
plt.title('Bitcoin exchanges, by months')
plt.ylabel('mean USD')
plt.show()
```

**Detalhes:**
- **DataFrame com datas futuras:** O DataFrame é expandido para incluir datas posteriores, garantindo que as previsões sejam exibidas de forma contínua junto aos dados históricos.
- **Transformação inversa com Box-Cox:** Essencial para reverter a transformação aplicada anteriormente, possibilitando a interpretação das previsões na mesma escala dos dados reais.
- **Visualização:** A linha tracejada vermelha distingue claramente os valores previstos dos dados reais, facilitando a comparação visual.

---

## Categoria 3: Visualização Tabular dos Resultados

Embora não seja um gráfico no sentido tradicional, esse trecho de código cria uma tabela (DataFrame) que organiza os resultados comparando os valores reais com os valores previstos e mostrando a diferença entre eles. Essa visualização é útil para uma análise detalhada dos resultados numéricos.

```python
pred_df = pd.DataFrame({
    'Actual': y_test, 
    'Predicted': y_pred, 
    'Difference': y_test - y_pred
})
pred_df
```

**Detalhes:**
- **Tabela de comparações:** Apresenta três colunas – os valores reais, os previstos e a diferença entre ambos, facilitando a identificação de discrepâncias.
- **Base para outras visualizações:** Essa estrutura tabular pode ser enriquecida com gráficos adicionais, como scatter plots ou gráficos de barras, para uma análise visual mais aprofundada dos erros.
