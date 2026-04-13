# Desafio-Dio-NotebookLM

Este repositório contém o Caderno Temático desenvolvido como parte do desafio da DIO, explorando o uso do NotebookLM como ferramenta de aprendizagem ativa e curadoria de conhecimento.

## 🎯 Contexto e Objetivos

A transformação de dados brutos em informações visuais é fundamental para a otimização de serviços. No ambiente de Tecnologia da Informação, o acompanhamento de métricas operacionais permite uma gestão proativa. Este projeto tem como objetivo criar um assistente virtual focado na construção e automação de dashboards (utilizando Power BI e Looker Studio) e na extração de dados através de automações (como Google Apps Script).

**Objetivos de Estudo:**
- Estruturar a modelagem de dados para painéis de indicadores de TI.
- Compreender as melhores práticas de extração, tratamento e automação de fontes de dados.
- Aplicar princípios de Data Storytelling para destacar KPIs críticos de operação.

## 📚 Curadoria de Fontes

Para treinar o assistente no NotebookLM, foram utilizados os seguintes materiais de referência:

1. [Métricas e KPIs de ITSM para Service Desk (Atlassian)](https://www.atlassian.com/br/itsm/service-request-management/kpis) - *Foco em regras de negócios e indicadores como MTTR e SLA.*
2. [Guias do Google Apps Script para Planilhas (Google Developers)](https://developers.google.com/apps-script/guides/sheets?hl=pt-br) - *Foco na automação da inserção de dados.*
3. [Conectar ao Planilhas Google no Looker Studio (Ajuda do Google)](https://support.google.com/looker-studio/answer/6285986?hl=pt) - *Foco em arquitetura de conexão.*
4. [Dicas para criar um ótimo dashboard (Microsoft Learn)](https://learn.microsoft.com/pt-br/power-bi/create-reports/service-dashboards-design-tips) - *Foco em design visual e performance.*
5. [O que é Data Storytelling? (Tableau)](https://www.tableau.com/pt-br/learn/articles/data-storytelling) - *Foco em UX e apresentação de resultados.*

## 🛠️ Engenharia de Prompts e "Cicatrizes"

Durante o desenvolvimento do assistente, testei diferentes abordagens para extrair as respostas mais técnicas e precisas. Abaixo estão os registros dessa interação (troubleshooting):

**Tentativa 1: Automação de Dados**
- **Prompt enviado:** "Como faço para automatizar uma planilha que recebe dados de chamados de TI?"
- **Resposta da IA:** (Resumo rápido sugerindo o uso de macros e integrações básicas).
- **Cicatriz (O que aprendi/ajustei):** O prompt foi muito genérico. A IA não considerou o volume de dados. Precisava de uma resposta focada em scripts e gatilhos.
- **Prompt Refinado:** "Atuando como um engenheiro de dados, crie um roteiro de como usar o Google Apps Script para capturar automaticamente relatórios de chamados de TI em anexo de e-mails e atualizar uma base de dados conectada ao Looker Studio, considerando as melhores práticas de performance."

**Tentativa 2: Estrutura de Dashboard**
- **Prompt enviado:** "Quais gráficos devo usar para um dashboard de TI?"
- **Cicatriz (O que aprendi/ajustei):** A IA listou gráficos aleatórios de pizza e barra. Faltou o contexto do Data Storytelling e métricas de ITSM.
- **Prompt Refinado:** "Com base nos guias de ITSM e Data Storytelling, sugira a disposição visual (layout) de um dashboard no Power BI focado em Service Desk. Quais KPIs devem ficar no topo da tela e quais gráficos reduzem a carga cognitiva do gestor ao analisar o MTTR?"

## 📖 Miniguia de Estudo (Entrega Final)

### Resumo Estruturado do Assunto
A criação de um ecossistema de análise de dados em TI envolve três pilares:
1. **Coleta e Automação:** Uso de scripts (ex: Apps Script) para garantir que os dados de sistemas de chamados cheguem à base sem intervenção manual.
2. **Modelagem e Conexão:** Preparação da base (ex: Google Sheets ou bancos SQL) para que ferramentas como Looker Studio ou Power BI leiam as métricas sem lentidão.
3. **Visualização:** Aplicação de conceitos de Data Storytelling, evitando saturação visual e destacando KPIs que direcionam ações imediatas (ex: chamados próximos do vencimento do SLA).

### Glossário
- **MTTR (Mean Time to Resolve):** Tempo médio necessário para resolver um chamado ou falha técnica.
- **SLA (Service Level Agreement):** Acordo de nível de serviço que define os prazos de atendimento.
- **Data Extractions/Agendamento:** Rotina configurada nas ferramentas de BI para buscar novos dados na origem em intervalos definidos.
- **Apps Script:** Plataforma de script baseada em JavaScript para automação de tarefas no ecossistema Google.
- **Carga Cognitiva:** Esforço mental exigido para o usuário interpretar as informações de um painel visual.

### 🤖 Prompts Reutilizáveis (Para revisões futuras)
Caso precise revisar os conceitos ou gerar novas ideias, utilize estes prompts no assistente:
1. *"Explique o conceito de [INSERIR MÉTRICA DE TI] e sugira o melhor tipo de gráfico para monitorá-lo diariamente."*
2. *"Analise este script de automação de dados: [COLAR SCRIPT]. Aponte possíveis gargalos de performance ao importar para uma ferramenta de BI."*
3. *"Quais são os princípios de design visual que devo aplicar para destacar uma quebra de SLA em uma tabela no Looker Studio?"*
