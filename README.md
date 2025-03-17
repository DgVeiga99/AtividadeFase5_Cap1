# Previsão de Rendimento de Safra com Machine Learning

## Introdução
Este projeto consiste em duas partes principais: (1) a previsão de rendimento agrícola utilizando Machine Learning e (2) a análise de custos para hospedar a API na AWS. A seguir, detalhamos ambas as etapas do projeto, incluindo os resultados e justificativas das escolhas técnicas.

---

## Parte 1: Código Jupyter
### **Descrição do Projeto**
Este projeto tem como objetivo prever o rendimento agrícola de diferentes culturas com base em condições climáticas e do solo. 
Utilizando **Machine Learning**, aplicamos **métodos de regressão supervisionada** para realizar previsões precisas a partir dos dados fornecidos.

### **Dataset Utilizado**
O dataset **crop_yield.csv** contém os seguintes atributos:

- **Cultura**: Tipo de plantação.
- **Precipitação (mm/dia)**: Quantidade de chuva diária.
- **Umidade Específica (g/kg)** e **Umidade Relativa (%)**.
- **Temperatura (°C)**: Temperatura a 2 metros acima do solo.
- **Rendimento (kg/ha)**: Quantidade de colheita por hectare (variável alvo).

### **Tecnologias e Modelos Utilizados**
O projeto foi desenvolvido em **Python** utilizando as bibliotecas:
- `pandas`, `seaborn`, `matplotlib` para análise exploratória de dados.
- `scikit-learn` para modelagem preditiva.

#### **Modelos de Regressão Utilizados**
- **K-Nearest Neighbors (`KNeighborsRegressor`)** - Algoritmo baseado na proximidade entre pontos.
- **Regressão Linear (`LinearRegression`)** - Modelo base simples para regressão.
- **Suporte a Vetores (`SVR`)** - Modelo baseado em margens de suporte.
- **Árvore de Decisão (`DecisionTreeRegressor`)** - Algoritmo baseado em regras de decisão.
- **Random Forest (`RandomForestRegressor`)** - Conjunto de múltiplas árvores para previsões mais robustas.

### **Como Executar o Código**

#### **Estrutura do Repositório**
```
 FASE-05-PREVISÃO-SAFRA
│── crop_yield.csv                           # Base de dados original
│── DiegoVeiga_RM560658_Fase5_Cap1.ipynb     # Notebook Jupyter com código do projeto
│── README.md                                # Documentação do projeto
│── aws_estimativas/                         # Pasta contendo os arquivos de estimativa AWS
│   │── Estimativa_SP_Linux.pdf              # Estimativa de custos para São Paulo - Linux
│   │── Estimativa_SP_Windows.pdf            # Estimativa de custos para São Paulo - Windows
│   │── Estimativa_USA_Linux.pdf             # Estimativa de custos para Virgínia - Linux
│   │── Estimativa_USA_Windows.pdf           # Estimativa de custos para Virgínia - Windows
```
#### **Instalação das Dependências**
Certifique-se de ter instalado todas as bibliotecas necessárias:
```sh
pip install pandas seaborn matplotlib scikit-learn
```

#### **Executar no Jupyter Notebook**
```sh
jupyter notebook DiegoVeiga_RM560658_Fase5_Cap1.ipynb
```

### **Vídeo Demonstrativo**
O vídeo explicando a execução do código pode ser acessado no link abaixo:
[Vídeo da Parte 1](https://youtu.be/seu-video-aqui)

---

## Parte 2: Estimativa de Custos na AWS
### **Descrição**
Para hospedar a API e rodar o modelo de Machine Learning, realizamos uma estimativa de custos usando a **Calculadora de Preços da AWS**, comparando **São Paulo (BR) e Virgínia do Norte (EUA)** para **Linux e Windows**.

Os detalhes das estimativas podem ser encontrados nos arquivos dentro da pasta `aws_estimativas/`:
- [Estimativa SP - Linux](aws_estimativas/Estimativa_SP_Linux.pdf)
- [Estimativa SP - Windows](aws_estimativas/Estimativa_SP_Windows.pdf)
- [Estimativa USA - Linux](aws_estimativas/Estimativa_USA_Linux.pdf)
- [Estimativa USA - Windows](aws_estimativas/Estimativa_USA_Windows.pdf)

### **Resultados da Estimativa**
| Região | Sistema Operacional | Custo Mensal (USD) | Custo Anual (USD) |
|--------|---------------------|--------------------|--------------------|
| **São Paulo** | **Linux** | **34,14** | **409,68** |
| **São Paulo** | **Windows** | **71,23** | **854,76** |
| **Virgínia (EUA)** | **Linux** | **24,29** | **291,48** |
| **Virgínia (EUA)** | **Windows** | **60,42** | **725,04** |

### **Justificativa Técnica**
#### **Escolha ideal para menor custo:**
- **Região:** Virgínia do Norte (EUA)  
- **Sistema Operacional:** Linux  
- **Motivo:** Menor custo mensal e anual comparado a todas as outras opções.  

#### **Escolha ideal para conformidade com a LGPD:**
- **Região:** São Paulo (Brasil)  
- **Sistema Operacional:** Linux  
- **Motivo:** Exigência legal para armazenamento de dados no Brasil.

#### **Escolha alternativa para compatibilidade com sistemas específicos:**
- **Windows Server** deve ser escolhido apenas se houver necessidade específica de compatibilidade com aplicações que não rodam em Linux.

### **Vídeo Demonstrativo**
O vídeo explicando a análise de custos da AWS pode ser acessado no link abaixo:
[Vídeo da Parte 2](https://youtu.be/seu-video-aqui)
