# 🏙️ São Paulo Real Estate — Análise e Modelagem Preditiva  
**Projeto didático de Machine Learning para previsão de preços de aluguel em São Paulo.**

---

## 📌 Descrição

Este projeto tem como objetivo ensinar, de maneira prática, os fundamentos de Machine Learning aplicados a dados reais do mercado imobiliário de São Paulo.  
A partir de um dataset público do Kaggle, realizamos:

- Análise exploratória (EDA)  
- Visualização geográfica  
- Tratamento de dados  
- Criação de features  
- Treino/teste  
- Avaliação por RMSE  
- Cross-Validation  
- Grid Search para otimização  

É um projeto introdutório, ideal como material de aula para ML supervisionado.

---

## 🗂️ Etapas do Projeto

### **1. Download Automático (KaggleHub)**
Os dados são baixados automaticamente via `kagglehub`:

- sem necessidade de baixar manualmente
- dataset sempre atualizado
- integração simples com notebooks

---

### **2. Análise Exploratória**
Inclui:

- `df.head()`, `df.info()`
- histogramas
- estatísticas descritivas
- análise de correlação
- distribuição por distrito e tipo de imóvel

---

### **3. Visualização Geográfica**
Criamos um mapa interativo com Plotly, mostrando:

- latitude e longitude  
- preço do aluguel  
- tamanho do imóvel  
- dispersão por regiões da cidade  

Esse passo ajuda a compreender padrões espaciais do mercado.

---

### **4. Limpeza e Preparação**
Processos aplicados:

- remoção de colunas constantes ou irrelevantes  
- filtragem apenas para imóveis de **aluguel**  
- tratamento de valores faltantes  
- transformação da variável `District` via **One-Hot Encoding**  
- separação entre features (X) e target (Y)

---

### **5. Split Treino/Teste**
Utilizamos `train_test_split` para garantir avaliação imparcial.

---

### **6. Modelagem**
Modelos testados:

- **Regressão Linear** (baseline, simples, explicativo)  
- **Decision Tree Regressor** (flexível, porém sujeito a overfitting)  
- **Random Forest Regressor** (melhor desempenho geral)

Os modelos foram avaliados usando:

- **Erro Quadrático Médio (MSE)**
- **Raiz do Erro Quadrático Médio (RMSE)**

Demonstrando:

- Linear → underfitting  
- Árvore → overfitting  
- Random Forest → melhor equilíbrio  

---

### **7. Validação Cruzada**
Aplicamos Cross-Validation (10 folds) para obter métricas mais robustas e evitar conclusões baseadas em um único split.

---

### **8. Hyperparameter Tuning**
Usamos `GridSearchCV` para testar combinações de hiperparâmetros do Random Forest:

- número de árvores (`n_estimators`)  
- número de features (`max_features`)  
- uso ou não de bootstrap  

O melhor modelo (`best_estimator_`) é usado para prever no conjunto de teste.

---

### **9. Avaliação Final**
Com o melhor modelo:

- cálculo do RMSE final  
- gráfico comparando valores reais vs previstos  
- análise do desempenho do modelo

---

## 📊 Tecnologias Utilizadas

- Python 3  
- Pandas  
- NumPy  
- Seaborn  
- Matplotlib  
- Plotly  
- Scikit-Learn  
- KaggleHub  

---