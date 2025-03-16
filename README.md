# FASE-05 - Previsão de Rendimento de Safra

## **📌 Descrição do Projeto**
Este projeto visa a previsão do rendimento agrícola de uma fazenda de médio porte (200 hectares), utilizando **Machine Learning** e técnicas de análise de dados. 

Através do estudo das condições climáticas e de solo, realizamos:
- **Análise exploratória dos dados** para entender padrões e correlações.
- **Clusterização** para identificar agrupamentos e outliers nas amostras.
- **Modelagem preditiva** para estimar o rendimento da safra com diferentes algoritmos.

O objetivo é desenvolver um modelo robusto que ajude a fazenda a prever a produtividade das culturas e otimizar suas decisões agrícolas.

---

## **📂 Estrutura do Código**
O projeto está organizado conforme descrito abaixo:

### 1️⃣ **Importação de Bibliotecas**
- `pandas`, `seaborn`, `matplotlib` para manipulação e visualização dos dados.
- `scikit-learn` para pré-processamento, clusterização e modelos de Machine Learning.

### 2️⃣ **Carregamento do Dataset**
- O dataset `crop_yield.csv` contém as seguintes variáveis:
  - **Cultura**: Tipo de plantação.
  - **Precipitação (mm/dia)**: Quantidade de chuva diária.
  - **Umidade Específica (g/kg)** e **Umidade Relativa (%)**.
  - **Temperatura (°C)**.
  - **Rendimento (kg/ha)**: Quantidade de colheita por hectare.

### 3️⃣ **Análise Exploratória**
- Identificação de correlações entre variáveis.
- Visualizações para detectar padrões e possíveis anomalias.

### 4️⃣ **Clusterização**
- **K-Means**: Identificação de agrupamentos nas culturas.
- **DBSCAN**: Detecção de outliers.

### 5️⃣ **Modelagem Preditiva**
Foram testados **cinco modelos** para prever o rendimento agrícola:
- **Regressão Linear (`LinearRegression`)**
- **Árvore de Decisão (`DecisionTreeRegressor`)**
- **Random Forest (`RandomForestRegressor`)**
- **SVR - Máquina de Vetores de Suporte (`SVR`)**
- **Gradient Boosting (`GradientBoostingRegressor`)**

Os modelos foram avaliados utilizando as métricas:
- **MAE (Mean Absolute Error)** → Quanto menor, melhor.
- **MSE (Mean Squared Error)** → Penaliza erros maiores, menor é melhor.
- **R² (Coeficiente de Determinação)** → Indica o quão bem o modelo explica a variação da variável alvo (quanto mais próximo de 1, melhor).

---

## **📊 Resultados Obtidos**
Após a análise dos modelos, os resultados indicam que:
- O modelo **(melhor modelo identificado aqui)** teve a maior precisão.
- A clusterização revelou padrões interessantes nos rendimentos das culturas.
- A previsão pode auxiliar na **tomada de decisões agrícolas estratégicas**.

---

## **🚀 Como Executar o Código**
### **Pré-requisitos**
1. **Python 3.8+** instalado.
2. Instalar as dependências:
   ```sh
   pip install -r requirements.txt
   ```

### **Executar no Jupyter Notebook**
```sh
jupyter notebook DiegoVeiga_RM560658_Fase5_Cap1_Corrigido.ipynb
```

---

## **📹 Vídeo Demonstrativo**
O vídeo explicativo do projeto pode ser acessado [**neste link do YouTube**](#).

---

## **📁 Estrutura do Repositório**
```
📦 FASE-05-PREVISÃO-SAFRA
│── crop_yield.csv           # Base de dados original
│── DiegoVeiga_RM560658_Fase5_Cap1_Corrigido.ipynb  # Notebook corrigido com o código final
│── README.md                # Documentação do projeto
│── requirements.txt         # Lista de dependências para executar o código
```

---

Caso tenha dúvidas ou sugestões, entre em contato! 🚀
