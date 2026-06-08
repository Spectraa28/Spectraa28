# Hey, I'm Sonu (Spectra) 👋

I'm a **Backend + ML Engineer** who came up through Java and Spring Boot before deliberately moving into ML infrastructure. That background shapes how I think about AI: not just whether the model is accurate, but what happens when a worker crashes mid-embedding, how failures propagate across language boundaries, and what the monitoring should look like at 3am.

I go deep before going wide. I wrote backpropagation in NumPy before touching PyTorch. I built BM25 retrieval from scratch before using a library. Every project I ship has Docker, health endpoints, Prometheus metrics, and documented failure modes — not because someone asked, but because that's what production-ready actually means.

---

## 🚀 What I've Built

### 🔐 [LexGuard](https://github.com/Spectraa28/LexGuard) — Legal Document Intelligence API
> Java · Spring Boot · Python · FastAPI · RabbitMQ · pgvector · Prometheus · Grafana · Docker

Enterprise document ingestion + RAG retrieval pipeline with full observability and security hardening.
- Transactional Outbox pattern across Java + Python — **zero document loss** under worker crashes
- Background supervisor with staged rollback (EMBEDDING→PARSED→UPLOADED) using `FOR UPDATE SKIP LOCKED` — **one failure can't block 49 concurrent recoveries**
- SHA-256 API auth, SlowAPI rate limiting, prompt injection defense with Pydantic regex rejection
- Prometheus Histogram (p99 **0.18s** idle / **0.48s** concurrent), Grafana dashboard, correlation ID threading
- RAG retrieval score **0.6233** on real ISO 27001 legal text (pgvector HNSW, 148 vectors)

🔗 **[Live recruiter demo + /demo/query endpoint](https://sonuverma.vercel.app/)**

---

### 📊 [Financial RAG API](https://github.com/Spectraa28/financial-rag-api) — SEC Document Intelligence
> Python · MiniLM · BM25 · Llama 3.3 70B · FastAPI · MLflow · Prometheus · Docker

Layout-aware retrieval pipeline over Apple + Microsoft 10-K SEC filings.
- Rebuilt retrieval from scratch: pure semantic → BM25 + dense hybrid (alpha=0.7), **Context Recall 0 → 1.0**
- Built `TableToNaturalLanguage` converter — made XBRL financial tables (previously 0% retrievable) semantically searchable
- Validated across **30 manually curated QA pairs**: Faithfulness 0.82, Context Recall 1.0, top score 0.8082
- Deployed on HuggingFace Spaces with Qdrant Cloud (ephemeral filesystem fix)

🔗 **[Live on HuggingFace Spaces](https://sonuverma.vercel.app/)**

---

### ⚡ [LLM Cost Router](https://github.com/Spectraa28/LLM-Cost-Router) — 3-Layer Routing Pipeline
> Python · FastAPI · FAISS · Redis · TF-IDF · Logistic Regression · Docker

Routes LLM queries through semantic cache → ML classifier → LLM fallback to minimize API spend.
- **93.19% cost reduction**, **87% cache hit rate**, **100% routing accuracy** across benchmark suite
- SemanticCache: FAISS + Redis (threshold 0.88), graceful in-memory degradation on Redis failure
- Classifier: TF-IDF + Logistic Regression on 450 weakly-supervised samples — sub-millisecond inference
- Deployed on Render

---

### 🗂️ [TaskFlow](https://github.com/Spectraa28/TaskManager) — Task Orchestration API
> Java · Spring Boot 4.0 · PostgreSQL · Redis · RabbitMQ · WebSockets · JWT · Gemini AI · Docker

Production task management backend — live on Render.
- JWT auth + refresh tokens, AOP role system, async processing (RabbitMQ), real-time WebSockets, Gemini AI integration

---

## 🛠️ Tech Stack

**Gen AI / LLMs**
`RAG Pipelines` `Vector Search` `pgvector` `FAISS` `ChromaDB` `LLM APIs` `Prompt Engineering` `Semantic Caching` `HuggingFace` `SentenceTransformers`

**Classical ML**
`PyTorch` `XGBoost` `scikit-learn` `TF-IDF` `Logistic Regression` `MLflow` `SHAP` `Drift Detection` `Backprop from scratch`

**Backend**
`FastAPI` `Spring Boot` `RabbitMQ` `WebSockets` `JWT` `REST APIs`

**Infra & Observability**
`Docker` `AWS (EC2, S3)` `Prometheus` `Grafana` `Git` `Linux (Arch, btw)`

**Languages**
`Python` `Java` `SQL`

---

## 📊 GitHub Stats

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=Spectraa28&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=true)
![Streak](https://nirzak-streak-stats.vercel.app/?user=Spectraa28&theme=tokyonight&hide_border=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Spectraa28&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=true&layout=compact)

---

## 🌐 Find Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/sonu-verma28)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://sonuverma.vercel.app/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:tannsonuverma@gmail.com)

---

> *"I find where the system breaks under real conditions and engineer it out."*
