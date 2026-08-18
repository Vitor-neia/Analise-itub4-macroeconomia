# 📊 Análise de Desempenho e Indicadores - Itaú Unibanco (ITUB4)

## 🎯 Objetivo do Projeto
Este projeto é uma análise financeira aprofundada das ações do Itaú (ITUB4), estruturada para cobrir três pilares essenciais do mercado financeiro: **Análise Técnica**, **Rentabilidade Comparada** e **Análise Fundamentalista**. O objetivo é extrair insights acionáveis sobre o comportamento da ação no último ano, seu risco (volatilidade), sua performance contra a renda fixa e a saúde financeira da operação.

## 🛠️ Tecnologias e Bibliotecas Utilizadas
* **Python**
* **Manipulação de Dados:** Pandas, NumPy
* **Extração de Dados (APIs):** `yfinance` (B3/Yahoo Finance) e `bcb` (Banco Central do Brasil)
* **Visualização de Dados:** Plotly (Gráficos Interativos Financeiros), Seaborn e Matplotlib

## 📈 Estrutura da Análise

### 1. Análise Técnica e de Tendências
*   **Médias Móveis:** Aplicação de Médias Móveis Simples (SMA 20, 21 e 50) e Exponenciais (EMA 21, 50).
*   **Golden Cross e Death Cross:** Algoritmo para identificar cruzamentos matemáticos entre a SMA de 21 e 50 dias para sinalização de compra (tendência de alta) e venda (tendência de baixa).
    * *Insight:* Médias curtas geraram muitos ruídos no período. O ativo formou uma "Golden Cross" em nov/2025 resultando em forte alta, mas apresentou correção ao final do período.
*   **Bandas de Bollinger:** Mapeamento da volatilidade usando janela de 20 períodos e desvio padrão duplo. Evidenciação visual da expansão do "spread" nos períodos de maior turbulência.

### 2. Evolução de Patrimônio e Comparativo (ITUB4 vs. CDI)
*   **Simulação de Carteira:** Modelagem da evolução de um aporte inicial de R$ 4.000,00 ao longo de 1 ano. 
    * O capital chegou a registrar um ganho máximo de 44,7% (R$ 5.786), fechando o período em R$ 4.549 (+13,7%).
*   **Comparativo de Base 100:** Cruzamento do preço de fechamento do Itaú com a taxa diária do CDI (extraída via API do Banco Central) utilizando normalização na Base 100.
    * *Insight:* Apesar dos altos picos de valorização, no fechamento exato do período, o retorno acumulado do CDI (renda fixa) superou o da ação, mitigando a relação risco-retorno no curto prazo.

### 3. Análise Fundamentalista e Múltiplos
*   **Extração Contábil Automática:** Leitura automática de dados de DRE (Lucro Líquido) e Balanço Patrimonial (Patrimônio Líquido).
*   **Indicadores de Rentabilidade:** Cálculo do ROE (Retorno sobre Patrimônio Líquido), fechando em expressivos **21,93%**.
*   **Valuation (P/L e P/VP):** O P/L calculado em ~9,3x indica um preço justo, negociando com ágio no valor patrimonial, o que é condizente com a alta rentabilidade que o banco entrega.
*   **Dividendos:** Agrupamento e análise histórica do Dividend Yield dos últimos 5 anos.

## 🚀 Como Executar
1. Clone este repositório.
2. Instale as dependências: `pip install pandas numpy yfinance matplotlib seaborn plotly python-bcb`
3. Execute o notebook `analise_itub4.ipynb` em seu ambiente Jupyter.

---
*Projeto construído com base em dados reais do mercado financeiro para portfólio de Análise de Dados.*