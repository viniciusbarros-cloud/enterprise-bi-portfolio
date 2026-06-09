# 💰 Engenharia Financeira & Fluxo de Caixa

![Dashboard Financeiro]([COLE_O_LINK_DA_IMAGEM_AQUI])

## 📌 O Desafio de Negócio
Muitas empresas falham por não terem visibilidade clara de suas entradas e saídas. Este projeto substitui fluxos de caixa baseados em planilhas manuais por um modelo automatizado, capaz de mostrar a saúde financeira, despesas operacionais e margem de lucro de forma clara e auditável.

## 🏗️ Solução Analítica e Engenharia de Dados
Neste projeto, a dificuldade principal estava em lidar com lançamentos de naturalezas diferentes (créditos vs débitos) em um modelo dimensional:

1. **Modelagem de Plano de Contas:** 
   * Estruturação de uma tabela dimensão de `dPlanoContas` hierárquica (ex: Receitas > Operacionais > Vendas de Produto A), permitindo a consolidação financeira em diferentes níveis.
2. **ETL de Lançamentos:**
   * Transformação e normalização (*Unpivot*) de bases financeiras horizontalizadas para um formato tabular (Data, Conta, Valor, Tipo), otimizando o modelo para o motor do Power BI/Excel.
3. **Cálculos Financeiros (DAX):**
   * Lógicas de acumulação de saldo móvel (*Running Total*) para projetar o caixa disponível no final do mês.

## 💡 Destaque de Visualização
Implementação do **Gráfico de Cascata (*Waterfall*)**. Esta é a melhor prática de mercado para análise financeira, pois ilustra visualmente a ponte entre o saldo inicial e o saldo final, detalhando o impacto exato (positivo ou negativo) das receitas e de cada categoria de despesa ao longo do período analisado.
