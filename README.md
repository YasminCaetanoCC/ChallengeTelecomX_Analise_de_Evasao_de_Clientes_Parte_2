# 📉 Challenge Telecom X - Análise de Evasão de Clientes (Parte 2)

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit_learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C4C4C?style=for-the-badge&logo=seaborn&logoColor=white)

## 📌 Sobre o Projeto
Este repositório contém a **Parte 2** do desafio da **Telecom X** - Alura + Oracle Next Education (ONE), focado em desenvolver soluções de Machine Learning para prever e mitigar o *Churn* (Evasão de Clientes).

O objetivo principal deste projeto foi carregar uma base de dados crua de clientes de telecomunicações, tratá-la, realizar uma profunda Análise Exploratória de Dados (EDA) e construir modelos preditivos capazes de identificar quais clientes têm maior probabilidade de cancelar seus serviços. Ao final, o projeto propõe **estratégias de retenção acionáveis** baseadas nos insights extraídos da Inteligência Artificial.

## 🚀 Etapas do Projeto

O fluxo de trabalho foi dividido em 5 etapas principais:

1. **Extração e Transformação (Limpeza de Dados):**
   * Carregamento do arquivo JSON original.
   * Tratamento de valores nulos, vazios e inconsistentes.
   * Conversão de tipos de dados (ex: strings para numéricos).
   * Tradução de colunas e mapeamento de variáveis binárias (Yes/No para 1/0).

2. **Análise Exploratória de Dados (EDA):**
   * Identificação de desequilíbrio na variável alvo (~73% Ativos vs ~27% Cancelamentos).
   * Visualização da evasão por gênero, tipo de contrato, e método de pagamento.
   * Análise de correlação utilizando Boxplots para entender a relação entre o Tempo de Contrato/Gasto Total e a Evasão.

3. **Preparação para Machine Learning:**
   * Remoção de colunas de identificação irrelevantes (ID do Cliente).
   * Aplicação de **One-Hot Encoding** (`get_dummies`) para variáveis categóricas.
   * **Padronização** de variáveis numéricas contínuas utilizando o `StandardScaler` para garantir o bom funcionamento dos algoritmos de distâncias.

4. **Modelagem Preditiva:**
   * Separação dos dados em Treino (70%) e Teste (30%) com estratificação.
   * Treinamento e avaliação de dois algoritmos:
     * **Regressão Logística** (Modelo escolhido pela alta interpretabilidade e ótimo equilíbrio de *Recall* sem apresentar *overfitting*).
     * **Random Forest** (Ajustado com `max_depth` para controle de *overfitting*).
   * Avaliação via Acurácia, Relatório de Classificação e Matrizes de Confusão.

5. **Análise de Importância e Relatório Estratégico:**
   * Extração de "Feature Importance" (Impureza da Árvore) e Coeficientes Lineares.
   * Criação de um relatório de negócios listando os principais ofensores do Churn e planos de ação recomendados.

## 📊 Principais Descobertas (Insights)

Através dos modelos, descobrimos que os maiores motivadores de evasão na Telecom X são:
* **Tipo de Contrato:** Clientes em contratos mensais (sem barreira de saída) são os maiores ofensores.
* **Tempo de Contrato:** O risco de evasão é crítico nos primeiros 6 meses.
* **Fibra Óptica:** Alta taxa de cancelamento neste serviço específico (indicando problemas técnicos ou de precificação).
* **Fatores Financeiros:** Mensalidades altas aliadas ao pagamento manual (Cheque Eletrônico) geram alto atrito e cancelamento.

---
Desenvolvido por Yasmin Caetano

Projeto desenvolvido para fins acadêmicos.
