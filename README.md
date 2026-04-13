# 📈 Previsão de Preços PETR4 com Machine Learning

Este projeto utiliza inteligência artificial para prever o preço de fechamento das ações da Petrobras (`PETR4`) para o dia seguinte. O objetivo é aplicar conceitos de **Análise de Séries Temporais** e **Regressão Linear** para identificar tendências no mercado financeiro.

## 🚀 Visão Geral
O modelo foi treinado com dados históricos reais coletados via API do Yahoo Finance. Para garantir a honestidade da previsão, aplicamos a técnica de *Lag* (deslocamento), onde o modelo usa as informações de hoje para tentar "adivinhar" o alvo de amanhã.

## 🛠️ Tecnologias Utilizadas

| Biblioteca | Função |
| :--- | :--- |
| **yfinance** | Extração de dados históricos da B3 |
| **Pandas** | Limpeza de dados e *Feature Engineering* |
| **Scikit-Learn** | Criação e avaliação do modelo de Machine Learning |
| **Matplotlib** | Geração de gráficos para análise visual |

## 🧠 Inteligência dos Dados (Features)
Para melhorar a precisão da Regressão Linear, criamos novos indicadores técnicos a partir dos preços base:

* **Média Móvel (7 dias):** Ajuda o modelo a entender a tendência da última semana.
* **Volatilidade (7 dias):** Calcula o risco baseado no desvio padrão dos preços recentes.
* **Alvo (Target):** Definido como o preço de fechamento do dia posterior ao registro atual.

## 📊 Resultados e Performance
O modelo apresentou uma excelente aderência aos preços reais, com as seguintes métricas de validação:

| Métrica | Valor Obtido |
| :--- | :--- |
| **MAE (Erro Médio Absoluto)** | R$ 0,73 |
| **MAPE (Erro Médio Percentual)** | 1,56% |

> **Nota:** O erro médio de apenas 1,56% demonstra que o modelo é capaz de acompanhar as flutuações da ação com alta fidelidade para previsões de curtíssimo prazo.