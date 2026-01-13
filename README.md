# financial-lakehouse-databricks

# Financial Lakehouse com Databricks e ADLS Gen2

## Objetivo
Projeto de portfólio para Engenharia de Dados com foco em:
- ingestão e transformação de dados financeiros
- arquitetura Lakehouse (Bronze / Silver / Gold)
- uso de Azure Databricks + ADLS Gen2
- controle de custos e boas práticas em ambiente cloud

O projeto simula um cenário real de dados financeiros e macroeconômicos,
com consumo final via Power BI.

---

## Arquitetura (TO-BE)
- **Armazenamento:** Azure Data Lake Storage Gen2
- **Processamento:** Azure Databricks (Apache Spark)
- **Formato:** Delta Lake
- **Camadas:** Bronze, Silver e Gold
- **Versionamento:** GitHub
- **BI:** Power BI

Diagrama detalhado em `docs/architecture.md`.

---

## Fontes de dados
- Dataset histórico de preços (CSV – dados públicos)
- Séries macroeconômicas (ex: BACEN/SGS – API pública)

---

## Organização do Data Lake
├─ bronze/
├─ silver/
├─ gold/
└─ landing/

---

## Como executar
1. Criar Storage Account com ADLS Gen2
2. Criar Azure Databricks Workspace
3. Configurar acesso seguro ao ADLS
4. Executar pipelines no Databricks (notebooks)

Detalhes em `docs/runbook.md`.

---

## Controle de custos
Este projeto foi desenvolvido considerando:
- conta Azure for Students
- cluster single-node
- auto-termination configurado
- execução apenas sob demanda

Mais detalhes em `docs/cost_control.md`.

---

## Status do projeto
- [x] Infraestrutura criada
- [x] Databricks conectado ao ADLS
- [X] Ingestão Bronze
- [X] Transformações Silver
- [X] Camada Gold
- [ ] Dashboard Power BI
