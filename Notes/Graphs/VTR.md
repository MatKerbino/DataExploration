## Visualização Tabular dos Resultados

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