# 🚚 Hub de Logística e Performance de Frota

![Dashboard Logística]([COLE_O_LINK_DA_IMAGEM_AQUI])

## 📌 O Desafio de Negócio
Uma operação logística gera um volume massivo de dados diariamente. 
O objetivo deste projeto foi consolidar dados de fretes, custos de manutenção, rotas e performance de entrega para responder à pergunta central: **"Quais veículos e rotas estão gerando o maior retorno financeiro com a melhor pontualidade?"**

## 🏗️ Solução Analítica e Engenharia de Dados
Para suportar o painel, a seguinte arquitetura de dados foi desenvolvida:

1. **Extração e Limpeza (ETL):** 
   * Tratamento de inconsistências nos registros de placas e motoristas.
   * Padronização das datas de saída e entrega para cálculo preciso do SLA (*Service Level Agreement*).
2. **Modelagem de Dados (Star Schema):**
   * Criação da tabela Fato (`fViagens`) contendo métricas aditivas (custo, receita, distância).
   * Criação das tabelas Dimensão (`dVeiculo`, `dMotorista`, `dRota`, `dCalendario`) para permitir a filtragem e o slice-and-dice da informação.
3. **Métricas Avançadas (DAX):**
   * Cálculo de **Margem de Lucro (%):** `DIVIDE([Receita Total] - [Custo Total], [Receita Total])`
   * Cálculo de **Eficiência de Entrega (% no Prazo):** Lógica condicional comparando `Data Entrega Real` vs `Data Entrega Prevista`.

## 💡 Destaque de UX/UI
O principal diferencial deste painel é o uso da **Árvore de Decomposição (*Decomposition Tree*)**. Ela permite que o usuário gerencial faça um "drill-down" interativo, abrindo a Receita Total em quebras sucessivas por Marca do Veículo, Placa e Rota, facilitando a identificação imediata de gargalos ou anomalias financeiras.
