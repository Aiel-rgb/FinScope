## FinScope – Painel de Análise de Ativos

Projeto de análise exploratória de ações brasileiras (B3) e americanas (NYSE/NASDAQ) com foco em retorno, risco e liquidez.

- **Linguagem**: Python  
- **Principais libs**: `pandas`, `numpy`, `yfinance`, `matplotlib`, `seaborn`  
- **Fonte de dados**: preços históricos via `yfinance` consolidados no CSV `CSV/acoes_analise.csv`

---

## Objetivo do projeto

- **Mapear** a distribuição dos ativos por setor e mercado.  
- **Avaliar** retornos acumulados e recentes.  
- **Comparar** desempenho de tecnologia x financeiro no Brasil e nos EUA.  
- **Mensurar** volatilidade, drawdown, risco (beta) e liquidez dos ativos.  
- **Explorar** correlação entre os ativos para apoiar decisões de diversificação.

---

## 1. Setores e mercados

Análise da distribuição dos ativos entre **B3** e **NYSE/NASDAQ** e entre os setores **Tecnologia** e **Financeiro**.

![Distribuição de tickers por mercado e setor](IMG/Distribuicao_tickers.png)

---

## 2. Retornos

Análise dos retornos acumulados e médios por mercado, incluindo a comparação entre melhores e piores ativos.

![Melhores/piores retornos e retorno médio por mercado](IMG/Retornos.png)

---

## 3. Tech BR x Tech USA

Comparação do retorno acumulado médio entre ativos de **Tecnologia** e **Financeiro** em B3 e NYSE/NASDAQ.

![Comparação Tech BR x Tech USA](IMG/TechBRXTechUSA.png)

---

## 4. Volatilidade e risco

Ranking dos ativos por nível de volatilidade anual, categorizando-os em diferentes faixas de risco.

![Volatilidade anual dos ativos](IMG/Volatilidade.png)

---

## 5. Classificação por risco (volatilidade)

Comparação dos ativos agrupados por faixas de risco / volatilidade.

![Ativos por faixa de risco](IMG/ativos_por_risco.png)

---

## 6. Liquidez: ativos líquidos x menos negociados

Análise do volume médio diário negociado para identificar ativos mais líquidos e menos negociados.

![Ativos líquidos x não negociáveis](IMG/Ativos_Liquidos_não_negociaveis.png)

---

## 7. Drawdown máximo

Análise da maior queda que cada ativo sofreu do pico até o ponto mais baixo (drawdown máximo).

![Drawdown máximo dos ativos](IMG/drawdown.png)

---

## 8. Beta vs S&P500

Classificação dos ativos como **defensivos** (beta < 1) ou **sensíveis** (beta > 1) ao índice S&P500.

![Beta dos ativos vs S&P500](IMG/beta.png)

---

## 9. Correlação entre os ativos

Matriz de correlação entre os retornos dos ativos para avaliar relacionamentos e possíveis oportunidades de diversificação.

![Correlação entre ativos](IMG/Correlacao.png)

---

## insights:


