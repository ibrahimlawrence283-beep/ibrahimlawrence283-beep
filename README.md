# Hi, I'm Lawrence 👋

**AI Engineer & System Architect** bridging quantitative rigor, enterprise governance, and production LLM deployment. I build specialized model systems, real-time middleware safeguards, and low-latency hybrid routing architectures designed for security, finance, and enterprise compliance.

---

## 🛡️ Featured Portfolio Builds

### 1. Hybrid ML + LLM Router & Telemetry Gateway (*Meridian Gateway*)

**Stack:** Python, FastAPI, Streamlit, Scikit-learn, Pandas, Plotly, NumPy, REST APIs

- **Overview:** High-performance enterprise AI gateway acting as an inline proxy between client applications and downstream foundation models (Llama 3.1 8B & GPT-4o) to optimize cost, latency, and financial governance.
- **Core Architecture:**
  - **Hybrid ML Routing Layer:** In-flight ML classifier dynamically categorizes incoming query complexity to route routine prompts to lightweight 8B models and complex reasoning tasks to frontier LLMs.
  - **In-Memory Semantic Cache:** Intercepts redundant queries, returning cached responses with sub-millisecond median latency (p50: 0.01 ms) at $0 API cost.
  - **Financial Governance & Telemetry Dashboard:** Real-time observability UI tracking tail latencies (p50/p95), cache hit distribution (86.7% hit rate under load), API spend, and avoided cost savings converted to local currency (KSh).
- **Key Metrics:** Reduced average query latency to 0.01 ms on cache hits and achieved up to 90% cost savings compared to direct frontier model execution.

---

### 2. Enterprise RAG with RBAC & Eval

**Stack:** Python, FastAPI, Qdrant, sentence-transformers (`all-MiniLM-L6-v2`), BM25 (`rank-bm25`), Docker

- **Overview:** Zero-trust, production-ready retrieval pipeline enforcing Role-Based Access Control (RBAC) directly at the retrieval layer—preventing data leakage and top-k truncation before context reaches the LLM.
- **Core Architecture:**
  - **Pre-Retrieval Policy Engine:** Evaluates role/department clearance before executing search operations.
  - **Dual-Path Hybrid Retrieval:** Executes payload-filtered Qdrant vector search alongside sparse BM25 keyword search, merged via Reciprocal Rank Fusion (RRF).
  - **Decoupled Engine:** Lightweight, CPU-friendly API execution without GPU or third-party LLM key dependencies.
- **Evaluation & Verification:** Achieved 15/15 (100%) RBAC compliance across multi-department adversarial test queries (HR, Finance, Engineering, Legal).

---

### 3. AuraGuard | AI Governance & Safety Middleware Engine

**Stack:** Python, Streamlit, Pandas, Plotly, IBM watsonx.ai integration

- **Overview:** Real-time telemetry, PII redaction tracking, and IP protection middleware operating as an inline security layer for enterprise creative workflows.
- **Core Architecture:**
  - Inbound gateway interception for prompt payloads.
  - Multi-track regex pattern matching to mask high-risk signatures (PII, credentials, network endpoints).
  - Dynamic synthetic masking with a persistent forensic audit ledger (`auraguard_audit.csv`).
- **Value:** Prevents sensitive data leakage before prompts reach downstream foundation models.

---

### 4. Meridian Data Assurance — Risk Triage Engine

**Stack:** Llama 3.2 3B Instruct, Unsloth QLoRA, PEFT, Streamlit, Transformers

- **Overview:** Domain-adapted lightweight LLM specialized for real-time financial, cyber, and operational risk triage.
- **Key Benchmarks & Metrics:**
  - **Fine-Tuning:** 4-bit Unsloth base with r = 16, α = 16 across all 28 layers.
  - **Performance:** Reached final training loss of 0.6565 and domain perplexity of 1.928.
- **Dual Inference Modes:**
  - **Fast Triage:** Low-latency micro-classification into structured severity categories (`CRITICAL`, `HIGH`, `MEDIUM`, `LOW`).
  - **Guided Narrative:** Prefix-forced generation for detailed audit and financial impact summaries.

---

### 5. OrbitGuard AI — Space Situational Awareness Platform

**Stack:** Python, FastAPI, SGP4, Skyfield, LangChain (LCEL), Ollama/Mistral, Next.js 14, Tailwind CSS, shadcn/ui

- **Overview:** Self-hostable, low-resource Space Situational Awareness (SSA) platform giving regional space agencies independent orbital tracking and AI-driven collision-risk reporting, without dependency on foreign SSA feeds or GPU infrastructure. Built for the BeMyApp AI Builders Challenge (August 2026: Advance Space Exploration with AI).
- **Core Architecture:**
  - **Deterministic Physics Layer:** FastAPI backend running SGP4 propagation and Skyfield geodetic calculations to track satellite position, altitude, inclination, and velocity in real time from TLE data.
  - **ARIA Hazard Agent:** LangChain LCEL chain against an on-device, OpenAI-compatible LLM (Ollama/Mistral) that translates raw orbital telemetry into structured, plain-language risk evaluations and mitigation recommendations per satellite.
  - **Edge-Optimized Deployment:** Runs fully offline on commodity hardware (Raspberry Pi 4 or standard server)—no GPU, no constant connectivity required, full data sovereignty for air-gapped environments.
  - **Build-Time AI Architecture:** Scaffolding, dependency management, and pipeline design architected using IBM Bob 2.0 as the primary development tool.
- **Value:** Gives emerging space programs (SANSA, NASRDA, KSA, ESSA, and similar) real-time orbital awareness and conjunction alerts without relying on Space Fence, ESA's SSA Programme, or cloud-dependent infrastructure.

---

## ⚙️ Technical Skills & Toolkit

| Domain | Tools & Frameworks |
|---|---|
| **Model Fine-Tuning & Quantization** | Unsloth, PEFT, QLoRA, Hugging Face Transformers, BitsAndBytes |
| **Search & Retrieval (RAG)** | Qdrant, BM25 (`rank-bm25`), Hybrid Search (RRF), Pre-Retrieval RBAC Filtering |
| **AI Governance & Middleware** | Real-time PII Interception, Synthetic Masking, Regex Filtering, Semantic Caching, Audit Logging, Evaluators |
| **Development & Deployment** | Python, FastAPI, Docker, Streamlit, Pandas, Plotly, Git, REST APIs |
| **Enterprise Cloud & AI Platforms** | IBM watsonx.ai, Google Cloud Vertex AI & Gemini APIs |
| **Aerospace & Simulation** | SGP4 Orbital Propagation, Skyfield, LangChain (LCEL), Ollama, FastAPI, Next.js |

---

## 📫 Connect With Me

- **GitHub:** [@ibrahimlawrence283-beep](https://github.com/ibrahimlawrence283-beep)
- **LinkedIn:** [Lawrence Ibrahim](https://www.linkedin.com/in/lawrence-ibrahim-b54578351)
