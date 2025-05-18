# Repursive

Local-first AI assistant that turns raw notes, articles, and research into immediately useful artefacts — action-item checklists, slide decks, and tweet threads — powered by on-device large-language models.

## Why Repursive?
We capture ideas in free-form text but need structured outputs to act on them. Repursive bridges that gap without handing your data to cloud LLM providers.

| Input | Output | Example |
|-------|--------|---------|
| Meeting minutes | Checklist of next actions | "👏 We should…" → ✅ tasks |
| Blog draft | Google Slides deck | Each H2 becomes a slide |
| Research notes | Twitter/X thread | Concise 280-char tweets |

## High-Level Architecture
| Layer | Tech | Repository |
|-------|------|-----------|
| API Gateway | FastAPI | [repursive-gateway](https://github.com/Repursive/repursive-gateway) |
| LLM Worker | FastAPI + LangChain / LlamaIndex | [repursive-worker](https://github.com/Repursive/repursive-worker) |
| Exporter | FastAPI + python-pptx/Pandas | [repursive-exporter](https://github.com/Repursive/repursive-exporter) |
| Web SPA | React 18 + Tailwind | [repursive-frontend](https://github.com/Repursive/repursive-frontend) |
| iOS | SwiftUI | [repursive-ios](https://github.com/Repursive/repursive-ios) |

Each service lives in its own repo for clarity and lightweight CI.

## Quick Start (Dev)
```bash
# Prerequisite: run a local LLM (e.g. `ollama run llama3`)

# Gateway
uvicorn gateway.main:app --reload --port 8000
# Worker
uvicorn worker.main:app --reload --port 8001
# Exporter
uvicorn exporter.main:app --reload --port 8002
# Frontend
cd frontend && pnpm dev
```

## Roadmap
- [ ] End-to-end MVP (meeting notes → checklist)
- [ ] Offline mobile support (SwiftUI)
- [ ] Cloud Run production deployment

---
MIT Licence 