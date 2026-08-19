# Hi, I'm Lawrence 👋

**AI Engineer & System Architect** bridging quantitative rigor, enterprise governance, and production LLM deployment. I build specialized model systems, real-time middleware safeguards, and low-latency hybrid routing architectures designed for security, finance, and enterprise compliance.

**At a glance:** 90% LLM cost reduction via hybrid routing · 100% RBAC compliance on adversarial retrieval tests · sub-millisecond cache latency at $0 marginal cost · 4-bit domain-adapted LLM in production triage use

---

## 🛡️ Featured Portfolio Builds

### 1. Meridian Gateway — Hybrid ML + LLM Router & Telemetry Gateway
**Why it matters:** Enterprises overpay for LLM inference by routing every query to a frontier model. This gateway decides, per-query, whether a task needs GPT-4o-level reasoning or can be handled by a cheaper local model — cutting spend without touching output quality.

**Stack:** Python, FastAPI, Streamlit, Scikit-learn, Pandas, Plotly, NumPy, REST APIs

- **Hybrid ML Routing Layer:** An in-flight ML classifier scores incoming query complexity and routes routine prompts to a lightweight 8B model, reserving Llama 3.1 8B / GPT-4o for genuinely complex reasoning.
- **In-Memory Semantic Cache:** Intercepts redundant queries, returning cached responses at sub-millisecond median latency (p50: 0.01 ms) and $0 API cost.
- **Financial Governance Dashboard:** Real-time observability tracking tail latencies (p50/p95), cache hit distribution, API spend, and cost savings converted to KES.
- **Result:** 86.7% cache hit rate under load; up to 90% cost savings vs. direct frontier-model calls.

[🔗 Repo](#) · [▶️ Demo](#)

---

### 2. Enterprise RAG with RBAC & Eval
**Why it matters:** Most RAG demos ignore who's allowed to see what. This pipeline enforces access control *before* retrieval, so a support agent's query can never surface finance or legal documents — a hard requirement for any enterprise deployment, not a nice-to-have.

**Stack:** Python, FastAPI, Qdrant, sentence-transformers (`all-MiniLM-L6-v2`), BM25 (`rank-bm25`), Docker

- **Pre-Retrieval Policy Engine:** Evaluates role/department clearance *before* executing any search — leakage is prevented at the query level, not filtered after the fact.
- **Dual-Path Hybrid Retrieval:** Dense vector search (Qdrant) merged with sparse BM25 keyword search via Reciprocal Rank Fusion for higher recall.
- **Decoupled Engine:** CPU-friendly, no GPU or third-party LLM key dependency required to run retrieval.
- **Result:** 15/15 (100%) RBAC compliance across multi-department adversarial test queries (HR, Finance, Engineering, Legal).

[🔗 Repo](#) · [▶️ Demo](#)

---

### 3. AuraGuard — AI Governance & Safety Middleware Engine
**Why it matters:** Employees pasting client data into public AI tools is one of the most common — and least defended-against — data leaks in modern enterprises. AuraGuard sits inline and stops sensitive data from ever reaching a downstream model.

**Stack:** Python, Streamlit, Pandas, Plotly, IBM watsonx.ai integration

- **Inbound gateway interception** of prompt payloads before they reach any foundation model.
- **Multi-track regex pattern matching** to detect and mask high-risk signatures — PII, credentials, network endpoints.
- **Dynamic synthetic masking** with a persistent forensic audit trail (`auraguard_audit.csv`) for compliance review.
- **Result:** Sensitive data is intercepted and neutralized before it can leave the organization's perimeter.

[🔗 Repo](#) · [▶️ Demo](#)

---

### 4. Meridian Data Assurance — Risk Triage Engine
**Why it matters:** Generic LLMs don't know what "critical" means in a specific financial or cyber-risk context. This is a small, fast model fine-tuned specifically to triage incidents by severity — cheap enough to run continuously, sharp enough to trust for first-pass classification.

**Stack:** Llama 3.2 3B Instruct, Unsloth QLoRA, PEFT, Streamlit, Transformers

- **Fine-Tuning:** 4-bit Unsloth base, LoRA rank 16 / alpha 16 across all 28 layers.
- **Performance:** Final training loss of 0.6565; domain perplexity of 1.928 *(down from a substantially higher baseline perplexity on the un-tuned base model — model is measurably more confident on in-domain risk language)*.
- **Fast Triage mode:** Low-latency micro-classification into structured severity categories (`CRITICAL`, `HIGH`, `MEDIUM`, `LOW`).
- **Guided Narrative mode:** Prefix-forced generation for detailed audit and financial-impact summaries, for when a human needs the full story, not just a label.

[🔗 Repo](#) · [▶️ Demo](#)

---

## ⚙️ Technical Skills & Toolkit

| Domain | Tools & Frameworks |
|---|---|
| **Model Fine-Tuning & Quantization** | Unsloth, PEFT, QLoRA, Hugging Face Transformers, BitsAndBytes |
| **Search & Retrieval (RAG)** | Qdrant, BM25 (`rank-bm25`), Hybrid Search (RRF), Pre-Retrieval RBAC Filtering |
| **AI Governance & Middleware** | Real-time PII Interception, Synthetic Masking, Regex Filtering, Semantic Caching, Audit Logging, Evaluators |
| **Development & Deployment** | Python, FastAPI, Docker, Streamlit, Pandas, Plotly, Git, REST APIs |
| **Enterprise Cloud & AI Platforms** | IBM watsonx.ai, Google Cloud Vertex AI & Gemini APIs |

---

## 🚀 R&D / Exploratory Builds

*Projects outside my core security/governance focus, built to test how fast I can pick up an unfamiliar technical domain.*

### OrbitGuard AI — Space Situational Awareness Platform
Self-hostable, low-resource SSA platform giving regional space agencies independent orbital tracking and AI-driven collision-risk reporting, without dependency on foreign SSA feeds or GPU infrastructure. Built for the BeMyApp AI Builders Challenge (August 2026: Advance Space Exploration with AI).

**Stack:** Python, FastAPI, SGP4, Skyfield, LangChain (LCEL), Ollama/Mistral, Next.js 14, Tailwind CSS, shadcn/ui

- **Deterministic Physics Layer:** FastAPI backend running SGP4 propagation and Skyfield geodetic calculations to track satellite position, altitude, inclination, and velocity in real time from TLE data.
- **ARIA Hazard Agent:** LangChain LCEL chain against an on-device LLM (Ollama/Mistral) that translates raw orbital telemetry into structured, plain-language risk evaluations and mitigation recommendations per satellite.
- **Edge-Optimized Deployment:** Runs fully offline on commodity hardware (Raspberry Pi 4 or standard server) — no GPU, no constant connectivity required, full data sovereignty for air-gapped environments.
- **Value:** Gives emerging space programs (SANSA, NASRDA, KSA, ESSA, and similar) real-time orbital awareness and conjunction alerts without relying on Space Fence, ESA's SSA Programme, or cloud-dependent infrastructure.

[🔗 Repo](#) · [▶️ Demo](#)

---

## 📫 Connect With Me

- **GitHub:** [@ibrahimlawrence283-beep](https://github.com/ibrahimlawrence283-beep)
- **LinkedIn:** [Lawrence Ibrahim](#)
