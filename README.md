<h1 align="center">Maksim Vasić</h1>

<p align="center">
  Software Engineering student at FTN Novi Sad · Software Engineer Apprentice at <b>WolkAbout</b><br/>
  Systems programming · Data engineering · AI agents · Applied ML
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
- **Learning:** core machine learning, computer vision, orchestration and the big-data stack (Spark, Airflow, Scala).
- **Open source:** merged contribution to [SuperPlane](https://github.com/superplanehq/superplane), an event-driven DevOps control plane.

---

### Selected projects

#### AI agents & applied ML

| Project | Description | Stack |
| :--- | :--- | :--- |
| [**the-analyst**](https://github.com/vasicm4/the-analyst) | CLI research assistant that reads a folder of academic papers, extracts claims into a typed schema with mandatory page pointers, detects contradictions between papers, re-runs headline numbers in a sandbox where data is public, and red-teams every logged conclusion. Bounded ReAct agent, BM25 + vector retrieval written from scratch with reciprocal rank fusion, file-based skills, MCP tool servers and a full eval harness for extraction accuracy, cost and latency. | Go · SQLite · MCP |
| [**kws-accent-robustness**](https://github.com/vasicm4/kws-accent-robustness) | Measures the accuracy gap of a 99k-parameter keyword-spotting CNN on 19 consented Serbian-accented speakers versus Speech Commands, with paired speaker-bootstrap CIs. Few-shot fine-tuning recovers 1 point on held-out speakers at no cost on the official set. Shipped as ONNX + FastAPI at 0.19 ms p50 per clip. | PyTorch · MLflow · ONNX · Docker |
| [**pico-gpt**](https://github.com/vasicm4/pico-gpt) | Decoder-only Transformer with hand-written backprop on the GPU: RMSNorm, RoPE, causal Grouped-Query Attention, SwiGLU and AdamW, gradients verified against a PyTorch reference. | Python · CuPy |
| [**black-box-optimization**](https://github.com/vasicm4/black-box-optimization) | Genetic algorithm that tunes neural-network parameters when the error function has no analytic form. | Python |

#### Systems & data

| Project | Description | Stack |
| :--- | :--- | :--- |
| [**forkasm**](https://github.com/vasicm4/forkasm) | Sub-millisecond forking of running WebAssembly sandboxes for branching AI agents. | Rust · Wasmtime · Linux |
| [**hnx-lake**](https://github.com/vasicm4/hnx-lake) | AWS data lake ingesting Hacker News and X streams through a Bronze → Silver → Gold Medallion architecture. | AWS · Python · SQL |
| [**key-value-engine**](https://github.com/vasicm4/key-value-engine) | LSM-tree storage engine with segmented WAL, memtables, SSTables with Merkle validation, size-tiered compaction, LRU cache, Bloom filter, Count-Min Sketch and HyperLogLog. | Go |
| [**aegis-iot**](https://github.com/vasicm4/aegis-iot) | Secure IoT ingestion microservices with hybrid encryption, message signing, rate limiting and Byzantine Fault Tolerant consensus to filter faulty sensors. | C# · .NET 8 · Kubernetes |
| [**ip-system**](https://github.com/vasicm4/ip-system) | Thread-safe, priority-aware task processing engine built on an async producer–consumer model. | C# |

#### Quantitative finance

| Project | Description | Stack |
| :--- | :--- | :--- |
| [**futures-analysis**](https://github.com/vasicm4/futures-analysis) | Ten years of weekly WTI, Brent and NVIDIA prices: white-noise diagnostics (Ljung-Box, ADF, ARCH), AR(1) and random-walk models, half-life analysis and Monte Carlo simulation. Petnica Computational Finance Seminar. | Python · statsmodels |
| [**portfolio-optimization**](https://github.com/vasicm4/portfolio-optimization) | Parallel genetic algorithm that evolves asset allocations to maximise the Sharpe ratio. | C++ |

#### Backend & full-stack

| Project | Description | Stack |
| :--- | :--- | :--- |
| **OmniEMR** | Electronic medical records system for a medical office. | |
| [**visor-inc-voom**](https://github.com/vasicm4/visor-inc-voom) | Cross-platform ride-sharing system with real-time location tracking, driver–passenger matching, JWT auth and end-to-end tests. Team project. | Spring Boot · PostgreSQL · WebSockets · Angular |
| [**chaotic-cupid**](https://github.com/vasicm4/chaotic-cupid) | Real-time matchmaking simulation: a background worker scores and pairs users, and a SignalR hub delivers acknowledged messages. | .NET 9 · SignalR |

Also built: TrustAnchor (X.509 PKI with hierarchical CAs and MFA), a Git-style version control system in Go, a PDF search engine with trie autocomplete and graph-based ranking, and a minimax checkers AI.

---

### Toolbox

| Area | Technologies |
| :--- | :--- |
| **Languages** | Go · Rust · Python · Java · SQL · C++ · C# · TypeScript |
| **Systems** | WebAssembly · Wasmtime · Linux memory management · concurrency · storage engines |
| **Data** | ETL · Medallion architecture · PostgreSQL · SQLite · Apache Druid · time-series analysis |
| **Cloud & infra** | AWS · GCP · Docker · Kubernetes · CI/CD |
| **Backend** | Spring Boot · .NET Core · FastAPI · gRPC · REST · WebSockets · SignalR |
| **AI / ML** | PyTorch · CuPy · ONNX · MLflow · LangChain · MCP · RAG · agent evaluation |
