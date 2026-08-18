# 🛡️ Detecção de Anomalias em Transações Financeiras

Este projeto tem como objetivo desenvolver um modelo de Machine Learning capaz de identificar anomalias e potenciais fraudes em transações financeiras. O foco principal está no tratamento de dados altamente desbalanceados e na construção de um pipeline robusto de classificação.

---

## 📌 Conteúdos e Módulos do Projeto

### 1. Primeiros Passos no Projeto
- Análise exploratória dos dados de transações.
- Identificação da distribuição das classes (normais vs. anômalas).
- Limpeza e pré-processamento dos dados.

### 2. Avaliação e Técnicas de Balanceamento
- Aplicação da técnica de reamostragem **SMOTE** (*Synthetic Minority Over-sampling Technique*) para equilibrar a base de dados de treino.
- Definição de métricas prioritárias para dados desbalanceados (Precision, Recall e F1-Score) em vez de apenas Acurácia.

### 3. Modelos Avançados e Explicabilidade
- Treinamento do modelo **Random Forest Classifier** com parâmetro `class_weight='balanced'`.
- Avaliação e validação de desempenho no conjunto de teste.

---

## 📊 Resultados do Modelo (Random Forest)

Após a aplicação das técnicas de balanceamento e ajuste de hiperparâmetros, o modelo obteve os seguintes resultados no conjunto de teste:

| Classe | Precision | Recall | F1-Score | Support |
| :--- | :---: | :---: | :---: | :---: |
| **0 (Normal)** | 1.00 | 1.00 | 1.00 | 85.295 |
| **1 (Anomalia)** | **0.84** | **0.76** | **0.79** | 148 |
| **Accuracy** | | | **1.00** | 85.443 |

> **Destaque:** O modelo alcançou um **Recall de 0.76** e **Precision de 0.84** para a classe minoritária (fraude), garantindo uma taxa de detecção efetiva com um nível controlado de falsos positivos.

---

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python 3
* **Manipulação de Dados:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn (`RandomForestClassifier`, `classification_report`)
* **Balanceamento de Dados:** Imbalanced-learn (`SMOTE`)

---

## 📁 Como Executar o Projeto

1. Clone este repositório:
   ```bash
   git clone [https://github.com/seu-usuario/nome-do-repositorio.git](https://github.com/seu-usuario/nome-do-repositorio.git)
