# Hi, I'm Aluizio Lira 👋

**Senior Backend Engineer | Distributed Systems & Data Infrastructure**

I engineer high-concurrency distributed systems and fault-tolerant data pipelines. I specialize in scaling Python/Go backends, ruthlessly optimizing cloud infrastructure footprint, and integrating applied ML to drive system efficiency at scale.

---

### 🚀 At a Glance

- **Leadership Profile:** Fast-tracked to Senior Engineer (16 months) for stabilizing and rebuilding a 5-person engineering pod during a period of 60% turnover.
- **Operational Scale:** Accountable for production systems processing **3B+ monthly events** and 120M+ daily requests with 99.9% availability.
- **Core Arsenal:** Python (Expert), Go, PostgreSQL, AWS (ECS, Lambda, RDS), Terraform.
- **Location:** Recife, Brazil (Remote).

---

## 🎯 High-Impact Technical Mastery

- **Zero-Downtime Migrations:** Architected critical infrastructure migrations, including serverless Lambda to ECS containers (handling **120M+ req/day**) and PostgreSQL 15.12→18.1 (2M+ records/day), maintaining complete system availability.
- **Cost Engineering at Scale:** Slashed AWS compute spend by **50%** through strategic Lambda→ECS containerization and reduced RDS operational costs by **25%** via version optimization and right-sizing.
- **ML-Optimized Pipelines:** Engineered an SGD Regressor for predictive payload prioritization (**20% extraction increase**) and deployed a Reinforcement Learning Multi-Armed Bandit (**35% scraping efficiency gain**).

---

## 💼 Featured Labs & Projects

### 🔬 [Mini Agent Telemetry Lab](https://github.com/aluiziolira/mini-agent-telemetry-lab)
**The Challenge:** Backend demonstrating production patterns for AI agent observability, turning opaque execution pipelines into queryable, evaluated traces with strict data integrity.

- **Tech:** Python 3.12+, Django, Django REST Framework, PostgreSQL 18, Huey 2.6, Docker, Prometheus, mypy (strict mode)
- **Impact:** Idempotent ingestion, immutable run semantics, durable async failures. These observability patterns are designed to withstand retry storms or partial failures.

### ⚡ [Async-Patterns Performance Lab](https://github.com/aluiziolira/async-patterns)
**The Challenge:** Demonstrating production patterns for high-concurrency HTTP workloads—circuit breaker protection, backpressure handling, and graceful shutdown—to solve the unbounded `gather()` anti-pattern that crashes systems under load.

- **Tech:** Python 3.12+, aiohttp, asyncio, pytest, Poetry, mypy (strict mode), GitHub Actions
- **Impact:** **20x throughput gain** (130 → 2,500 RPS) with cascade failure prevention via circuit breaker state machine, bounded concurrency enforcement, and graceful degradation under load.

### 🌊 [Go Books Scraper: Streaming ETL](https://github.com/aluiziolira/go-scrape-books)
**The Challenge:** Web-scale data extraction that maintains constant memory footprint regardless of crawl size, solving the classic scraper OOM failure mode.

- **Tech:** Go, Colly, Worker Pools, Prometheus, LRU Deduplication, Buffered Channels
- **Impact:** **2.2M items/sec** throughput with constant memory footprint via intentional backpressure design

### 📊 [SQL Throughput Challenge](https://github.com/aluiziolira/sql-throughput-challenge)
**The Challenge:** Empirical proof of the most efficient PostgreSQL bulk-read strategies, replacing anecdote with benchmarked evidence for architectural decisions.

- **Tech:** Python, asyncpg, multiprocessing, Pydantic, PostgreSQL 16
- **Impact:** **124K rows/sec** (5.3x baseline) via multiprocessing, or **97% memory reduction** via async streaming

---

## 🛠️ Tech Stack & Tooling

| Category | Tools |
| :--- | :--- |
| **Languages** | Python (Expert), Go, SQL, Bash |
| **Backend & Frameworks** | Django, Django REST Framework, FastAPI, asyncio, aiohttp, asyncpg |
| **Data & Cloud** | AWS (ECS, Lambda, RDS, S3, Kinesis, Glue, Athena), PostgreSQL, Terraform |
| **Machine Learning** | scikit-learn (SGD Regressor), Reinforcement Learning (Multi-Armed Bandit), A/B Testing, Feature Engineering |
| **AI Workflows** | LLM Integration (GPT, Claude), RAG, Semantic Search, Prompt Engineering |
| **DevOps & IaC** | Docker, Terraform, CloudFormation, Bitbucket Pipelines, GitHub Actions |
| **Observability** | Prometheus, CloudWatch, OpenTelemetry-inspired tracing, structured logging |
| **Data Engineering** | ETL/ELT pipelines, Parquet, JSONB, data lakes (S3 + Glue + Athena), streaming processing |

---

## 🏆 Verified Expertise

<p align="left">
<a href="https://www.credly.com/badges/bf2c4386-88a8-4f25-8fe5-c3573b128273"><img src="https://images.credly.com/images/1a634b4e-3d6b-4a74-b118-c0dcb429e8d2/image.png" width="125" height="125"></a>
<a href="https://www.credly.com/badges/f051c585-460d-4f90-9414-6c52228d192d"><img src="https://images.credly.com/images/b9feab85-1a43-4f6c-99a5-631b88d5461b/image.png" width="125" height="125"></a>
</p>

- **Anthropic:** [MCP: Advanced Topics](https://verify.skilljar.com/c/89absohofk4b) & [Claude Code in Action](https://verify.skilljar.com/c/bkqqi5i5qns6) (2026)

---

## 📫 Networking & Collaboration

I am always interested in discussing **distributed systems architecture, zero-downtime migrations, ML-driven optimization, or high-scale data infrastructure.** If you are solving complex problems in these domains, let's connect.

- **Email:** [alumlira@gmail.com](mailto:alumlira@gmail.com)
- **LinkedIn:** [linkedin.com/in/aluiziolira](https://linkedin.com/in/aluiziolira)
