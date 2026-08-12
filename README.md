<div align="center">

**English** · [Português](README.pt-BR.md)

# Otelmo Junior

### AI Data Engineer — building the data platforms *and* the AI systems that run on top of them

I design production-grade data platforms (lakehouse, streaming CDC, exactly-once)
and the AI infrastructure that sits on them (GraphRAG, multi-agent orchestration,
LLMOps). Open formats, distributed systems, and real numbers over slideware.

[![Email](https://img.shields.io/badge/Email-otelmojunior@gmail.com-D14836?style=flat&logo=gmail&logoColor=white)](mailto:otelmojunior@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-OtelmoJr-181717?style=flat&logo=github&logoColor=white)](https://github.com/OtelmoJr)

</div>

---

## What I do

I work across the whole modern data + AI stack — from the bytes on object storage
to the agent reasoning over them:

- **Data Engineering** — lakehouse on open table formats (Apache Iceberg), git-like
  data versioning (Nessie), federated SQL (Trino), real-time Change Data Capture
  with exactly-once guarantees, and a Medallion (Bronze → Silver) architecture.
- **AI Engineering** — Retrieval-Augmented Generation beyond naïve vector search
  (GraphRAG over a knowledge graph), stateful multi-agent orchestration (LangGraph),
  and production LLMOps (semantic caching, guardrails, cost & latency telemetry).
- **Platform & rigor** — everything ships as a one-command Docker stack, runs the
  scenarios end to end, and pastes the **real output** into the README. Each repo
  also carries a consultancy-style requirements package (business case, ISO/IEC/IEEE
  29148 requirements spec, solution architecture, acceptance plan).

> My bar is not "it compiles." It's: **it comes up, runs the scenarios end to end,
> and proves every differentiator with real output.** Bringing the full stack up is
> exactly what surfaces the bugs a demo never would.

---

## Featured projects

Four production-grade systems, each running 100% locally at zero cloud cost, each
with bilingual (EN/PT-BR) docs and measured results.

### Data platform

| Project | What it proves | Stack |
|---|---|---|
| **[Zero-Copy Data Mesh](https://github.com/OtelmoJr/zero-copy-lakehouse)** | Cross-domain joins with **zero data duplication**; data-as-code (branch → validate → merge/rollback) via Nessie; quality gate that blocks bad data before it reaches `main`. | Iceberg · Nessie · Trino · MinIO · Dagster · Great Expectations |
| **[Real-Time CDC → Lakehouse](https://github.com/OtelmoJr/real-time-cdc-lakehouse)** | Every insert/update/delete in Postgres mirrored into a Silver table in **~12s, row-for-row**; **exactly-once** across crashes; deletes and late/out-of-order events handled correctly. | Postgres · Debezium · Redpanda · Spark Structured Streaming · Iceberg · Trino |
| **[Kubernetes-Native FinOps Pipeline](https://github.com/OtelmoJr/k8s-finops-pipeline)** | Attributes cloud cost — down to a **3-minute pod** — to the right team/namespace, and surfaces waste (**53.8% of modelled spend** was reserved-but-unused). Spark-on-K8s via the Spark Operator. | Spark-on-K8s · MinIO · ClickHouse · Grafana · Prometheus |

### AI platform

| Project | What it proves | Stack |
|---|---|---|
| **[GraphRAG Multi-Agent](https://github.com/OtelmoJr/graphrag-multiagent)** | Multi-hop reasoning a plain vector search gets wrong; a knowledge graph + hybrid retrieval feeding a Supervisor / Reader / **Fact-Checker** agent loop with self-correction. | LangGraph · Neo4j · Qdrant · Ollama · Ragas |
| **[LLMOps Production Gateway](https://github.com/OtelmoJr/llmops-gateway)** | Drop-in OpenAI-compatible gateway adding semantic cache (**TTFT ~9ms on a hit vs ~820ms to the model**), fail-closed PII/injection guardrails, and full cost/latency telemetry — without wrecking latency. | FastAPI · Qdrant · Ollama · SQLite · Prometheus |
| **[Autonomous SRE Agent](https://github.com/OtelmoJr/sre-agent)** | Sandbox-first, rollback-always, approval-gated remediation: the agent proves a fix in an isolated sandbox, then a **human-in-the-loop gate** must approve before it touches production — deny it and nothing runs. | Python · Docker sandbox · HITL · pluggable LLM |

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

## How I build (the differentiators)

- **Open formats first.** Iceberg / Delta over proprietary lock-in — data outlives
  the engine that wrote it.
- **Correctness under failure.** Exactly-once, idempotent upserts, checkpoint
  recovery, blocking data-quality gates — the parts that are invisible in a demo and
  decisive in production.
- **Latency as a budget.** In the LLM gateway, only the cheap guardrail and cache
  lookup run before the first token; everything else is deferred to background tasks.
- **Cost-aware by default.** Every design states its trade-offs (latency vs
  throughput, cost vs performance) and, where relevant, tracks token/cloud cost.
- **Documented like a real delivery.** Business case, requirements spec, architecture
  doc, and acceptance plan per project — not just code.

---

## GitHub stats

<div align="center">

![Otelmo's GitHub stats](https://github-readme-stats.vercel.app/api?username=OtelmoJr&show_icons=true&theme=tokyonight&hide_border=true&count_private=true)
![Top languages](https://github-readme-stats.vercel.app/api/top-langs/?username=OtelmoJr&layout=compact&theme=tokyonight&hide_border=true)

</div>

---

<div align="center">

**Open to AI Data Engineer · AI Engineer · Data Engineer roles.**
Let's talk — [otelmojunior@gmail.com](mailto:otelmojunior@gmail.com)

</div>
