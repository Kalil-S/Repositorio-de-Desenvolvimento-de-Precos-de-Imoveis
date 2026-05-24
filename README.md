# Relatório Técnico Relatório Técnico - Precificação de Imóveis (Ames Housing)

## 1. Capa
* **Equipe:** Grupo G
* **Integrantes:**
  * Gabriel Abreu Cunha De Alencar - 2315097
  * Igor Gomes Ximenes -2217665
  * Kalil Smith Pinto Palheta - 2223857

* **Repositório:**
    * [Repositório de Submissão](https://github.com/Kalil-S/Repositorio-de-Submissao-de-Precos-de-Imoveis-.git)
    * [Repositório de Desenvolvimento](https://github.com/Kalil-S/Repositorio-de-Desenvolvimento-de-Precos-de-Imoveis.git)

---

## 2. Introdução
Este projeto detalha os procedimentos metodológicos, estatísticos e computacionais adotados no desenvolvimento de um modelo preditivo para a base de dados *Ames Housing*. O cerne do problema consistiu em estimar o valor de venda (`SalePrice`) de propriedades residenciais por intermédio de múltiplos atributos estruturais, espaciais e temporais. A resolução de problemas de regressão no contexto imobiliário demanda um tratamento rigoroso da alta dimensionalidade de características contínuas e categóricas.

Para fins de otimização paramétrica, a métrica fundamental estabelecida pela equipe foi o **RMSLE (Root Mean Squared Logarithmic Error)**, mas não deixando de atender as outra metricas registradas no arquivo "metricas_baseline.txt". A escolha dessa métrica justifica-se estatisticamente pois a avaliação do erro em escala logarítmica garante que a penalização incida sobre a proporção do desvio em relação ao valor intrínseco da propriedade, mitigando severas distorções na função de custo causadas por *outliers* naturais (casas de luxo com preços exponencialmente maiores).

---

## 3. Análise Exploratória de Dados (EDA)
A etapa de exploração visual permitiu identificar a estrutura latente dos dados e balizar as decisões de engenharia. 
* **Apresentação Visual:** Histogramas de densidade comprovaram que a distribuição da variável alvo (`SalePrice`) sofre de assimetria positiva substancial (*Right Skewness*), uma característica esperada em ativos financeiros. Gráficos de dispersão (*scatter plots*) evidenciaram a presença de propriedades com vasta área territorial, mas valores atípicos de venda, identificando *outliers* primários.
<img scr="https://github.com/Kalil-S/Repositorio-de-Desenvolvimento-de-Precos-de-Imoveis/blob/main/plots/eda_engineered_features.png" width="100%">

* **Identificação de Correlações Relevantes:** A matriz de correlação de Pearson destacou que atributos dimensionais globais e índices de qualidade construtiva ostentam as mais elevadas correlações lineares positivas e diretas com o preço. Variáveis fragmentadas ou esparsas isoladamente demonstraram baixo coeficiente de determinação explicativo.

---
