<h1 align="center">Maksim Vasić</h1>

<p align="center">
  Software Engineering student at FTN Novi Sad · Software Engineer Apprentice at <b>WolkAbout</b><br/>
  Systems programming · Data engineering · Distributed systems · AI agents
</p>

<p align="center">
  <a href="https://vasicm4.github.io">Portfolio</a> ·
  <a href="https://www.linkedin.com/in/maksim-vasic-066762245/">LinkedIn</a> ·
  <a href="https://leetcode.com/u/vasicm4/">LeetCode</a>
</p>

---

### Spotlight: forkasm

**[forkasm](https://github.com/vasicm4/forkasm)** is a Rust library that forks a *running* WebAssembly sandbox (memory, globals, WASI state and filesystem) in about **100 µs**, many ways and many levels deep, so an AI agent can branch mid-task, explore alternatives in parallel and keep the best path.

- **99 µs** median fork for a 64 MiB sandbox: 6.3× faster than a process `fork()` and roughly 1,500× faster than published VM-branching systems
- Fork cost scales with pages written, not memory size: a 1 GiB sandbox still spawns in 54 µs, and idle branches cost under 1 KiB
- Copy-on-write memfd layers with dirty-page tracking via userfaultfd write-protect and `PAGEMAP_SCAN`, plus an in-crate, fully clonable WASI implementation
- Forks a CPython interpreter between statements in under 1 ms; the demo runs 8 competing approaches in parallel and keeps the fastest correct one

[Repository](https://github.com/vasicm4/forkasm) · [Benchmarks](https://github.com/vasicm4/forkasm/blob/main/BENCHMARKS.md) · [Blog post](https://vasicm4.github.io/#/blog/forkasm)

---

### Currently

- **At WolkAbout:** validating industrial IoT ingestion pipelines with a device simulator, integrating OPC device services, and building an agentic AI workflow (LangChain + MCP) that grounds LLMs on live telemetry.
- **Building:** Analyst, an agentic research engine in Go with hybrid retrieval (BM25 + vector search), MCP integrations and execution sandboxes.
- **Learning:** orchestration and the big-data stack (Spark, Airflow, Scala).

---

### Selected projects

#### Systems & data

| Project | Description | Stack |
| :--- | :--- | :--- |
| [**forkasm**](https://github.com/vasicm4/forkasm) | Sub-millisecond forking of running WebAssembly sandboxes for branching AI agents. | Rust · Wasmtime · Linux |
| [**hnx-lake**](https://github.com/vasicm4/hnx-lake) | AWS data lake ingesting Hacker News and X streams through a Bronze → Silver → Gold Medallion architecture. | AWS · Python · SQL |
| [**key-value-engine**](https://github.com/vasicm4/key-value-engine) | LSM-tree storage engine with segmented WAL, memtables, SSTables with Merkle validation, size-tiered compaction, LRU cache, Bloom filter, Count-Min Sketch and HyperLogLog. | Go |
| [**aegis-iot**](https://github.com/vasicm4/aegis-iot) | Secure IoT ingestion microservices with hybrid encryption, message signing, rate limiting and Byzantine Fault Tolerant consensus to filter faulty sensors. | .NET 8 · Docker · Kubernetes |
| [**IP-System**](https://github.com/vasicm4/IP-System) | Thread-safe, priority-aware task processing engine built on an async producer–consumer model. | C# |

#### AI, ML & quantitative finance

| Project | Description | Stack |
| :--- | :--- | :--- |
| [**pico-gpt**](https://github.com/vasicm4/pico-gpt) | Decoder-only Transformer with hand-written backprop on the GPU: RMSNorm, RoPE, causal Grouped-Query Attention, SwiGLU and AdamW, gradients verified against a PyTorch reference. | Python · CuPy |
| [**futures-analysis**](https://github.com/vasicm4/futures-analysis) | Ten years of weekly WTI, Brent and NVIDIA prices: white-noise diagnostics (Ljung-Box, ADF, ARCH), AR(1) and random-walk models, half-life analysis and Monte Carlo simulation. Petnica Computational Finance Seminar. | Python · statsmodels |
| [**portfolio-optimization**](https://github.com/vasicm4/portfolio-optimization) | Parallel genetic algorithm that evolves asset allocations to maximise the Sharpe ratio. | C++ |
| [**black-box-optimization**](https://github.com/vasicm4/black-box-optimization) | Genetic algorithm that tunes neural-network parameters when the error function has no analytic form. | Python |

#### Backend & full-stack

| Project | Description | Stack |
| :--- | :--- | :--- |
| [**visor-inc-voom**](https://github.com/vasicm4/visor-inc-voom) | Cross-platform ride-sharing system with real-time location tracking, driver–passenger matching, JWT auth and end-to-end tests. | Spring Boot · PostgreSQL · WebSockets · Angular |
| [**chaotic-cupid**](https://github.com/vasicm4/chaotic-cupid) | Real-time matchmaking simulation: a background worker scores and pairs users, and a SignalR hub delivers acknowledged messages. | .NET 9 · SignalR |

Also built: TrustAnchor (X.509 PKI with hierarchical CAs, MFA and RBAC) and Graph Visualiser (plugin-based graph explorer).

---

### In progress

- **Analyst** – agentic research engine for extracting and backtesting econometric strategies
- **NickelDB** – relational database engine in Rust
- **Governo** – simulation framework using synthetic populations to help local governments test policy decisions
- **OmniEMR** – electronic medical records system for a medical office

---

### Toolbox

| Area | Technologies |
| :--- | :--- |
| **Languages** | Rust · Go · Python · Java · SQL · C++ · C# · TypeScript |
| **Systems** | WebAssembly · Wasmtime · Linux memory management · concurrency · storage engines |
| **Data** | ETL · Medallion architecture · PostgreSQL · Apache Druid · time-series analysis · vector databases |
| **Cloud & infra** | AWS · GCP · Docker · Kubernetes · CI/CD |
| **Backend** | Spring Boot · .NET Core · gRPC · REST · WebSockets · SignalR |
| **AI / ML** | PyTorch · NumPy · CuPy · LangChain · MCP · RAG · genetic algorithms |
