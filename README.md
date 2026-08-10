# Hi, I'm Lawrence 👋

**AI Engineer** bridging quantitative rigor, enterprise governance, and production LLM deployment. I build specialized, domain-adapted model systems, real-time middleware safeguards, and secure retrieval architectures designed for security, finance, and enterprise compliance.

---

## 🛡️ Featured Portfolio Builds

### 1. [Enterprise RAG with RBAC & Eval](https://github.com/ibrahimlawrence283-beep/enterprise-rag-rbac)
**Stack:** Python, FastAPI, Qdrant, sentence-transformers (`all-MiniLM-L6-v2`), BM25 (`rank-bm25`), Docker

* **Overview:** Zero-trust, production-ready retrieval pipeline enforcing Role-Based Access Control (RBAC) directly at the retrieval layer—preventing data leakage and top-$k$ truncation before context reaches the LLM.
* **Core Architecture:**
  * **Pre-Retrieval Policy Engine:** Evaluates role/department clearance before executing search operations.
  * **Dual-Path Hybrid Retrieval:** Executes payload-filtered Qdrant vector search alongside sparse BM25 keyword search, merged via Reciprocal Rank Fusion (RRF).
  * **Decoupled Engine:** Lightweight, CPU-friendly API execution without GPU or third-party LLM key dependencies.
* **Evaluation & Verification:** Achieved **15/15 (100%) RBAC compliance** across multi-department adversarial test queries (HR, Finance, Engineering, Legal).

---

### 2. AuraGuard | AI Governance & Safety Middleware Engine
**Stack:** Python, Streamlit, Pandas, Plotly, IBM watsonx.ai integration

* **Overview:** Real-time telemetry, PII redaction tracking, and IP protection middleware operating as an inline security layer for enterprise creative workflows.
* **Core Architecture:**
  * Inbound gateway interception for prompt payloads.
  * Multi-track regex pattern matching to mask high-risk signatures (PII, credentials, network endpoints).
  * Dynamic synthetic masking with a persistent forensic audit ledger (`auraguard_audit.csv`).
* **Value:** Prevents sensitive data leakage before prompts reach downstream foundation models.

---

### 3. Meridian Data Assurance — Risk Triage Engine
**Stack:** Llama 3.2 3B Instruct, Unsloth QLoRA, PEFT, Streamlit, Transformers

* **Overview:** Domain-adapted lightweight LLM specialized for real-time financial, cyber, and operational risk triage.
* **Key Benchmarks & Metrics:**
  * **Fine-Tuning:** 4-bit Unsloth base with $r = 16, \alpha = 16$ across all 28 layers.
  * **Performance:** Reached final training loss of **0.6565** and domain perplexity of **1.928**.
* **Dual Inference Modes:**
  * **Fast Triage:** Low-latency micro-classification into structured severity categories (`CRITICAL`, `HIGH`, `MEDIUM`, `LOW`).
  * **Guided Narrative:** Prefix-forced generation for detailed audit and financial impact summaries.

---

## ⚙️ Technical Skills & Toolkit

| Category | Technologies & Frameworks |
| :--- | :--- |
| **Model Fine-Tuning & Quantization** | Unsloth, PEFT, QLoRA, Hugging Face Transformers, BitsAndBytes |
| **Search & Retrieval (RAG)** | Qdrant, BM25 (`rank-bm25`), Hybrid Search (RRF), Pre-Retrieval RBAC Filtering |
| **AI Governance & Middleware** | Real-time PII Interception, Synthetic Masking, Regex Filtering, Audit Logging, Evaluators |
| **Development & Deployment** | Python, FastAPI, Docker, Streamlit, Pandas, Plotly, Git, REST APIs |
| **Enterprise Cloud & AI Platforms** | IBM watsonx.ai, Google Cloud Vertex AI & Gemini APIs |

---

## 📬 Connect With Me

* **GitHub:** [@ibrahimlawrence283-beep](https://github.com/ibrahimlawrence283-beep)
* **LinkedIn:** [Lawrence Ibrahim](https://www.linkedin.com/in/lawrence-ibrahim)
