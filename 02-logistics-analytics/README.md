# 🚚 Hub de Logística e Performance de Frota

![Dashboard Logística Principal](image_26ef27.png)

## 📌 O Desafio de Negócio
Uma operação logística gera um volume massivo de dados transacionais diariamente (fretes, pedágios, combustíveis, tempos de pátio). O objetivo central deste projeto foi consolidar dados de faturamento de fretes, custos de manutenção, cubagem e rotas operacionais para responder à pergunta mais crítica da diretoria: **"Quais combinações de veículos, marcas e rotas trazem a maior margem líquida com o menor índice de atraso?"**

## 🏗️ Solução Analítica e Engenharia de Dados
Para suportar uma tomada de decisão rápida e performática, a seguinte arquitetura de modelagem foi desenvolvida no Power BI / Excel:

1. **Tratamento de Dados e ETL (Power Query):** * Saneamento e padronização de registros de texto (ex: placas de veículos e nomes de motoristas duplicados ou mal preenchidos).
   * Normalização de tabelas de custos operacionais e conversão de tipos de dados para evitar erros de arredondamento em valores monetários.
   * Criação de colunas calculadas de tempo para mensurar a diferença exata entre a data de entrega prevista e a real.

2. **Modelagem de Dados (Star Schema):**
   * **Tabela Fato (`fViagens`):** Centraliza as métricas aditivas e transacionais (Volume transportado, Valor do Frete, Custo de Combustível, Km Rodados).
   * **Tabelas Dimensão (`dVeiculos`, `dMotoristas`, `dRotas`, `dCalendario`):** Permitem a filtragem cruzada e o *slice-and-dice* dos dados por qualquer cenário de negócio.

3. **Métricas de Negócio Avançadas (DAX):**
   * **Margem de Lucro Real:** ```dax
     Margem Lucro % = DIVIDE([Receita Frete Total] - [Custo Operacional Total], [Receita Frete Total], 0)
     ```
   * **Percentual de SLA de Entrega:** Mede a eficiência de pontualidade da frota rodoviária.

---

## 💡 Engenharia de UX/UI: A Árvore de Decomposição
O grande destaque técnico e visual deste painel é a implementação da **Árvore de Decomposição (*Decomposition Tree*)**. 

![Análise Dinâmica](tree_26ef27.png)

Em vez de prender o usuário em relatórios estáticos, essa funcionalidade permite que o gestor clique no faturamento total e escolha dinamicamente por qual caminho quer quebrar o dado (ex: *Quero abrir o faturamento primeiro por Rota, depois ver qual Marca de caminhão rodou nela, e por fim qual veículo específico performou pior*). Isso reduz o tempo de descoberta de gargalos financeiros de horas para poucos cliques.
