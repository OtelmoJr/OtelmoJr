<div align="center">

[English](README.md) · **Português**

# Otelmo Junior

### AI Data Engineer

Construo plataformas de dados e os sistemas de IA que rodam sobre elas: arquiteturas
lakehouse, CDC em streaming, GraphRAG, orquestração multi-agente, LLMOps. Trabalho
com formatos abertos e procuro publicar números que eu realmente medi, não promessas.

[![Email](https://img.shields.io/badge/Email-otelmojunior@gmail.com-D14836?style=flat&logo=gmail&logoColor=white)](mailto:otelmojunior@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-OtelmoJr-181717?style=flat&logo=github&logoColor=white)](https://github.com/OtelmoJr)

</div>

---

## O que eu faço

Trabalho nas duas metades da stack moderna de dados e IA.

- **Data engineering.** Lakehouse em formato de tabela aberto (Apache Iceberg),
  versionamento de dados estilo git com Nessie, SQL federado via Trino, Change Data
  Capture em tempo real com garantia de exactly-once e camadas Medallion
  Bronze/Silver.
- **AI engineering.** Retrieval que vai além da busca vetorial simples (GraphRAG
  sobre grafo de conhecimento), orquestração multi-agente com estado usando LangGraph
  e LLMOps de produção: cache semântico, guardrails, telemetria de custo e latência.
- **Plataforma.** Todo projeto sobe com um comando Docker, roda os cenários de ponta
  a ponta e tem a saída real colada no README. Cada repo ainda traz um pacote de
  requisitos escrito como entrega de consultoria: business case, especificação de
  requisitos ISO/IEC/IEEE 29148, arquitetura da solução e plano de aceite.

Procuro não parar no "compila". Um projeto está pronto quando a stack inteira sobe e
toda afirmação do README tem saída por trás. Rodar de ponta a ponta também é onde eu
acho os bugs que uma demo teria escondido.

---

## Projetos em destaque

Seis sistemas, todos rodando localmente a custo zero de nuvem, com documentação
bilíngue (EN/PT-BR) e resultados medidos.

### Plataforma de dados

| Projeto | O que prova | Stack |
|---|---|---|
| **[Zero-Copy Data Mesh](https://github.com/OtelmoJr/zero-copy-lakehouse)** | Joins cross-domain com **zero duplicação de dados**; data-as-code (branch → validar → merge/rollback) via Nessie; um quality gate que barra dado ruim antes de chegar na `main`. | Iceberg · Nessie · Trino · MinIO · Dagster · Great Expectations |
| **[Real-Time CDC → Lakehouse](https://github.com/OtelmoJr/real-time-cdc-lakehouse)** | Todo insert, update e delete no Postgres espelhado numa tabela Silver em **~12s, linha a linha**, exactly-once mesmo com crash, com deletes e eventos atrasados ou fora de ordem tratados corretamente. | Postgres · Debezium · Redpanda · Spark Structured Streaming · Iceberg · Trino |
| **[Pipeline FinOps Kubernetes-Native](https://github.com/OtelmoJr/k8s-finops-pipeline)** | Atribui custo de nuvem até o **pod de 3 minutos**, ao time e namespace que o gerou, e escancara o desperdício: **53.8% do gasto modelado** foi reservado e nunca usado. Spark-on-K8s via Spark Operator. | Spark-on-K8s · MinIO · ClickHouse · Grafana · Prometheus |

### Plataforma de IA

| Projeto | O que prova | Stack |
|---|---|---|
| **[GraphRAG Multi-Agent](https://github.com/OtelmoJr/graphrag-multiagent)** | Perguntas multi-hop que a busca vetorial pura erra. Um grafo de conhecimento somado a retrieval híbrido alimenta um loop de agentes Supervisor / Reader / Fact-Checker que se autocorrige. | LangGraph · Neo4j · Qdrant · Ollama · Ragas |
| **[LLMOps Production Gateway](https://github.com/OtelmoJr/llmops-gateway)** | Gateway drop-in compatível com a API da OpenAI, com cache semântico (**TTFT ~9ms no hit contra ~820ms indo ao modelo**), guardrails fail-closed de PII e injection, e telemetria completa de custo e latência. | FastAPI · Qdrant · Ollama · SQLite · Prometheus |
| **[Agente SRE Autônomo](https://github.com/OtelmoJr/sre-agent)** | O agente escreve o rollback antes e prova o fix num sandbox isolado. Depois um **portão human-in-the-loop** precisa aprovar antes de qualquer coisa tocar produção; negue e nada roda. | Python · Sandbox Docker · HITL · LLM plugável |

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

## Como eu construo

- **Formato aberto primeiro.** Iceberg e Delta no lugar de lock-in proprietário, para
  o dado sobreviver ao engine que o escreveu.
- **Correção sob falha.** Exactly-once, upsert idempotente, recovery por checkpoint,
  quality gate bloqueante. Nada disso aparece numa demo, e tudo isso importa em
  produção.
- **Latência é orçamento.** No gateway de LLM só o guardrail barato e o lookup de
  cache rodam antes do primeiro token; o resto vai para background tasks.
- **Custo entra na conta.** Os designs explicitam seus trade-offs, latência contra
  throughput e custo contra performance, e rastreiam gasto de token e de nuvem quando
  faz sentido.
- **Documentado como entrega real.** Business case, especificação de requisitos,
  documento de arquitetura e plano de aceite por projeto, não só código.

---

<div align="center">

**Aberto a vagas de AI Data Engineer · AI Engineer · Data Engineer.**
Vamos conversar — [otelmojunior@gmail.com](mailto:otelmojunior@gmail.com)

</div>
