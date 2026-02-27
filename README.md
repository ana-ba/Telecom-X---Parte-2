# Telecom X - Parte 2: Predição de Churn de Clientes

Este repositório contém a segunda etapa do projeto **Telecom X**, focada na aplicação de modelos de Machine Learning para prever a evasão de clientes (Churn). O objetivo é identificar padrões de comportamento que levam ao cancelamento e fornecer insights para estratégias de retenção.

---

## 📌 Propósito da Análise
O objetivo principal deste projeto é desenvolver um modelo preditivo de classificação capaz de antecipar quais clientes têm maior probabilidade de deixar a empresa. 

**Metas principais:**
* Analisar variáveis demográficas e de consumo.
* Prever o churn com base em dados históricos.
* Identificar os principais fatores que influenciam a decisão do cliente de cancelar o serviço.

---

## 📂 Estrutura do Projeto
A organização do repositório segue as boas práticas de Ciência de Dados:

* `notebooks/`: Contém o arquivo `telecom_x_parte2.ipynb` com todo o ciclo de vida do projeto.
* `data/`: Pasta destinada aos conjuntos de dados.
    * `churn_treated.csv`: Base de dados após limpeza e engenharia de recursos.
* `visuals/`: Prints e gráficos gerados durante a Análise Exploratória (EDA).
* `README.md`: Documentação do projeto.

---

## 🛠️ Preparação dos Dados
Para garantir a eficiência dos algoritmos, o processo de preparação incluiu:

1.  **Classificação de Variáveis:**
    * **Quantitativas:** Tenure (meses de contrato), MonthlyCharges e TotalCharges.
    * **Qualitativas:** Gênero, SeniorCitizen, Dependents, MultipleLines, InternetService, OnlineSecurity, etc.
2.  **Codificação (Encoding):** Transformação de variáveis categóricas em numéricas através de técnicas como *One-Hot Encoding* e *Label Encoding*.
3.  **Normalização:** Ajuste de escala das variáveis numéricas para evitar que valores de diferentes grandezas (ex: meses vs. reais) afetem o peso do modelo.
4.  **Divisão de Dados:** Separação da base em conjuntos de **Treino (80%)** e **Teste (20%)** para validação da performance.

---

## 📊 Insights e EDA
Durante a Análise Exploratória de Dados, destacaram-se os seguintes pontos:
* **Contratos Mensais:** Clientes com contratos de renovação mês a mês possuem a maior taxa de churn.
* **Serviços de Fibra Óptica:** Apresentam uma correlação alta com o cancelamento, sugerindo possíveis problemas de custo ou estabilidade percebida.
* **Inadimplência:** Clientes que utilizam boleto eletrônico (Paperless Billing) tendem a sair mais do que aqueles em débito automático.

---

## ⚖️ Justificativas de Modelagem
A escolha do modelo foi baseada no equilíbrio entre **precisão** e **interpretabilidade**. Optou-se por modelos de classificação que permitem extrair a "Importância das Variáveis" (Feature Importance), essencial para que o time de negócios entenda o *porquê* da previsão e não apenas o resultado final.

---

## 🚀 Como Executar o Notebook

### 1. Pré-requisitos
É necessário ter o Python instalado. Recomenda-se o uso do ambiente **Anaconda** ou **VS Code** com a extensão Jupyter.

### 2. Instalação de Dependências
No terminal, instale as bibliotecas necessárias:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
