# Hi, I'm Aluizio Lira

**Senior Backend Engineer working on AI evaluation, MLOps infrastructure, distributed systems, and data-intensive Python/Go backends.**

I build production systems where correctness, throughput, cost, and observability matter. My background combines high-scale backend engineering on AWS, ML-driven workload optimization, and portfolio projects that model the kinds of infrastructure AI teams need: agent evaluation, trace observability, rate limiting, async ingestion, and reproducible performance benchmarking.

---

## Engineering Focus

| Area | Recent work |
| :--- | :--- |
| **Backend systems** | 5+ years building Python/Go services, including platforms handling **120M+ requests/day** and **3B+ monthly events**. |
| **AI / MLOps infrastructure** | ML-driven prioritization systems, agent evaluation tooling, LLM-judge scoring, reproducible benchmark fixtures, and agent telemetry backends. |
| **Distributed systems** | Event-driven pipelines, async orchestration, Redis Lua atomicity, bounded concurrency, blue-green migrations, and failure-aware data pipelines. |
| **Cloud & cost engineering** | AWS infrastructure redesign that reduced compute spend by **50%**, deployment pipeline time by **70%**, and RDS operating cost by **25%**. |

**Core stack:** Python, Go, PostgreSQL, Redis, MongoDB, FastAPI, Django, asyncio, AWS, Terraform, Docker, CI/CD, LLM APIs.

---

## Featured Portfolio

### [AgentBench AI Evaluation](https://github.com/aluiziolira/agentbench-ai-evaluation)

**Event-driven benchmark platform for comparing AI code-review agents against versioned, reproducible PR-review cases.**

- **Why it matters:** AI-agent benchmarks drift when inputs change or raw outputs are discarded. AgentBench fixes the inputs, stores the outputs, and can re-score past runs under new rubrics without paying for new provider calls.
- **Architecture:** Redis Streams orchestration, explicit orchestrator/dispatcher/scoring/aggregator boundaries, MongoDB report persistence, raw I/O archive, FastAPI API, Typer CLI.
- **AI evaluation:** deterministic finding-match scoring plus configurable LLM-judge scoring across OpenAI and Anthropic adapters.
- **Quality bar:** **460+ tests**, `mypy --strict`, ruff, GitHub Actions, Gitleaks, Docker Compose, seeded fixtures, latency/failure metrics.
- **Sample result:** 8 PR-review cases comparing Claude and GPT agents, with stored raw outputs, average score, P50/P95 latency, and failure-rate reporting.

### [Mini Agent Telemetry Lab](https://github.com/aluiziolira/mini-agent-telemetry-lab)

**Django/PostgreSQL observability backend for LLM-agent traces, span ingestion, run finalization, metrics, and async quality evaluation.**

- **Why it matters:** Moves agent debugging from console logs into queryable execution traces with cost, timing, errors, and evaluation lifecycle state.
- **Backend details:** idempotent ingestion, immutable completed-run semantics, strict DRF boundary validation, SQL constraints/indexes, hierarchical trace reconstruction.
- **MLOps details:** framework-agnostic Python tracer, fail-open telemetry transport, durable async evaluator failures, Prometheus-style metrics.
- **Stack:** Python 3.12, Django, DRF, PostgreSQL, Huey/SqlHuey, OpenAI, Docker, pytest, ruff, mypy.

### [Rate Limit Patterns](https://github.com/aluiziolira/rate-limit-patterns)

**Production-grade rate limiting primitives with local and Redis-backed algorithms for atomic multi-instance quotas.**

- **Why it matters:** Naive rate limiters leak under concurrent multi-instance traffic. This project pushes quota decisions into Redis Lua scripts for atomic check-and-update behavior.
- **Engineering details:** token bucket, leaky bucket, sliding-window log, stateless algorithm protocol, Redis/local contract tests, ASGI/FastAPI integration, fail-open/fail-closed policy.
- **Benchmark proof:** local path up to **197K-264K RPS** with microsecond overhead; Redis Lua path around **7K+ RPS**; multi-instance simulation accepted exactly **100/100** under a global limit.

### [Async Patterns Performance Lab](https://github.com/aluiziolira/async-patterns)

**Python async HTTP ingestion lab for bounded concurrency, connection pooling, retries, circuit breakers, and streaming persistence.**

- **Benchmark proof:** sync **130 RPS** -> threaded **600 RPS** -> async **2,500 RPS**, a **20x throughput gain** over the sync baseline.
- **Reliability details:** semaphore backpressure, pooled `aiohttp` sessions, retry budgets with jitter, circuit-breaker state transitions, event-loop monitoring, JSONL/SQLite persistence.
- **Quality bar:** unit/integration tests, mock HTTP server, resilience benchmarks, strict typing, ruff, CI.

### [SQL Throughput Challenge](https://github.com/aluiziolira/sql-throughput-challenge)

**Reproducible PostgreSQL bulk-read benchmark lab comparing sync, pooled, async streaming, cursor, and multiprocessing strategies.**

- **Benchmark proof:** multiprocessing reached **124K rows/sec** at 1M rows, about **5.3x** the naive baseline.
- **Memory proof:** async streaming processed 1M rows with about **97% lower peak memory** than naive `fetchall()`.
- **Engineering details:** Docker-constrained methodology, RSS/CPU profiling, Pydantic settings, strict typing, strategy abstraction, Postgres integration tests.

### [Go Books Scraper](https://github.com/aluiziolira/go-scrape-books)

**Bounded-memory Go scraping ETL with Colly, worker-pool backpressure, retries, Prometheus metrics, and atomic CSV/JSONL output.**

- **Benchmark proof:** in-memory pipeline at **2.2M items/sec** with ~326 B/op and 4 allocs/op; real crawl run at **108 items/sec** with rate limits respected.
- **Engineering details:** buffered-channel streaming pipeline, LRU dedupe, typed error handling, context cancellation, atomic writers, Dockerized runtime, parser/retry/pipeline/e2e tests.

---

## Production Experience Highlights

- **Scale:** Accountable for production scraping and data systems processing **3B+ monthly events**, **120M+ daily requests**, and millions of daily database transactions.
- **Cloud migration:** Architected a zero-downtime AWS Lambda -> ECS Fargate migration for a **120M+ req/day** suite, removing timeout/concurrency bottlenecks and reducing infrastructure cost by **50%**.
- **Data infrastructure:** Built event-driven ETL from Kinesis -> Glue -> S3 -> Athena, transforming daily JSON event streams into queryable Parquet data lake partitions.
- **ML optimization:** Deployed an SGD Regressor for payload prioritization, improving extraction rates by **20%**; implemented a reinforcement-learning multi-armed bandit that improved scraping efficiency by **35%**.
- **Database operations:** Planned and executed a controlled PostgreSQL RDS major-version upgrade for a **2M+ records/day** workload, improving analytical query performance by **40%** and reducing RDS cost by **25%** through benchmarking, query tuning, and right-sizing.
- **Leadership:** Fast-tracked to Senior Engineer after rebuilding team practices during **60% turnover**, onboarding a new manager and developers, and standardizing documentation and repository patterns.

---

## Technical Toolbox

| Category | Tools |
| :--- | :--- |
| **Languages** | Python, Go, SQL, Bash |
| **Backend** | FastAPI, Django, Django REST Framework, Pydantic, Typer, REST APIs |
| **Concurrency & Systems** | asyncio, aiohttp, asyncpg, Redis Streams, Redis Lua, worker pools, circuit breakers, backpressure |
| **Data & Storage** | PostgreSQL, Redis, MongoDB, S3, Parquet, JSONL, Glue, Athena, Kinesis |
| **AI / ML** | LLM integration, OpenAI, Anthropic, agent evaluation, LLM-judge scoring, RAG, scikit-learn, multi-armed bandits |
| **Cloud & DevOps** | AWS ECS, Lambda, RDS, CloudWatch, Terraform, Docker, Bitbucket Pipelines, GitHub Actions |
| **Quality & Observability** | pytest, mypy strict, ruff, Gitleaks, Prometheus metrics, structured logging, trace-style telemetry |

---

## Certifications

<p align="left">
<a href="https://www.credly.com/badges/bf2c4386-88a8-4f25-8fe5-c3573b128273"><img src="https://images.credly.com/images/1a634b4e-3d6b-4a74-b118-c0dcb429e8d2/image.png" width="110" height="110" alt="AWS Certified Machine Learning Engineer - Associate"></a>
<a href="https://www.credly.com/badges/f051c585-460d-4f90-9414-6c52228d192d"><img src="https://images.credly.com/images/b9feab85-1a43-4f6c-99a5-631b88d5461b/image.png" width="110" height="110" alt="AWS Certified Developer - Associate"></a>
</p>

- **AWS Certified Machine Learning Engineer - Associate**
- **AWS Certified Developer - Associate**
- **Anthropic:** [MCP: Advanced Topics](https://verify.skilljar.com/c/89absohofk4b) and [Claude Code in Action](https://verify.skilljar.com/c/bkqqi5i5qns6)

---

## Contact

- **Email:** [alumlira@gmail.com](mailto:alumlira@gmail.com)
- **LinkedIn:** [linkedin.com/in/aluiziolira](https://linkedin.com/in/aluiziolira)
- **Location:** Recife, Brazil | Remote
