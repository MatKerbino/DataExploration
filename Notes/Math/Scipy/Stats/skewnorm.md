## scipy.stats.skewnorm
- **O que é:** `skewnorm` é uma classe dentro do módulo `scipy.stats` que representa a distribuição normal assimétrica.
- **Detalhes:** A distribuição normal assimétrica é uma generalização da distribuição normal que permite a assimetria. É caracterizada por três parâmetros: a média (loc), o desvio padrão (scale) e o parâmetro de assimetria (a).
- **Exemplo Analógico:** Imagine que você está modelando a altura de um grupo de pessoas onde a altura não segue uma distribuição normal, mas tem uma cauda mais longa em uma direção; a distribuição normal assimétrica ajuda a capturar essa característica.
- **Funcionalidades:** Permite calcular propriedades como média, variância, quantis, e gerar variáveis aleatórias a partir dessa distribuição.
- **Exemplo de uso:**
  ```python
  from scipy.stats import skewnorm
  distribution = skewnorm(a=5, loc=0, scale=1)  # Cria uma distribuição normal assimétrica.
  mean = distribution.mean()  # Calcula a média da distribuição.
  ```

### scipy.stats.skewnorm.rvs()
- **O que faz:** Gera variáveis aleatórias a partir de uma distribuição normal assimétrica (skew normal).
- **Detalhes:** A função `rvs` (random variates) permite amostrar valores aleatórios de uma distribuição normal assimétrica especificada por sua média (loc), desvio padrão (scale) e parâmetro de assimetria (a).
- **Exemplo Analógico:** Imagine que você está simulando a altura de um grupo de pessoas onde a altura não segue uma distribuição normal, mas sim uma distribuição assimétrica; `skewnorm.rvs()` ajuda a gerar essas alturas aleatórias.
- **Parâmetros:** 
  - `a`: O parâmetro de assimetria (opcional).
  - `loc`: A média da distribuição (opcional, padrão é 0).
  - `scale`: O desvio padrão da distribuição (opcional, padrão é 1).
  - `size`: O número de amostras a serem geradas (opcional).
- **Retorno:** Retorna um array de variáveis aleatórias amostradas da distribuição normal assimétrica especificada.
- **Exemplo de uso:**
  ```python
  from scipy.stats import skewnorm
  random_samples = skewnorm.rvs(a=5, loc=0, scale=1, size=100)  # Gera 100 amostras de uma distribuição normal assimétrica.
  ```