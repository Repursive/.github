# 👋 Welcome to **Repursive**

_Local-first AI assistant that turns your raw text into structured artefacts you can use straight away._

## Why Repursive?
We all jot ideas in free-form text—meeting minutes, blog drafts, messy research notes. Repursive converts that into:

- ✅ **Action-item checklists** from meeting notes
- 🎞️ **Slide decks** from Markdown/blog posts
- 🧵 **Twitter/X threads** from research summaries

All powered by on-device large-language models (via [Ollama](https://ollama.ai/) or your favourite self-hosted provider)—so your data never leaves your machine unless you want it to.

## Repositories
| Layer | Tech | Repo |
|-------|------|------|
| API Gateway | FastAPI | [repursive-gateway](https://github.com/Repursive/repursive-gateway) |
| LLM Worker | FastAPI + LangChain/LlamaIndex | [repursive-worker](https://github.com/Repursive/repursive-worker) |
| Exporter | FastAPI + python-pptx/Pandas | [repursive-exporter](https://github.com/Repursive/repursive-exporter) |
| Web SPA | React 18 + Tailwind | [repursive-frontend](https://github.com/Repursive/repursive-frontend) |
| iOS | SwiftUI | [repursive-ios](https://github.com/Repursive/repursive-ios) |

## Quick Start (dev)
```bash
# Prerequisite: run a local LLM
ollama run llama3

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
- [ ] Offline iOS support
- [ ] Cloud Run production deployment

---
MIT License 