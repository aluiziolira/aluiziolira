# Hi, I'm Aluizio Lira

**Senior Backend Engineer focused on distributed systems, data-intensive Python/Go services, and AI/agent infrastructure on AWS.**

I build backend systems where correctness, throughput, cost, and observability are measured rather than assumed. At work I'm accountable for data-extraction and processing platforms handling **120M+ requests/day**; outside work I maintain a set of engineering labs covering infrastructure that AI teams need: agent evaluation, trace observability, rate limiting, async ingestion, and reproducible performance benchmarking.

## Engineering Focus

| Area | Work |
| :--- | :--- |
| **Backend systems** | 5+ years building backend services, primarily in Python with Go for performance-critical tooling, including high-traffic data-extraction and processing platforms. |
| **Distributed systems** | Event-driven pipelines, async orchestration, Redis Lua atomicity, bounded concurrency, blue-green deployments, failure-aware data processing. |
| **Cloud & cost engineering** | AWS infrastructure redesign that cut compute spend by **50%**, deployment pipeline time by **70%**, and RDS operating cost by **25%**. |
| **AI / ML infrastructure** | ML-driven workload optimization in production; agent evaluation, LLM-judge scoring, and trace observability tooling in the projects below. |

**Core stack:** Python, Go, PostgreSQL, Redis, MongoDB, FastAPI, Django, asyncio, AWS, Terraform, Docker, LLM APIs.

## Production Experience

- **Cloud migration:** Architected the AWS Lambda → ECS Fargate migration for a **120M+ req/day** scraping suite: load-tested at scale, cut over blue-green with zero downtime, removed Lambda's timeout and concurrency ceilings, and cut infrastructure cost by **50%**.
- **Database operations:** Planned and executed a controlled PostgreSQL RDS major-version upgrade (15 → 18) for a 2M+ records/day workload, benchmarking performance before and after cutover: **40% faster** analytical queries and **25% lower** RDS cost through query-plan tuning and instance right-sizing.
- **Data infrastructure:** Designed a serverless event-driven ETL pipeline (Kinesis → Glue → S3 → Athena) that turns millions of daily JSON error events into queryable Parquet data-lake partitions, replacing ad-hoc log digging with real-time error analysis.
- **ML in production:** Deployed an SGD-regressor model that prioritizes scraping payloads by predicted value, lifting extraction rates by **20%**, plus a reinforcement-learning multi-armed bandit that automated performance tuning across millions of daily database transactions.
- **Leadership:** Promoted to Senior after 16 months at mid-level for rebuilding the team through 60% turnover: onboarded a new engineering manager and two developers, grew the team back from 2 to 5 engineers, and standardized documentation templates and repository structure.

## Featured Projects

### [AgentBench: AI Agent Evaluation](https://github.com/aluiziolira/agentbench-ai-evaluation)

Event-driven benchmark platform for comparing AI code-review agents against versioned, reproducible PR-review cases.

- Fixes the inputs and stores raw outputs, so past runs can be re-scored under new rubrics without paying for new provider calls, solving the drift that makes most agent benchmarks incomparable.
- Redis Streams orchestration with explicit orchestrator/dispatcher/scoring/aggregator boundaries, MongoDB report persistence, FastAPI API, Typer CLI.
- Deterministic finding-match scoring plus configurable LLM-judge scoring across OpenAI and Anthropic adapters; sample run compares Claude and GPT agents with average score, P50/P95 latency, and failure-rate reporting.
- 462 tests, `mypy --strict`, ruff, CI with secret scanning, seeded fixtures.

### [Mini Agent Telemetry Lab](https://github.com/aluiziolira/mini-agent-telemetry-lab)

Django/PostgreSQL observability backend for LLM-agent traces: span ingestion, run finalization, metrics, and async quality evaluation.

- Moves agent debugging from console logs into queryable execution traces with cost, timing, errors, and evaluation lifecycle state.
- Idempotent ingestion, immutable completed-run semantics, hierarchical trace reconstruction, and database-level integrity constraints.
- Framework-agnostic fail-open Python tracer, durable persistence of async evaluator failures, Prometheus-style metrics.

### [Rate Limit Patterns](https://github.com/aluiziolira/rate-limit-patterns)

Distributed rate-limiting library implementing token bucket, leaky bucket, and sliding-window log over local and Redis backends.

- Pushes quota decisions into Redis Lua scripts for atomic check-and-update, closing the race condition that breaks naive check-then-increment limiters across instances.
- Pure-function algorithm core with swappable backends, contract tests verifying local-vs-Redis behavioral equivalence, FastAPI/ASGI integration, configurable fail-open/fail-closed policy.
- Benchmarked at **197K–264K RPS** in-process with microsecond overhead; a multi-instance simulation admitted exactly **100/100** requests under a global limit.

### Performance Labs

Reproducible, benchmark-backed experiments in throughput and memory behavior:

- **[Async Patterns](https://github.com/aluiziolira/async-patterns):** bounded-concurrency HTTP ingestion in Python: sync 130 RPS → async **2,500 RPS** (**20x**), with circuit breakers, retry budgets, connection pooling, and backpressure.
- **[SQL Throughput Challenge](https://github.com/aluiziolira/sql-throughput-challenge):** PostgreSQL bulk-read strategies compared under Docker resource constraints: multiprocessing at **124K rows/sec** (5.3x baseline); async streaming with **~97% lower** peak memory at 1M rows.
- **[Go Books Scraper](https://github.com/aluiziolira/go-scrape-books):** bounded-memory scraping ETL in Go: **2.2M items/sec** in-memory pipeline at 4 allocs/op (**108 items/sec** end-to-end over live HTTP, rate limits respected), constant memory regardless of crawl size, Prometheus metrics.

## Technical Toolbox

| Category | Tools |
| :--- | :--- |
| **Languages** | Python, Go, SQL, Bash |
| **Backend** | FastAPI, Django, Django REST Framework, Pydantic, asyncio, aiohttp, asyncpg, REST API design |
| **Data & Storage** | PostgreSQL, Redis, MongoDB, Kinesis, S3 data lakes (Glue, Athena, Parquet) |
| **AI / ML** | LLM integration (OpenAI, Anthropic), agent evaluation, LLM-judge scoring, scikit-learn, multi-armed bandits |
| **Cloud & DevOps** | AWS (ECS, Lambda, RDS, CloudWatch), Terraform, Docker, GitHub Actions, Bitbucket Pipelines |
| **Quality & Observability** | pytest, mypy strict, ruff, Gitleaks, Prometheus metrics, structured logging, trace-style telemetry |

## Certifications

<p align="left">
<a href="https://www.credly.com/badges/bf2c4386-88a8-4f25-8fe5-c3573b128273"><img src="https://images.credly.com/images/1a634b4e-3d6b-4a74-b118-c0dcb429e8d2/image.png" width="110" height="110" alt="AWS Certified Machine Learning Engineer - Associate"></a>
<a href="https://www.credly.com/badges/f051c585-460d-4f90-9414-6c52228d192d"><img src="https://images.credly.com/images/b9feab85-1a43-4f6c-99a5-631b88d5461b/image.png" width="110" height="110" alt="AWS Certified Developer - Associate"></a>
</p>

- **AWS Certified Machine Learning Engineer – Associate**
- **AWS Certified Developer – Associate**
- **Anthropic:** [MCP: Advanced Topics](https://verify.skilljar.com/c/89absohofk4b) and [Claude Code in Action](https://verify.skilljar.com/c/bkqqi5i5qns6)

## Contact

Happy to talk about distributed systems, database performance, cost engineering, and AI agent infrastructure.

- **Email:** [alumlira@gmail.com](mailto:alumlira@gmail.com)
- **LinkedIn:** [linkedin.com/in/aluiziolira](https://linkedin.com/in/aluiziolira)
- **Location:** Recife, Brazil | Remote
