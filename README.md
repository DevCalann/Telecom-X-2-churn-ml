# 📊 Telecom X - Parte 2: Previsão de Evasão de Clientes (Churn)

## 🎯 Propósito do Projeto

Este projeto tem como objetivo principal **prever a evasão de clientes (churn)** em uma empresa de telecomunicações, utilizando técnicas de **machine learning**. A partir da análise de variáveis comportamentais e financeiras, buscamos identificar **fatores determinantes** na saída de clientes, além de propor **estratégias de retenção**.

---

## 🔧 Preparação e Limpeza dos Dados

### ✅ Classificação das Variáveis
- **Categóricas**: Gender, PaymentMethod, Contract, InternetService, entre outras.
- **Numéricas**: tenure, Charges.Monthly, Charges.Total.

### 🔄 Etapas de Pré-processamento
1. **One-hot Encoding**: Aplicado às variáveis categóricas para torná-las numéricas.
2. **Normalização**: Realizada com `StandardScaler` nas variáveis após balanceamento.
3. **Balanceamento de Classes**: Utilização do **SMOTE** para lidar com desbalanceamento no target `ChurnStatus`.
4. **Split dos Dados**: Divisão em **80% treino** e **20% teste**, com estratificação.

---

## 🧠 Modelagem e Justificativas

### Modelos Treinados
- **Regressão Logística**: Modelo linear interpretável, utilizado como benchmark.
- **Random Forest**: Modelo de árvore com bom desempenho em dados tabulares, robusto a outliers e capaz de capturar não-linearidades.

> As escolhas foram motivadas pela **busca de equilíbrio entre performance e interpretabilidade**.

---

## 📈 Análise Exploratória (EDA) e Insights

### Exemplos de Gráficos Produzidos
- 📊 **Distribuição de Churn**: Evidenciou desbalanceamento inicial.
- 🔥 **Heatmap de Correlação**: Indicou correlação negativa entre `tenure` e churn.
- 📉 **Boxplots**:
  - Clientes com **menor tenure** tendem a evadir mais.
  - Faturas mensais e gastos totais **altos** estão relacionados ao churn.

### Fatores-chave identificados:
- Contrato mensal aumenta chance de churn.
- Ausência de suporte técnico e segurança online contribuem negativamente.
- Métodos de pagamento eletrônico apresentam mais evasão.

---

## 🖥️ Execução do Projeto

### Passos para Executar o Notebook
1. Clone o repositório:
```bash
git clone https://github.com/DevCalann/Telecom-X-2-churn-ml.git
cd Telecom-X-2-churn-ml
```

2. Instale as bibliotecas necessárias:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
```

3. Execute o notebook:
- Abra `notebook_telecom_x2.ipynb` com Jupyter Notebook, Google Colab ou VSCode.

---

## 💡 Conclusões e Estratégias

Com base nos modelos e variáveis mais influentes, foram propostas **ações práticas para retenção**, como:
- Incentivar contratos longos.
- Reduzir custos para clientes com alto gasto.
- Melhorar suporte e serviços adicionais.

> O projeto demonstrou que **modelos preditivos são ferramentas viáveis e eficientes** na **tomada de decisão comercial estratégica**.

---

## 🤝 Contribuição
Este projeto foi desenvolvido como parte do curso **Formação Cientista de Dados** da **Alura|ONE**, com foco em análise prática, modelagem e entrega de valor por meio de dados.

---
