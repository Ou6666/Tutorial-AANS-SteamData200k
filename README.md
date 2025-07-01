# Tutorial 2: Aprendizagem Não Supervisionada - Construção de um Sistema de Recomendação


**Dataset:** Steam Video Games (steam-200k.csv)

---

Este repositório contém o trabalho desenvolvido para o **Tutorial 2** da disciplina de Aprendizagem Não Supervisionada. O objetivo principal é explorar a aplicação de diversas técnicas de Aprendizagem Não Supervisionada (AANS) para analisar dados de interação de utilizadores com videojogos e extrair insights que possam informar a construção de um sistema de recomendação.

**O projeto completo, com todo o código, análises detalhadas, visualizações e conclusões, está documentado no Jupyter Notebook:**

* **`Tutorial_2_AANS_steam200k.ipynb`**

---

## Estrutura do Projeto (Conteúdo do Notebook)

O notebook aborda as seguintes etapas e técnicas:

1.  **Introdução:** Contexto do dataset (Steam Video Games), objetivos do tutorial e análise inicial das features.
2.  **Carregamento e Limpeza Inicial dos Dados:** Processamento inicial do dataset.
3.  **Análise Exploratória de Dados (EDA):** Entendimento das distribuições de horas jogadas, jogos e utilizadores mais populares.
4.  **Transformação e Preparação dos Dados:** Criação da matriz Utilizador-Jogo e dados transacionais para Apriori.
5.  **Deteção de Outliers:**
    * Padronização dos Dados (`StandardScaler`).
    * Aplicação e Comparação de **Isolation Forest** e **Local Outlier Factor (LOF)**.
    * Visualização dos outliers via **PCA** e **UMAP**.
6.  **Redução de Dimensionalidade com PCA:** Análise da variância explicada e aplicação do PCA para preparar dados para SOM/K-Means.
7.  **Mapas Auto-Organizáveis (SOM):**
    * Treino do SOM com input original (padronizado) e com input reduzido por PCA.
    * Análise de U-Matrix, Mapa de Densidade e Erro de Quantização.
    * **Comparação detalhada da eficácia do SOM com e sem PCA.**
8.  **Mineração de Regras de Associação (Apriori):**
    * Preparação de dados transacionais de compras.
    * Geração e análise de regras de associação (Antecedentes -> Consequentes) com base em `support`, `confidence` e `lift`.
    * Exemplo conceptual de recomendação baseada em regras.
9.  **Clustering com K-Means:**
    * Determinação do número ótimo de clusters (`k`) usando o Método do Cotovelo.
    * Aplicação do K-Means aos dados reduzidos por PCA.
    * Visualização dos clusters K-Means via UMAP.
    * **Comparação entre K-Means e SOM (PCA+SOM) para a tarefa de segmentação de utilizadores.**
10. **Tabela Comparativa Final das Técnicas AANS Aplicadas:** Resumo das forças, limitações e utilidade de cada técnica para um sistema de recomendação.
11. **Conclusão Geral:** Sumário dos principais achados e impacto na construção de sistemas de recomendação.

---

## Como Executar o Notebook

Para replicar os resultados e explorar o notebook:

1.  **Clone este repositório:**
    ```bash
    git clone <URL_DO_SEU_REPOSITORIO>
    ```
    
2.  **Navegue até a pasta do projeto:**
    ```bash
    cd Tutorial_2_AANS_steam200k (1)/archive
    ```
3.  **Instale as dependências necessárias:**
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn umap-learn minisom mlxtend
    ```
4.  **Certifique-se de que o dataset `steam-200k.csv` está na mesma pasta que o notebook.**
5.  **Abra o Jupyter Notebook:**
    ```bash
    jupyter notebook Tutorial_2_AANS_steam200k.ipynb
    ```

Isso abrirá o Jupyter na sua máquina, permitindo que você execute cada célula do notebook sequencialmente.
