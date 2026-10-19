# Sovereign AI Systems Landing Page

A unified landing page, interactive systems playground, and deep-dive technical showcase for **IronWarden** and **SearchBoost**, engineered by [Somnerd](https://github.com/Somnerd).

---

## 🏛️ Architecture & Project Overview

This project serves as the joint public portal, benchmark explorer, and live client-side demonstrator for two complementary sovereign AI infrastructure systems:

1. **IronWarden** (`cyan`)
   - **Role**: Sub-microsecond Streaming Security & Privacy Gateway for LLMs.
   - **Key Specs**: Written in bare-metal Rust (Axum / Tokio), `503.2 ns – 821.8 ns` Criterion-audited SSE chunk rehydration, `98.13%` recall across 100k multilingual prompts (`0` false positives on code/SQL), SIMD Aho-Corasick token restoration (`126.0 µs`), and cryptographic HMAC-SHA256 Merkle-audit chaining.
   - **GitHub**: [Somnerd/IronWarden](https://github.com/Somnerd/IronWarden)

2. **SearchBoost** (`violet`)
   - **Role**: Autonomous Cognitive Multi-Tier Search & Grounding Engine.
   - **Key Specs**: React 19 UI, Express 5 API, Rust Warden Relay (Failsafe circuit breaker & GCRA rate limiting), Python ARQ Worker, pgvector (HNSW 768-dim), SearXNG metasearch with Reciprocal Rank Fusion ($k=60$), and 167 automated tests passing across 4 tiers.
   - **GitHub**: [Somnerd/SearchBoost](https://github.com/Somnerd/SearchBoost)

3. **Synergy Stack** (`emerald`)
   - Demonstrates how SearchBoost delegates LLM egress PII scrubbing and audit logging to IronWarden via a shared `searchboost_net` Docker bridge with zero port collisions.

4. **Interactive Demos (`#demos`)** (`amber`)
   - Zero-dependency in-browser laboratories for testing Dual-Track PII redaction (Track A Checksums/Heuristics vs Track B ONNX DistilBERT), GDPR cryptographic shredding (`mcp_PurgeUser`), cross-chunk SSE sliding-window token rehydration, live Reciprocal Rank Fusion ($k=60$) re-ranking, prompt-fence breakout sanitization, and Failsafe circuit-breaker fault injection.

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
