# Gráficos e Visualizações Utilizados

A seguir, são apresentados os códigos usados para gerar as visualizações, acompanhados de detalhes explicativos sobre cada um deles.

---

## Gráfico de Análise dos Resíduos e ACF (Modelo ARIMA)

Este código cria um gráfico com duas partes:
- **Parte Superior:** Plota os resíduos do modelo ARIMA (a partir do índice 13, para evitar valores iniciais instáveis). A visualização dos resíduos é útil para identificar tendências ou padrões não capturados pelo modelo.
- **Parte Inferior:** Exibe a função de autocorrelação (ACF) dos resíduos para 48 defasagens (lags). Este gráfico ajuda a verificar se os resíduos se comportam como ruído branco, o que é essencial para a validade do modelo.

Graph_Explanation
```python
plt.figure(figsize=(15,7))

# Parte superior: Plot dos resíduos do modelo ARIMA a partir do índice 13
plt.subplot(211)
best_model.resid[13:].plot()
plt.ylabel('Residuals')

# Parte inferior: Plot da função de autocorrelação (ACF) dos resíduos para 48 lags
ax = plt.subplot(212)
sm.graphics.tsa.plot_acf(best_model.resid[13:].values.squeeze(), lags=48, ax=ax)

# Exibe o p-value do teste Dickey-Fuller para verificar a estacionariedade
print("Dickey–Fuller test:: p=%f" % sm.tsa.stattools.adfuller(best_model.resid[13:])[1])

plt.tight_layout()
plt.show()
```

*Detalhes adicionais:*  
- O uso do corte (`best_model.resid[13:]`) elimina os resíduos iniciais que podem apresentar comportamento atípico.  
- A ACF é essencial para detectar correlações residuais; uma ausência de correlação significativa indica que o modelo ARIMA capturou adequadamente a estrutura da série temporal.

---

## Gráfico de Previsão do Preço do Bitcoin

Neste código, é realizada a visualização da série temporal dos preços reais (coluna `Weighted_Price`) juntamente com as previsões geradas pelo modelo ARIMA. A transformação inversa da Box-Cox (por meio da função `invboxcox`) reconverte os valores previstos para a escala original.

```python:Graph_Explanation.md
# Prepara o DataFrame com os preços reais e datas futuras para inclusão das previsões
df_month2 = df_month[['Weighted_Price']]
date_list = [
    datetime(2017, 6, 30), datetime(2017, 7, 31), datetime(2017, 8, 31), 
    datetime(2017, 9, 30), datetime(2017, 10, 31), datetime(2017, 11, 30), 
    datetime(2017, 12, 31), datetime(2018, 1, 31), datetime(2018, 1, 28)
]
future = pd.DataFrame(index=date_list, columns=df_month.columns)
df_month2 = pd.concat([df_month2, future])

# Calcula as previsões e aplica a transformação inversa Box-Cox para obter os valores na escala original
df_month2['forecast'] = invboxcox(best_model.predict(start=0, end=75), lmbda)

# Plota a série temporal dos preços reais e a linha de previsão (em vermelho tracejado)
plt.figure(figsize=(15,7))
df_month2.Weighted_Price.plot()  # Dados reais
df_month2.forecast.plot(color='r', ls='--', label='Predicted Weighted_Price')  # Previsão
plt.legend()
plt.title('Bitcoin exchanges, by months')
plt.ylabel('mean USD')
plt.show()
```

*Detalhes adicionais:*  
- O DataFrame é expandido para incluir datas futuras, garantindo que as previsões sejam plotadas no mesmo eixo temporal dos dados reais.  
- A linha de previsão em vermelho tracejado facilita a comparação visual entre os valores observados e os previstos.  
- A transformação inversa é crucial para interpretar os resultados na mesma escala dos dados originais.

---

## Visualização da Tabela de Preços (Car Price Prediction)

Embora não seja um gráfico tradicional, este código gera um DataFrame que compara os preços reais com os previstos e calcula a diferença entre eles. Essa visualização tabular é útil para uma análise numérica detalhada do desempenho do modelo.

```python:Graph_Explanation.md
pred_df = pd.DataFrame({
    'Actual': y_test, 
    'Predicted': y_pred, 
    'Difference': y_test - y_pred
})
pred_df
```

*Detalhes adicionais:*  
- A tabela mostra, lado a lado, os valores reais e os valores previstos, permitindo identificar rapidamente discrepâncias.  
- Esse resultado pode servir de base para a criação de gráficos complementares, como scatter plots ou gráficos de barras, ajudando na avaliação mais visual dos erros do modelo.
```
