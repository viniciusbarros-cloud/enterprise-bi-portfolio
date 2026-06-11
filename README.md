# Enterprise BI Portfolio: Do Dado Bruto ao Insight Estratégico 📊

Este repositório consolida meu portfólio de Business Intelligence e Visualização de Dados desenvolvidos ao longo da minha trajetória profissional. O foco principal destes projetos foi transformar bases de dados relacionais e planilhas corporativas complexas (Excel) em repositórios analíticos otimizados, utilizando modelagem dimensional e lógicas avançadas de negócio.

---

## 🚀 Projetos em Destaque 

### 1. Analytics de Produtividade e Compliance (Polícia Federal - CACs)
* **Escopo:** Painel gerencial focado no controle de processos regulatórios, concessões de CR e aquisições de armamentos.
* **Destaque Técnico:** Arquitetura multi-página com sistema avançado de navegação via botões (UX/UI), cálculo de SLA de atendimento (Tempo médio de análise) e distribuição percentual de desfechos.
* **Métricas-Chave:** Volume de Processos, Taxa de Deferimento/Indeferimento e Gargalos de Documentação.

### 2. Hub de Logística e Performance de Frota
* **Escopo:** Análise ponta a ponta de faturamento, margem de lucro e eficiência de entregas (% no Prazo) por tipo de veículo e rotas operacionais.
* **Destaque Técnico:** Implementação de Árvore de Decomposição para *drill-down* dinâmico de receita por marca/veículo e tratamento de dados temporais para cálculo de pontualidade.
* **Métricas-Chave:** Receita Total, Lucro Líquido, Km Rodados, Volumetria de Viagens e Taxa de SLA.


### 3. Engenharia Financeira & Fluxo de Caixa
* **Escopo:** Consolidação de entradas, saídas, despesas operacionais e saúde financeira corporativa.
* **Destaque Técnico:** Estruturação de gráfico de cascata (*Waterfall*) para tracking de variação de saldo mensal e cálculo matemático de margens reais.
* **Métricas-Chave:** Saldo Final, Margem de Lucro, Proporção de Despesas e Fluxo de Entradas/Saídas.

---

## 🛠️ Engenharia Oculta (O que está por trás dos Painéis)

Para que estes dashboards operassem com alta performance, foram aplicadas as seguintes premissas de Engenharia de Analytics:

* **Tratamento e ETL (Power Query):** Limpeza de dados brutos provenientes de planilhas isoladas, tipagem correta de dados, eliminação de redundâncias e criação de chaves substitutas para relacionamento.
* **Modelagem Dimensional (Star Schema):** Divisão clara entre tabelas Fato (vendas, contratações, processos) e tabelas Dimensão (calendário, clientes, veículos, produtos), evitando tabelas únicas infladas (*flat tables*).
* **Cálculos Avançados (DAX / Fórmulas):** Construção de medidas robustas para cálculos de acumulados no ano (YTD), médias móveis e percentuais de participação sobre o total.

---

## 📦 Outros Projetos Inclusos no Hub
* **RH Analytics:** Indicadores de turnover, folha salarial total e distribuição de headcount por cargo/área.
* **Dashboard de Produção:** Monitoramento de eficiência industrial (OEE simplificado), indicando horas produtivas vs. paradas e volume de rejeitos.

---
## 🚀 Portfólio de Projetos (Navegação Rápida)

Clique nos links abaixo para acessar o painel completo, a documentação técnica (DAX/SQL) e os detalhes de arquitetura de cada projeto corporativo:

* **[01. Setor Público & Compliance (CAC)](./01-public-sector-cac/)**
  * *Foco:* Gestão de SLAs, conformidade e navegação UX/UI avançada.
* **[02. Hub de Logística & Performance](./02-logistics-analytics/)**
  * *Foco:* Faturamento de fretes, controle de frota e Árvores de Decomposição.
* **[03. Engenharia Financeira & Fluxo de Caixa](./03-financial-cashflow/)**
  * *Foco:* Inteligência de tempo, saldos móveis acumulados e gráfico de cascata (*Waterfall*).
* **[04. Projetos Adicionais (People Analytics & Produção)](./04-projetos-adicionais/)**
  * *Foco:* Gestão de massa salarial (RH) e Eficiência Operacional/OEE (Manufatura).

---

## 📂 Estrutura do Repositório

Para facilitar a navegação e auditoria técnica, o projeto está estruturado de forma modular conforme o ecossistema abaixo:

```text
├── .github/                  # Imagens e prints dos dashboards
├── 01-public-sector-cac/     # Arquivo .pbix + Mini README
├── 02-logistics-analytics/    # Arquivo .pbix / Excel + Mini README
├── 03-financial-cashflow/    # Arquivo .pbix / Excel + Mini README
├── 04-additional-projects/   # Subpastas com outros projetos para RH, Produção, etc.
```
