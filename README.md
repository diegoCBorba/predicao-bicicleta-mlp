# **Predição do Uso de Bicicletas com Redes Neurais MLP**

Este projeto tem como objetivo prever a quantidade de bicicletas alugadas em um sistema de compartilhamento de bicicletas utilizando uma **rede neural MLP (Multilayer Perceptron)**. O modelo foi treinado com base em variáveis como condições climáticas, hora do dia, dia da semana e outras informações relevantes.

---

## **Descrição do Problema**

O problema consiste em prever o número total de bicicletas alugadas (`cnt`) em uma estação específica e em um horário específico. Trata-se de um **problema de regressão**, onde o modelo deve aprender a relação entre as variáveis preditoras e a variável alvo.

O conjunto de dados utilizado é o **Bike Sharing Dataset**, que contém registros horários de aluguel de bicicletas em Washington, D.C., durante os anos de 2011 e 2012.

---

## **Dados**

O dataset contém as seguintes variáveis:

- **Variáveis Temporais**: Hora do dia, dia da semana, mês, ano.
- **Variáveis Climáticas**: Temperatura, umidade, velocidade do vento, condições climáticas.
- **Variáveis Categóricas**: Estação do ano, tipo de dia (dia útil ou fim de semana/feriado).
- **Variável Alvo**: Número total de bicicletas alugadas (`cnt`).

O dataset pode ser baixado [aqui](https://archive.ics.uci.edu/ml/datasets/Bike+Sharing+Dataset).

---

## **Etapas do Projeto**

1. **Pré-processamento dos Dados**:
   - Remoção de colunas desnecessárias.
   - Codificação de variáveis categóricas (one-hot encoding).
   - Normalização de variáveis numéricas.
   - Divisão dos dados em conjuntos de treino (80%) e teste (20%).

2. **Construção da Rede Neural MLP**:
   - Arquitetura: 2 camadas ocultas com 64 e 32 neurônios, respectivamente.
   - Funções de ativação: ReLU para as camadas ocultas e linear para a camada de saída.
   - Função de perda: Mean Squared Error (MSE).
   - Otimizador: Adam.

3. **Treinamento do Modelo**:
   - Treinamento por 50 épocas com batch size de 32.
   - Uso de validação (20% dos dados de treino) para monitorar o desempenho.
   - Ajuste de hiperparâmetros e uso de callbacks (early stopping e model checkpoint).

4. **Avaliação do Modelo**:
   - Métricas calculadas no conjunto de teste:
     - **MAE (Erro Médio Absoluto)**: 0.1730
     - **MSE (Erro Quadrático Médio)**: 0.0622
     - **RMSE (Raiz do Erro Quadrático Médio)**: 0.2494
     - **R² (Coeficiente de Determinação)**: 0.94

---

## **Resultados**

O modelo obteve um **R² de 0.94**, indicando que ele explica 94% da variância dos dados. As métricas de erro (MAE e RMSE) sugerem que o modelo tem um bom desempenho, mas ainda há espaço para melhorias, especialmente na redução de erros maiores.

### **Métricas Finais**:
| Métrica | Valor |
|---------|-------|
| MAE     | 0.1730 |
| MSE     | 0.0622 |
| RMSE    | 0.2494 |
| R²      | 0.94  |

---

## **Como Reproduzir o Projeto**

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/seu-usuario/nome-do-repositorio.git
   cd nome-do-repositorio
   ```

2. **Instale as dependências**:
   Certifique-se de ter as bibliotecas necessárias instaladas:
   ```bash
   pip install pandas numpy scikit-learn tensorflow matplotlib
   ```
4. **Execute o código**:
   - O código está dividido em etapas no arquivo `projeto_bicicletas.ipynb` (ou `.py`).
   - Execute o Jupyter Notebook ou o script Python para reproduzir o projeto.

---

## **Melhorias Futuras**

- **Ajuste de Hiperparâmetros**: Testar diferentes arquiteturas de rede neural (número de camadas, neurônios, funções de ativação).
- **Engenharia de Features**: Criar novas variáveis ou transformar as existentes para melhorar a capacidade do modelo.
- **Regularização**: Adicionar técnicas como dropout ou L2 regularization para evitar overfitting.
- **Análise de Outliers**: Identificar e tratar outliers que possam estar afetando as previsões.

---

## **Referências**

- [Bike Sharing Dataset](https://archive.ics.uci.edu/ml/datasets/Bike+Sharing+Dataset)
- Documentação do [TensorFlow/Keras](https://www.tensorflow.org/api_docs)
- Documentação do [scikit-learn](https://scikit-learn.org/stable/)