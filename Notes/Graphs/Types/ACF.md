## Análise dos Resíduos e Função de Autocorrelação (ACF)

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