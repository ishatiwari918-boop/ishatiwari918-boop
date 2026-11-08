# Hi, I'm Isha Tiwari 👋

B.Tech CSE student at **UPES** (Batch 2024-2028), building full-stack web applications and developer tools with **AI integration**. I'm looking for **SDE internship** opportunities.

---

## 🚀 Projects

### [CodeMind](https://github.com/ishatiwari918-boop/codemind): AI Assistant for Codebase Q&A
Ask natural-language questions about a codebase and get answers with citations to the exact file, function and line range. It refuses to answer when the code doesn't contain the answer.

- **RAG built from scratch**, without LangChain
- **Hybrid retrieval** (vector + keyword) over function-level chunks parsed with an AST: Hit@1 improved from **56% to 69%** and MRR from **0.72 to 0.79** over vector-only search on a 21-question evaluation set
- **Refusal on unanswerable questions:** correctly refused all 5 in the evaluation set
- **Adaptive query routing** that sets retrieval depth by question complexity, plus a **corrective filter** that drops low-relevance and stale chunks before generation
- **Full-stack, multi-user app:** JWT auth with bcrypt, per-user data isolation, rate limiting and caching, background indexing, and safe GitHub repo import
- **Deployed** on Render with Neon Postgres + pgvector

**Tech:** Node.js · Express · Llama 3.1 8B (via Groq) for routing and answer generation · all-MiniLM-L6-v2 embeddings (384-dim, run locally) · PostgreSQL · pgvector · JWT · Render · Neon

[🔗 Live Demo](YOUR-DEMO-LINK) · [📂 Source Code](https://github.com/ishatiwari918-boop/codemind)

---

### [AgentTrace](https://github.com/ishatiwari918-boop/agenttrace): Observability for LLM Apps 🚧
Shows what every step of an AI app is doing and what it costs, so you can tell which step made an answer slow, wrong or expensive. Built from scratch, with no frameworks hiding the hard parts.

**Working today**
- **TypeScript SDK:** `trace()` and `llm()` wrappers that return your result unchanged and re-throw your errors
- **Nested spans** (including parallel branches) using `AsyncLocalStorage`, so a request becomes a tree
- **Background batching** with retry, exponential backoff with jitter, and a memory cap, so the SDK never blocks or breaks the host app
- **LLM cost tracking:** records model, token counts and estimated cost per call
- **Ingestion API** (Express + PostgreSQL): API keys stored as SHA-256 hashes, validation, batch limits, and duplicate protection so retries never create duplicate spans
- **Measured overhead:** about **3.9 µs mean / 17.3 µs p99** per `trace()` call (20,000 calls, local machine)

**Next:** SDK tests, instrumenting CodeMind as the first real user, a React dashboard with a trace waterfall, and an eval system with a GitHub Action that fails PRs when quality regresses.

**Tech:** TypeScript · Node.js · Express · PostgreSQL · Docker

[📂 Source Code](https://github.com/ishatiwari918-boop/agenttrace)

---

## 🛠️ Skills

**Languages:** ![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black) ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)

**Backend:** ![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white) ![Express.js](https://img.shields.io/badge/Express.js-000000?style=flat&logo=express&logoColor=white)

**Databases:** ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white) · pgvector

**AI / Retrieval:** RAG · Hybrid search (vector + keyword) · Embeddings (all-MiniLM-L6-v2) · LLM integration (Llama 3.1 via Groq) · AST-based code chunking · Retrieval evaluation (Hit@k, MRR) · LLM observability

**Security & DevOps:** JWT authentication · bcrypt · API key hashing · Rate limiting · Docker · Render · Neon

**Core CS:** Data Structures & Algorithms (C++) · DBMS · Object-Oriented Programming

---

## 🔭 Currently Working On

- Building out **AgentTrace**: SDK tests, a trace dashboard, and an eval system
- Instrumenting **CodeMind** with AgentTrace as its first real user

---

## 📫 Connect With Me

- 💼 LinkedIn: [Isha Tiwari](https://www.linkedin.com/in/isha-tiwari-79b179340)
- 📧 Email: [ishatiwari918@gmail.com](mailto:ishatiwari918@gmail.com)
