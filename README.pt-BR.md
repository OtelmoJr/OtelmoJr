<div align="center">

[English](README.md) · **Português**

# Otelmo Junior

### AI Data Engineer — construo as plataformas de dados *e* os sistemas de IA que rodam sobre elas

Projeto plataformas de dados production-grade (lakehouse, CDC em streaming,
exactly-once) e a infraestrutura de IA que roda em cima (GraphRAG, orquestração
multi-agente, LLMOps). Formatos abertos, sistemas distribuídos e números reais
no lugar de slide.

[![Email](https://img.shields.io/badge/Email-otelmojunior@gmail.com-D14836?style=flat&logo=gmail&logoColor=white)](mailto:otelmojunior@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-OtelmoJr-181717?style=flat&logo=github&logoColor=white)](https://github.com/OtelmoJr)

</div>

---

## O que eu faço

Trabalho na stack moderna de dados + IA de ponta a ponta — dos bytes no object
storage ao agente que raciocina sobre eles:

- **Data Engineering** — lakehouse em formato de tabela aberto (Apache Iceberg),
  versionamento de dados estilo git (Nessie), SQL federado (Trino), Change Data
  Capture em tempo real com garantia de exactly-once e arquitetura Medallion
  (Bronze → Silver).
- **AI Engineering** — RAG além da busca vetorial ingênua (GraphRAG sobre grafo de
  conhecimento), orquestração multi-agente com estado (LangGraph) e LLMOps de
  produção (cache semântico, guardrails, telemetria de custo e latência).
- **Plataforma & rigor** — tudo sobe com um comando via Docker, roda os cenários de
  ponta a ponta e cola a **saída real** no README. Cada repo ainda traz um pacote de
  documentação estilo consultoria (business case, especificação de requisitos
  ISO/IEC/IEEE 29148, arquitetura da solução e plano de aceite).

> Minha régua não é "compila". É: **sobe, roda os cenários de ponta a ponta e prova
> cada diferencial com saída real.** Subir a stack inteira é justamente o que revela
> os bugs que uma demo nunca mostraria.

---

## Projetos em destaque

Quatro sistemas production-grade, cada um rodando 100% local a custo zero de nuvem,
com documentação bilíngue (EN/PT-BR) e resultados medidos.

### Plataforma de dados

| Projeto | O que prova | Stack |
|---|---|---|
| **[Zero-Copy Data Mesh](https://github.com/OtelmoJr/zero-copy-lakehouse)** | Joins cross-domain com **zero duplicação de dados**; data-as-code (branch → validar → merge/rollback) via Nessie; quality gate que barra dado ruim antes de chegar na `main`. | Iceberg · Nessie · Trino · MinIO · Dagster · Great Expectations |
| **[Real-Time CDC → Lakehouse](https://github.com/OtelmoJr/real-time-cdc-lakehouse)** | Todo insert/update/delete no Postgres espelhado numa tabela Silver em **~12s, linha a linha**; **exactly-once** mesmo com crash; deletes e eventos atrasados/fora de ordem tratados corretamente. | Postgres · Debezium · Redpanda · Spark Structured Streaming · Iceberg · Trino |
| **[Pipeline FinOps Kubernetes-Native](https://github.com/OtelmoJr/k8s-finops-pipeline)** | Atribui custo de nuvem — até o **pod de 3 minutos** — ao time/namespace certo, e destaca desperdício (**53.8% do gasto modelado** era reservado e não usado). Spark-on-K8s via Spark Operator. | Spark-on-K8s · MinIO · ClickHouse · Grafana · Prometheus |

### Plataforma de IA

| Projeto | O que prova | Stack |
|---|---|---|
| **[GraphRAG Multi-Agent](https://github.com/OtelmoJr/graphrag-multiagent)** | Raciocínio multi-hop que a busca vetorial pura erra; grafo de conhecimento + retrieval híbrido alimentando um loop de agentes Supervisor / Reader / **Fact-Checker** com auto-correção. | LangGraph · Neo4j · Qdrant · Ollama · Ragas |
| **[LLMOps Production Gateway](https://github.com/OtelmoJr/llmops-gateway)** | Gateway drop-in compatível com a API da OpenAI, com cache semântico (**TTFT ~9ms no hit vs ~820ms indo ao modelo**), guardrails fail-closed de PII/injection e telemetria completa de custo/latência — sem estourar a latência. | FastAPI · Qdrant · Ollama · SQLite · Prometheus |
| **[Agente SRE Autônomo](https://github.com/OtelmoJr/sre-agent)** | Remediação sandbox-first, rollback-sempre, com portão de aprovação: o agente prova o fix num sandbox isolado, e um **portão human-in-the-loop** precisa aprovar antes de tocar produção — negue e nada roda. | Python · Sandbox Docker · HITL · LLM plugável |

---

## Stack

**Linguagens & processamento**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-025E8C?style=flat&logo=postgresql&logoColor=white)
![Apache Spark](https://img.shields.io/badge/Apache%20Spark-E25A1C?style=flat&logo=apachespark&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=flat&logo=apachespark&logoColor=white)

**Lakehouse & storage**
![Apache Iceberg](https://img.shields.io/badge/Apache%20Iceberg-1D4ED8?style=flat&logo=apacheiceberg&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta%20Lake-00ADD4?style=flat&logo=databricks&logoColor=white)
![Trino](https://img.shields.io/badge/Trino-DD00A1?style=flat&logo=trino&logoColor=white)
![Nessie](https://img.shields.io/badge/Nessie-73C41D?style=flat)
![MinIO](https://img.shields.io/badge/MinIO-C72E49?style=flat&logo=minio&logoColor=white)

**Streaming & orquestração**
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat&logo=apachekafka&logoColor=white)
![Redpanda](https://img.shields.io/badge/Redpanda-E14F26?style=flat)
![Debezium](https://img.shields.io/badge/Debezium-4E8FD4?style=flat)
![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat&logo=apacheairflow&logoColor=white)
![Dagster](https://img.shields.io/badge/Dagster-654FF0?style=flat&logo=dagster&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat&logo=dbt&logoColor=white)

**IA / LLM**
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat&logo=langchain&logoColor=white)
![Neo4j](https://img.shields.io/badge/Neo4j-4581C3?style=flat&logo=neo4j&logoColor=white)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat&logo=ollama&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)

**Plataforma**
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat&logo=databricks&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat&logo=grafana&logoColor=white)

---

## Como eu construo (os diferenciais)

- **Formato aberto primeiro.** Iceberg / Delta no lugar de lock-in proprietário — o
  dado sobrevive ao engine que o escreveu.
- **Correção sob falha.** Exactly-once, upsert idempotente, recovery por checkpoint,
  quality gate bloqueante — as partes invisíveis numa demo e decisivas em produção.
- **Latência é orçamento.** No gateway de LLM, só o guardrail barato e o lookup de
  cache rodam antes do primeiro token; o resto é adiado para background tasks.
- **Consciente de custo por padrão.** Todo design explicita seus trade-offs (latência
  vs throughput, custo vs performance) e, quando cabe, rastreia custo de token/nuvem.
- **Documentado como entrega real.** Business case, especificação de requisitos,
  documento de arquitetura e plano de aceite por projeto — não só código.

---

## Estatísticas do GitHub

<div align="center">

![Estatísticas do GitHub de Otelmo](https://github-readme-stats.vercel.app/api?username=OtelmoJr&show_icons=true&theme=tokyonight&hide_border=true&count_private=true)
![Linguagens mais usadas](https://github-readme-stats.vercel.app/api/top-langs/?username=OtelmoJr&layout=compact&theme=tokyonight&hide_border=true)

</div>

---

<div align="center">

**Aberto a vagas de AI Data Engineer · AI Engineer · Data Engineer.**
Vamos conversar — [otelmojunior@gmail.com](mailto:otelmojunior@gmail.com)

</div>
