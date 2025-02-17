- **Estrutura do Modelo (Classe ANNModel):**  
  A rede neural é definida na classe `ANNModel`, que constrói a arquitetura com duas camadas ocultas e uma camada de saída para classificação.
  ```python
  class ANNModel(nn.Module):
      def __init__(self, input_size):
          super(ANNModel, self).__init__()
          self.fc1 = nn.Linear(input_size, 64)
          self.relu = nn.ReLU()
          self.fc2 = nn.Linear(64, 32)
          self.fc3 = nn.Linear(32, 2)
          self.softmax = nn.Softmax(dim=1)

      def forward(self, x):
          x = self.fc1(x)
          x = self.relu(x)
          x = self.fc2(x)
          x = self.relu(x)
          x = self.fc3(x)
          return self.softmax(x)
  ```
- **Detalhes:**  
  - **fc1, fc2, fc3:** Camadas lineares que transformam os dados.  
  - **ReLU:** Função de ativação que introduz não-linearidade.  
  - **Softmax:** Normaliza a saída para fornecer probabilidades de classificação.
- **Exemplo Analógico:**  
  Imagine uma fábrica onde os dados passam por diversas estações de trabalho, cada uma responsável por uma transformação específica até a obtenção do produto final (a predição).

- **Explicação:**  
  A rede neural possui duas camadas ocultas (com 64 e 32 unidades, respectivamente) e uma camada de saída com 2 nós para classificação. A função softmax no final normaliza as previsões para que possam ser interpretadas como probabilidades.

  - **Treinamento:**  
  Utiliza-se o otimizador Adam e a função de perda CrossEntropy para atualizar os pesos da rede ao longo de 20 épocas.
- **Avaliação:**  
  Após o treinamento, o desempenho é medido pela acurácia no conjunto de teste, comparando as predições com os valores reais.

