<div align="center">

**English** · [Português](README.pt-BR.md)

# Otelmo Junior

### AI Data Engineer

I build data platforms and the AI systems that run on top of them: lakehouse
architectures, streaming CDC, GraphRAG, multi-agent orchestration, LLMOps. I work in
open formats, and I try to publish numbers I actually measured rather than claims.

[![Email](https://img.shields.io/badge/Email-otelmojunior@gmail.com-D14836?style=flat&logo=gmail&logoColor=white)](mailto:otelmojunior@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-OtelmoJr-181717?style=flat&logo=github&logoColor=white)](https://github.com/OtelmoJr)

</div>

---

## What I do

I work across both halves of the modern data and AI stack.

- **Data engineering.** Lakehouse on open table formats (Apache Iceberg), git-like
  data versioning with Nessie, federated SQL through Trino, real-time Change Data
  Capture with exactly-once guarantees, and Bronze/Silver Medallion layers.
- **AI engineering.** Retrieval that goes past plain vector search (GraphRAG over a
  knowledge graph), stateful multi-agent orchestration with LangGraph, and LLMOps in
  production: semantic caching, guardrails, cost and latency telemetry.
- **Platform work.** Every project comes up with one Docker command, runs its
  scenarios end to end, and has the real output pasted into its README. Each repo
  also carries a requirements package written like a consultancy deliverable:
  business case, ISO/IEC/IEEE 29148 requirements spec, solution architecture, and an
  acceptance plan.

I try not to stop at "it compiles". A project is finished when the whole stack comes
up and every claim in the README has output behind it. Running things end to end is
also where I find the bugs a demo would have hidden.

---

## Featured projects

Six systems, all running locally at zero cloud cost, with bilingual docs (EN/PT-BR)
and measured results.

### Data platform

| Project | What it proves | Stack |
|---|---|---|
| **[Zero-Copy Data Mesh](https://github.com/OtelmoJr/zero-copy-lakehouse)** | Cross-domain joins with **zero data duplication**; data-as-code (branch → validate → merge/rollback) through Nessie; a quality gate that blocks bad data before it reaches `main`. | Iceberg · Nessie · Trino · MinIO · Dagster · Great Expectations |
| **[Real-Time CDC → Lakehouse](https://github.com/OtelmoJr/real-time-cdc-lakehouse)** | Every insert, update and delete in Postgres mirrored into a Silver table in **~12s, row for row**, exactly-once across crashes, with deletes and late or out-of-order events handled correctly. | Postgres · Debezium · Redpanda · Spark Structured Streaming · Iceberg · Trino |
| **[Kubernetes-Native FinOps Pipeline](https://github.com/OtelmoJr/k8s-finops-pipeline)** | Attributes cloud cost down to a **3-minute pod**, to the team and namespace that incurred it, and surfaces waste: **53.8% of modelled spend** was reserved and never used. Spark-on-K8s through the Spark Operator. | Spark-on-K8s · MinIO · ClickHouse · Grafana · Prometheus |

### AI platform

| Project | What it proves | Stack |
|---|---|---|
| **[GraphRAG Multi-Agent](https://github.com/OtelmoJr/graphrag-multiagent)** | Multi-hop questions that plain vector search gets wrong. A knowledge graph plus hybrid retrieval feeds a Supervisor / Reader / Fact-Checker agent loop that self-corrects. | LangGraph · Neo4j · Qdrant · Ollama · Ragas |
| **[LLMOps Production Gateway](https://github.com/OtelmoJr/llmops-gateway)** | Drop-in OpenAI-compatible gateway with a semantic cache (**TTFT ~9ms on a hit against ~820ms going to the model**), fail-closed PII and injection guardrails, and full cost and latency telemetry. | FastAPI · Qdrant · Ollama · SQLite · Prometheus |
| **[Autonomous SRE Agent](https://github.com/OtelmoJr/sre-agent)** | The agent writes its rollback first and proves the fix in an isolated sandbox. A **human-in-the-loop gate** then has to approve before anything touches production; deny it and nothing runs. | Python · Docker sandbox · HITL · pluggable LLM |

---

## Tech stack

**Languages & processing**
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

**Streaming & orchestration**
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat&logo=apachekafka&logoColor=white)
![Redpanda](https://img.shields.io/badge/Redpanda-E14F26?style=flat)
![Debezium](https://img.shields.io/badge/Debezium-4E8FD4?style=flat)
![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat&logo=apacheairflow&logoColor=white)
![Dagster](https://img.shields.io/badge/Dagster-654FF0?style=flat&logo=dagster&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat&logo=dbt&logoColor=white)

**AI / LLM**
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat&logo=langchain&logoColor=white)
![Neo4j](https://img.shields.io/badge/Neo4j-4581C3?style=flat&logo=neo4j&logoColor=white)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat&logo=ollama&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)

**Platform**
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat&logo=databricks&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat&logo=grafana&logoColor=white)

---

## How I build

- **Open formats first.** Iceberg and Delta instead of proprietary lock-in, so the
  data outlives whatever engine wrote it.
- **Correctness under failure.** Exactly-once delivery, idempotent upserts, recovery
  from checkpoints, blocking data-quality gates. None of it shows up in a demo, and
  all of it matters in production.
- **Latency is a budget.** In the LLM gateway only the cheap guardrail and the cache
  lookup run before the first token; everything else moves to background tasks.
- **Cost gets tracked.** Designs state their trade-offs, latency against throughput
  and cost against performance, and track token and cloud spend where it applies.
- **Documented like a real delivery.** Business case, requirements spec, architecture
  document and acceptance plan for each project, not just code.

---

<div align="center">

**Open to AI Data Engineer · AI Engineer · Data Engineer roles.**
Let's talk — [otelmojunior@gmail.com](mailto:otelmojunior@gmail.com)

</div>
