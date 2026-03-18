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

#### Insights
### O dataset é composto por 29 ativos distribuídos entre NYSE/NASDAQ (18) e B3 (11), com leve predominância do mercado americano. Por setor, Tecnologia lidera com 15 ativos contra 14 do Financeiro — distribuição equilibrada que permite comparações justas entre os dois setores.

---

## 2. Retornos

Análise dos retornos acumulados e médios por mercado, incluindo a comparação entre melhores e piores ativos.

![Melhores/piores retornos e retorno médio por mercado](IMG/Retornos.png)

#### Insights
### A B3 superou a NYSE em retorno médio acumulado no período — 37.96% contra 32.78%. Os destaques individuais foram INTC (105%) e AMD (104%), impulsionados pelo boom de semicondutores. No lado brasileiro, Bradesco (93%) e BTG Pactual (89%) lideraram. O pior desempenho foi da Salesforce com -27% de retorno acumulado.

---

## 3. Tech BR x Tech USA

Comparação do retorno acumulado médio entre ativos de **Tecnologia** e **Financeiro** em B3 e NYSE/NASDAQ.

![Comparação Tech BR x Tech USA](IMG/TechBRXTechUSA.png)

#### Insights
### O setor Financeiro brasileiro liderou com retorno médio de 55.88%, impulsionado pela alta SELIC que favorece diretamente a rentabilidade dos bancos. Nos EUA, o setor de Tecnologia dominou com 40.25%, puxado por gigantes como NVIDIA e AMD. A maior diferença observada foi entre Tech BR (16.46%) e Tech USA (40.25%) — empresas tecnológicas brasileiras ainda são menos maduras e capitalizadas que suas concorrentes americanas, resultando em retornos significativamente menores. Conclusão: Brasil venceu no Financeiro, EUA venceu na Tecnologia.

---

## 4. Volatilidade e risco

Ranking dos ativos por nível de volatilidade anual, categorizando-os em diferentes faixas de risco.

![Volatilidade anual dos ativos](IMG/Volatilidade.png)

#### Insights
### A volatilidade mede a intensidade das oscilações de preços. Ambos os mercados registraram volatilidade anual média semelhante — B3 (36.38%) e NYSE/NASDAQ (36.33%) — ambos classificados na faixa de alta volatilidade (30-50%). O ativo mais volátil foi a Méliuz (CASH3.SA) com 75.17%, indicando que o investidor poderia ter visto seu patrimônio oscilar até 75% em um ano — risco extremamente alto. Um dos mais estáveis foi o Itaú (ITUB4.SA) com 27%, dentro da faixa moderada. O cruzamento mais relevante: a Tech BR concentrou a maior volatilidade do dataset com menor retorno — mais risco para menos resultado comparado à Tech americana.

---

## 5. Sharpe Ratio — Retorno Ajustado ao Risco

Análise da eficiência dos ativos — quanto de retorno cada um entregou por unidade de risco assumido.

![Sharpe Ratio dos ativos](IMG/ativos_por_risco.png)

#### Insights
### O Sharpe Ratio mede a eficiência de um ativo — o quanto de retorno ele entregou por unidade de risco assumido. A B3 se destacou com Sharpe médio de 1.16 contra 0.82 da NYSE, indicando que o mercado brasileiro recompensou melhor o risco no período. O grande destaque foi o Bradesco (BBDC4.SA) com Sharpe de 2.53 — considerado excelente, pois entregou alto retorno (93%) com volatilidade controlada, sendo o ativo mais eficiente do dataset. No extremo oposto, a Salesforce (CRM) registrou o pior Sharpe (-0.741) — além de cair 27%, ainda apresentou alta volatilidade, caracterizando o pior perfil risco-retorno da análise. O cruzamento mais relevante: Bradesco aparece consistentemente no topo em retorno, Sharpe e drawdown — confirmando ser o ativo mais equilibrado e eficiente do período analisado.

---

## 6. Liquidez: ativos líquidos x menos negociados

Análise do volume médio diário negociado para identificar ativos mais líquidos e menos negociados.

![Ativos líquidos x não negociáveis](IMG/Ativos_Liquidos_não_negociaveis.png)

#### Insights
### Liquidez mede a facilidade de comprar ou vender um ativo sem impactar seu preço — quanto maior o volume médio diário, mais líquido e negociável é o ativo. A NYSE dominou completamente o ranking de liquidez — NVIDIA liderou com 202 milhões de ações negociadas por dia, reflexo direto do boom de inteligência artificial. Os ativos brasileiros concentraram-se na base do ranking, com Méliuz, Intelbras e Positivo entre os menos negociados. Curiosamente, BlackRock (697 mil) foi o menos líquido do dataset mesmo sendo americano — ações de alto valor unitário tendem a ter menor volume em quantidade. Baixa liquidez representa risco adicional ao investidor: em momentos de crise, ativos pouco negociados são mais difíceis de vender rapidamente.

---

## 7. Drawdown máximo

Análise da maior queda que cada ativo sofreu do pico até o ponto mais baixo (drawdown máximo).

![Drawdown máximo dos ativos](IMG/drawdown.png)

#### Insights
### Drawdown é a maior queda que um ativo sofre do seu pico mais alto até o ponto mais baixo no período. A B3 registrou drawdown médio mais severo que a NYSE (-26.40% vs -24.81%). O ativo que mais sofreu foi a Méliuz (CASH3.SA) com -68.43% — combinado à sua alta volatilidade de 75%, representa o perfil de maior risco do dataset. Paradoxalmente, a B3 também abrigou os ativos mais resistentes — Bradesco (-10.08%), BTG Pactual (-10.22%) e Itaú (-13.01%) sofreram menos que qualquer ativo americano, demonstrando que o mercado brasileiro concentrou tanto os extremos de risco quanto de resiliência.

---

## 8. Beta vs S&P500

Classificação dos ativos como **defensivos** (beta < 1) ou **sensíveis** (beta > 1) ao índice S&P500.

![Beta dos ativos vs S&P500](IMG/beta.png)

#### Insights
### O beta mede a sensibilidade de um ativo em relação ao S&P500 — valores acima de 1 indicam ativos que se movem mais que o mercado americano (sensíveis), enquanto valores abaixo de 1 indicam ativos mais independentes (defensivos). A B3 apresentou beta médio de 0.46 — comportamento majoritariamente defensivo, pois os ativos brasileiros são mais influenciados por fatores locais como SELIC, câmbio e política do que pelo mercado americano. A NYSE registrou beta médio de 1.28, com AMD liderando (2.30) como o ativo mais sensível ao S&P500. O Banco do Brasil (BBAS3.SA) foi o mais defensivo com beta de 0.22 — praticamente independente do mercado americano.

---

## 9. Correlação entre os ativos

Matriz de correlação entre os retornos dos ativos para avaliar relacionamentos e possíveis oportunidades de diversificação.

![Correlação entre ativos](IMG/Correlacao.png)

#### Insights
### A correlação mede o quanto dois ativos se movem juntos — valores próximos de 1 indicam alta correlação, próximos de 0 indicam independência e negativos indicam movimentos opostos. Nenhum ativo do dataset ultrapassou correlação média de 0.46, indicando um conjunto bem diversificado. Os ativos mais correlacionados com o mercado geral foram Morgan Stanley (0.45) e Goldman Sachs (0.45) — bancos americanos que tendem a seguir o movimento do mercado como um todo. Os menos correlacionados foram TOTVS (0.22) e Oracle (0.22) — ativos com comportamento mais independente, ideais para compor carteiras diversificadas. A baixa correlação geral entre B3 e NYSE reforça que combinar ativos dos dois mercados reduz o risco total da carteira.