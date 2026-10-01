# Hi, I'm Aluizio Lira 👋

**Senior Backend Engineer | Distributed Systems, Data Infrastructure & Applied AI**

I build Python backends and data pipelines, with experience in high-volume AWS workloads, PostgreSQL performance, and cloud cost optimization. My work spans production data-enrichment systems, internal AI tooling, and engineering analytics. I design and develop systems from scratch, work with product and operations teams, and help engineers maintain and extend them.

---

## At a Glance

- **Production scale:** Architected a Lambda-to-ECS migration for infrastructure handling **120M+ requests/day**.
- **Delivery:** Built a functional data-enrichment MVP in **one working day** and evolved it into a production system in **under four weeks**.
- **Team leadership:** Onboarded a new manager and two developers during a transition from five engineers to two, helping rebuild the team and standardize development practices.
- **Core technologies:** Python, PostgreSQL, AWS, Terraform; Go for portfolio systems work.

---

## Selected Engineering Work

- **Production data enrichment:** Architected and delivered an enterprise campaign discovery and data-enrichment platform with retries, deduplication, checkpointing, and resumable execution. Reduced a **5,000-place campaign from approximately 20 hours in early runs to approximately 4 hours** through pipeline and workload optimization, iterating with product and operations teams.
- **Internal AI engineering assistant:** Designed and developed an assistant from scratch with reusable tools and documentation-grounded workflows for engineering investigations and operational tasks. Implemented asynchronous processing, persistent conversations, and context management for follow-up investigations and large inputs.
- **Engineering analytics platform:** Designed and developed a platform from scratch with Python/SQL collection pipelines, PostgreSQL metric history, and reporting APIs. Implemented failure isolation, retries, historical backfills, and idempotent persistence, with reporting rules that distinguish missing data, measured zeros, estimates, and projections.
- **Infrastructure and database optimization:** Delivered a **zero-downtime Lambda-to-ECS migration** with **50% lower AWS infrastructure costs**. Executed a separate controlled Aurora PostgreSQL major-version upgrade for a cluster ingesting **2M+ records/day**, achieving **40% faster analytical queries** and **25% lower operational costs through instance optimization**.
- **Applied ML optimization:** Implemented scikit-learn SGD Regressor payload prioritization with a **20% extraction-rate increase**, and a separate Multi-Armed Bandit optimization with a **35% scraping-efficiency improvement**.

---

## Featured Portfolio Projects

These public projects demonstrate engineering patterns and benchmark results; their measurements describe the documented lab workloads.

### [Mini Agent Telemetry Lab](https://github.com/aluiziolira/mini-agent-telemetry-lab)

An AI-agent observability backend using **Python, Django, Django REST Framework, and PostgreSQL**. Demonstrates idempotent ingestion, immutable run semantics, durable asynchronous processing, boundary validation, and explicit failure handling.

### [Async-Patterns Performance Lab](https://github.com/aluiziolira/async-patterns)

A **Python, asyncio, and aiohttp** lab for bounded concurrency, circuit breakers, retry budgets, backpressure, and graceful shutdown. Documented benchmarks increased throughput from **130 to 2,500 requests/sec**.

### [Go Books Scraper: Streaming ETL](https://github.com/aluiziolira/go-scrape-books)

A **Go and Colly** scraper with worker pools, bounded buffers, LRU deduplication, and Prometheus metrics. The streaming pipeline achieved **2.2M items/sec in an in-memory benchmark**; bounded buffering demonstrates memory control independently of network extraction speed.

### [SQL Throughput Challenge](https://github.com/aluiziolira/sql-throughput-challenge)

A **Python, asyncpg, and PostgreSQL** benchmark comparing bulk-read strategies over one million rows. Multiprocessing achieved **124K rows/sec (5.3× the naive baseline)**; a separate async-streaming strategy reduced memory use by **97%**.

---

## Technical Skills

| Domain | Technologies & Practices |
| :--- | :--- |
| **Backend** | Python, Django, Django REST Framework, FastAPI, asyncio, aiohttp, asyncpg, REST APIs |
| **Data infrastructure** | PostgreSQL, SQL, ETL/ELT, historical backfills, idempotent persistence, data-quality rules |
| **Cloud & delivery** | AWS ECS, Lambda, RDS/Aurora, S3, Kinesis, Glue, Athena; Terraform, Docker, CI/CD |
| **Applied AI & ML** | Tool-using assistants, documentation-grounded workflows, conversation/context management, scikit-learn, Multi-Armed Bandit optimization |
| **Reliability & observability** | Bounded concurrency, retries, checkpointing, circuit breakers, Prometheus, CloudWatch, structured logging |
| **Additional languages** | Go, JavaScript/TypeScript, Bash |

---

## Certifications & Course Completions

<p>
<a href="https://www.credly.com/badges/bf2c4386-88a8-4f25-8fe5-c3573b128273"><img src="https://images.credly.com/images/1a634b4e-3d6b-4a74-b118-c0dcb429e8d2/image.png" alt="AWS Certified Machine Learning Engineer – Associate badge" width="125" height="125"></a>
</p>

- **AWS:** [Certified Machine Learning Engineer – Associate](https://www.credly.com/badges/bf2c4386-88a8-4f25-8fe5-c3573b128273) — active, February 2026–February 2029.
- **Anthropic course completions (2026):** [MCP: Advanced Topics](https://verify.skilljar.com/c/89absohofk4b) and [Claude Code in Action](https://verify.skilljar.com/c/bkqqi5i5qns6).

---

## Connect

Happy to connect and discuss distributed systems, data infrastructure, reliability, and applied AI tooling.

- **Email:** [alumlira@gmail.com](mailto:alumlira@gmail.com)
- **LinkedIn:** [linkedin.com/in/aluiziolira](https://linkedin.com/in/aluiziolira)
