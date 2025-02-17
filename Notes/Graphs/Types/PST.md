## Previsão da Série Temporal

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