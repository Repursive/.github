# 👋 Welcome to **Repursive**

Repursive transforms unstructured content—PDFs, articles, notes—into ready-to-use artefacts such as action-item checklists, slide decks and tweet threads. Go from **idea → impact** in minutes.

## What Repursive can do for you
- ✅ Turn meeting minutes into clear, assignable **action items**
- 🎞️ Convert blog posts or Markdown into polished **slide decks**
- 🧵 Distil dense research into concise **Twitter/X threads**

## Why Repursive?
1. **Privacy-first** – Repursive manages encrypted LLM API keys centrally, so you don't have to handle secrets yourself.
2. **Frictionless** – Paste text, pick a template, get structured output ready to share.
3. **Modular** – Gateway, Orchestrator, LLM Worker and Processing services scale independently.

## Tech at a Glance
- **Backend**  FastAPI micro-services, async-first, deployed on Google Cloud Run
- **Messaging**  Google Cloud Pub/Sub for event-driven workflows
- **LLM Runtime**  Supports local Ollama models and hosted APIs (OpenAI, Anthropic)
- **Processing**  Containerised extractors (PDF, DOCX) and converters (PDF, PPTX) written in Python
- **Frontend**  React 18 + Tailwind; native iOS app built with SwiftUI
- **Infra-as-Code**  Terraform, GitHub Actions → Cloud Build CI/CD

---
Follow our progress and announcements here on GitHub.

*Made with ❤️  by the Repursive team* 