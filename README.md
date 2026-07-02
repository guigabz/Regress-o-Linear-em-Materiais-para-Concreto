# 🧱 Previsão de Resistência à Compressão do Concreto

Este projeto utiliza técnicas de **Machine Learning** (Aprendizado de Máquina) para prever a resistência à compressão do concreto (em MPa) com base na sua composição química e tempo de cura. 

O objetivo é criar um modelo preditivo capaz de otimizar traços de concreto, reduzindo custos e ensaios laboratoriais demorados.

---

## 📊 Sobre o Dataset

O conjunto de dados utilizado simula o famoso *Concrete Compressive Strength Dataset* (UCI Machine Learning Repository). Ele contém as seguintes características (features):

*   **Cement** (Cimento) - $kg/m^3$
*   **Blast Furnace Slag** (Escória de Alto Forno) - $kg/m^3$
*   **Fly Ash** (Cinza Volante) - $kg/m^3$
*   **Water** (Água) - $kg/m^3$
*   **Superplasticizer** (Superplastificante) - $kg/m^3$
*   **Coarse Aggregate** (Agregado Graúdo) - $kg/m^3$
*   **Fine Aggregate** (Agregado Miúdo) - $kg/m^3$
*   **Age** (Idade/Tempo de cura) - Dias
*   **Concrete compressive strength** (Variável Alvo) - MPa

---

## 🛠️ Tecnologias e Bibliotecas Utilizadas

*   **Python 3**
*   **Pandas & NumPy**: Manipulação e análise de dados.
*   **Matplotlib & Seaborn**: Visualização de dados e gráficos estatísticos.
*   **Scikit-Learn**: Divisão dos dados, treinamento dos modelos e avaliação de métricas.

---

## 🚀 Estrutura do Projeto

O pipeline do projeto foi desenvolvido em um Jupyter Notebook (Google Colab) e dividido nas seguintes etapas:

1.  **Análise Exploratória de Dados (EDA)**: Visualização de distribuições, detecção de outliers e análise de correlação entre os componentes.
2.  **Engenharia de Recursos (Feature Engineering)**: Criação de categorias de resistência para análises secundárias.
3.  **Pré-processamento**: Divisão do dataset em conjuntos de treino (80%) e teste (20%).
4.  **Treinamento de Modelos**: Implantação e ajuste de dois algoritmos:
    *   *Regressão Linear* (Baseline)
    *   *Random Forest Regressor* (Modelo Não-Linear)
5.  **Avaliação**: Comparação dos modelos utilizando as métricas **$R^2$ Score** (Coeficiente de Determinação) e **MAE** (Erro Médio Absoluto).

---

## 📈 Resultados Otimizados

Após o treinamento, os modelos apresentaram os seguintes desempenhos no conjunto de teste:

| Modelo | $R^2$ Score (Precisão) | MAE (Erro Médio Absoluto) |
| :--- | :---: | :---: |
| **Regressão Linear** | ~0.61 | ~8.2 MPa |
| **Random Forest** | **~0.90** | **~3.5 MPa** |

> 💡 **Conclusão:** O modelo de **Random Forest** apresentou um desempenho significativamente superior, capturando com precisão as relações não-lineares e interações complexas entre os componentes químicos do concreto.
