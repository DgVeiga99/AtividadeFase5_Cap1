# Previsão de Rendimento de Safra com Machine Learning

## Descrição do Projeto
Este projeto tem como objetivo prever o rendimento agrícola de diferentes culturas com base em condições climáticas e do solo. 
Utilizando **Machine Learning**, aplicamos **métodos de regressão supervisionada** para realizar previsões precisas a partir dos dados fornecidos.

## Dataset Utilizado
O dataset **crop_yield.csv** contém os seguintes atributos:

- **Cultura**: Tipo de plantação.
- **Precipitação (mm/dia)**: Quantidade de chuva diária.
- **Umidade Específica (g/kg)** e **Umidade Relativa (%)**.
- **Temperatura (°C)**: Temperatura a 2 metros acima do solo.
- **Rendimento (kg/ha)**: Quantidade de colheita por hectare (variável alvo).

## Tecnologias e Modelos Utilizados
O projeto foi desenvolvido em **Python** utilizando as bibliotecas:
- `pandas`, `seaborn`, `matplotlib` para análise exploratória de dados.
- `scikit-learn` para modelagem preditiva.

### **Modelos de Regressão Utilizados**
- **K-Nearest Neighbors (`KNeighborsRegressor`)** - Algoritmo baseado na proximidade entre pontos.
- **Regressão Linear (`LinearRegression`)** - Modelo base simples para regressão.
- **Suporte a Vetores (`SVR`)** - Modelo baseado em margens de suporte.
- **Árvore de Decisão (`DecisionTreeRegressor`)** - Algoritmo baseado em regras de decisão.
- **Random Forest (`RandomForestRegressor`)** - Conjunto de múltiplas árvores para previsões mais robustas.

## Etapas do Processo
 **Pré-processamento dos dados**:  
- Tratamento de valores ausentes e dados duplicados.  
- Normalização das variáveis preditoras com `MinMaxScaler()`.  

 **Exploração dos dados**:  
- Análise estatística e visualização com `seaborn` e `matplotlib`.  
- Matriz de correlação para identificar relações entre variáveis.  

 **Treinamento dos Modelos**:  
- Separação do dataset em treino (30%) e teste (30%).  
- Aplicação dos modelos de Machine Learning.  

 **Avaliação dos Modelos**:  
Os modelos foram avaliados usando as métricas:
- **Erro Absoluto Médio (`MAE`)**: Média da diferença entre os valores reais e previstos.
- **Erro Quadrático Médio (`MSE`)**: Penaliza erros maiores para melhorar previsões.
- **Coeficiente de Determinação (`R²`)**: Mede o quão bem o modelo explica a variabilidade dos dados.

## Como Executar o Código

### Estrutura do Repositório
```
 FASE-05-PREVISÃO-SAFRA
│── crop_yield.csv                           # Base de dados original
│── DiegoVeiga_RM560658_Fase5_Cap1.ipynb     # Notebook Jupyter com código do projeto
│── README.md                                # Documentação do projeto
```
### **Instalação das Dependências**
Certifique-se de ter instalado todas as bibliotecas necessárias:
```sh
pip install pandas seaborn matplotlib scikit-learn
```

### **Executar no Jupyter Notebook**
```sh
jupyter notebook DiegoVeiga_RM560658_Fase5_Cap1.ipynb
```

## Vídeo Demonstrativo
O vídeo explicando a execução do projeto pode ser acessado no link abaixo:


