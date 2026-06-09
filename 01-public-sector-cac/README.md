# ⚖️ Analytics de Produtividade e Compliance (Polícia Federal / SINARM)

<img src="download.gif" width="700">

## 📌 O Desafio de Negócio
No setor público e regulatório, o controle de processos, especialmente relacionados à aquisição de armamentos e registros (CACs), exige altíssima precisão e controle de prazos. O objetivo deste painel foi criar uma ferramenta de gestão à vista para monitorar o **fluxo de processos, gargalos operacionais e SLA de análise técnica**.

## 🏗️ Solução Analítica e Engenharia de Dados
O foco tecnológico deste projeto foi a contagem eficiente de transações e a modelagem de funil de status:

1. **Tratamento de Dados Categóricos:** 
   * Limpeza de bases governamentais e padronização dos status dos processos (Deferido, Indeferido, Em Análise, Exigência).
2. **Modelagem Temporal e SLA:**
   * Utilização avançada de inteligência de tempo para calcular o **Tempo Médio de Análise (Dias)** entre a entrada do protocolo e o despacho final, excluindo fins de semana/feriados.
3. **Sistema de Navegação:**
   * Arquitetura em múltiplas páginas interligadas por botões de navegação, simulando um aplicativo web completo e melhorando drasticamente a experiência do usuário (UX).

## 💡 Principais Métricas (KPIs)
* Volume total de processos por categoria (Aquisição, Transferência, Renovação).
* Taxa de Aprovação vs. Rejeição.
* Distribuição de processos estagnados aguardando documentação.
