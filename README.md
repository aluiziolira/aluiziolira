# Aluízio Lira

**Senior Backend Engineer** | Python · AWS · Distributed Systems · PostgreSQL

5+ years in Python and AWS building distributed backend services and high-throughput data pipelines where reliability, latency, and cloud unit economics matter. Beyond architecture and production ownership, I mentor engineers, raise delivery standards, and build AI-assisted workflows with reusable MCP tools.

## Selected Work

- **Search extraction scaling (`ECS Fargate`, `SQS`, `Aurora PostgreSQL`):** Migrated a throttled search-engine service from Lambda and tuned worker concurrency, autoscaling, caching, and DB hot paths, cutting unit cost **~92%** at **4-8x volume**, median job time from **12.8s to 4.1s**, and backlog wait from **~1.3-2.4h to ~2 min**.
- **Platform migration (`AWS Lambda → ECS Fargate`):** Drove the move for continuous workers on a **120M+ requests/day** platform (`SQS`, `SNS`, proxy traffic) via gated production load shifts on shared queues with one-parameter rollback and no consumer gap, cutting total AWS costs **~50%**.
- **Aurora PostgreSQL upgrade (`15.12 → 18.3`):** Led a cross-team upgrade across 33 repos via Terraform and a planned cutover to a fresh cluster (**2M+ records/day**), reclaiming **~75%** initial storage bloat for **~25%** lower monthly DB spend and standardized pooling/alerting.
- **Infrastructure standardization (`Terraform`, `CI/CD`):** Replaced ad-hoc Serverless Framework and CloudFormation setups with reusable Terraform modules and centralized CI/CD pipelines, cutting deployment times **~70%**.

## Portfolio

- **[Async-Patterns Performance Lab](https://github.com/aluiziolira/async-patterns):** Python `asyncio` library with bounded concurrency, circuit breakers, jittered backoff, and backpressure queues (**130 to 2,500 req/s** in benchmarks).
- **[Rate Limit Patterns](https://github.com/aluiziolira/rate-limit-patterns):** Distributed Python rate limiter (Token Bucket, Sliding Window, Leaky Bucket) with atomic **Redis/Lua** `EVALSHA` enforcement and parity contract tests.
- **[Mini Agent Telemetry Lab](https://github.com/aluiziolira/mini-agent-telemetry-lab):** Framework-agnostic **Django/PostgreSQL** observability backend for AI agents with OTel-style spans, idempotent ingestion, async evaluation, and Prometheus metrics.
- **[SQL Throughput Challenge](https://github.com/aluiziolira/sql-throughput-challenge):** Reproducible **PostgreSQL** 1M-row bulk-read benchmark (**124K rows/sec** via multiprocessing, **97%** lower peak memory via async streaming cursors).

## Stack

- **Backend:** Python, Django, Django REST Framework, FastAPI, asyncio
- **Data & persistence:** PostgreSQL, SQLAlchemy, asyncpg, SQL
- **Cloud & delivery:** AWS (ECS Fargate, Lambda, Aurora/RDS, SQS, SNS, S3, Kinesis, Athena), Terraform, Docker, CI/CD
- **Also used:** Go in portfolio systems; scikit-learn for workload prioritization

## Credentials

<p>
<a href="https://www.credly.com/badges/bf2c4386-88a8-4f25-8fe5-c3573b128273"><img src="https://images.credly.com/images/1a634b4e-3d6b-4a74-b118-c0dcb429e8d2/image.png" alt="AWS Certified Machine Learning Engineer - Associate badge" width="125" height="125"></a>
</p>

- **Certification:** [AWS Certified Machine Learning Engineer - Associate](https://www.credly.com/badges/bf2c4386-88a8-4f25-8fe5-c3573b128273) (valid February 2026 - February 2029)
- **Course completions (2026):** [MCP: Advanced Topics](https://verify.skilljar.com/c/89absohofk4b) and [Claude Code in Action](https://verify.skilljar.com/c/bkqqi5i5qns6)

## Contact

- [hi@aluiziolira.dev](mailto:hi@aluiziolira.dev)
- [linkedin.com/in/aluiziolira](https://linkedin.com/in/aluiziolira)
