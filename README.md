# Sovereign AI Systems Landing Page

A unified landing page and deep-dive technical showcase for **IronWarden** and **SearchBoost**, engineered by [Nikolas Alexandrakis](https://github.com/Somnerd).

---

## 🏛️ Architecture & Project Overview

This project serves as the joint public portal and technical architecture explorer for two complementary sovereign AI infrastructure systems:

1. **IronWarden** (`cyan`)
   - **Role**: Microsecond-latency Security & Privacy Gateway for LLMs.
   - **Key Specs**: Written in Rust, `<0.07ms` P95 latency overhead, ~18MB RAM footprint, SIMD Aho-Corasick PII scrubbing, cryptographic HMAC-SHA256 Merkle-audit chaining.
   - **GitHub**: [Somnerd/IronWarden](https://github.com/Somnerd/IronWarden)

2. **SearchBoost** (`violet`)
   - **Role**: Cognitive Multi-Tier Search & Grounding Engine.
   - **Key Specs**: React 19 UI, Express 5 API, Rust Warden Relay, Python ARQ Worker, pgvector (HNSW 768-dim), SearXNG metasearch, sovereign port collision immunity.
   - **GitHub**: [Somnerd/SearchBoost](https://github.com/Somnerd/SearchBoost)

3. **Synergy Stack** (`emerald`)
   - Demonstrates how SearchBoost delegates LLM egress PII scrubbing and audit logging to IronWarden via a shared `searchboost_net` Docker bridge.

---

## 🚀 Running Locally

The landing page is fully self-contained in `index.html` with zero mandatory build steps. You can run it immediately in any of the following ways:

### Option 1: Direct File
Open `index.html` directly in any web browser:
```powershell
start index.html
```

### Option 2: Vite Dev Server
```bash
npm install
npm run dev
```

### Option 3: Python Simple Server
```bash
python -m http.server 4000
```
Then navigate to `http://localhost:4000`.
