# Doriel Chiche

**AI / Full-Stack Engineer**

I build LLM-powered products end to end: the model layer, the backend behind it, and the native clients on top. Seven years of production experience, the last three and a half spent making AI features reliable enough to ship — not just impressive in a demo.

---

## What I'm building

**[Leirod](https://leirod.com/download)** — an AI nutrition and coaching app, live on the App Store and Google Play. Designed, built and released solo across four production codebases: a Hono/Node.js API, native iOS (Swift/SwiftUI) and Android (Kotlin/Jetpack Compose) clients, and a Next.js site — carried by 1,500+ automated tests.

Some of the engineering I'm most happy with:

- **Multi-provider LLM routing with real failover.** Every AI feature declares a `primary → fallback → tertiary` chain across Gemini, Claude, GPT and Mistral. Model selection is config-driven — swapping a model is an environment variable, never a deploy. A provider outage degrades the feature instead of breaking the product. Google models are pinned to Vertex AI so EU data residency holds. **20,000+ production calls have gone through the chain.**
- **Vision-based food recognition.** A vision model extracts foods and portions from a photo; the result is matched against the USDA FNDDS and French CIQUAL nutrition databases in PostgreSQL. Full nutritional breakdown in about two seconds per scan, across **1,000+ meal photos in production**.
- **A streaming chat agent with tool use.** Provider-agnostic multi-turn tool loop operating on the user's own data — log a meal, correct a portion, query history. Per-turn credit billing is protected by HMAC-signed, user-bound, short-lived tokens, so billing can never be bypassed from the client.
- **Deterministic scoring, narrative LLM.** Weekly health scores are computed in code, not by a model. The LLM only writes the prose around them. Scores stay reproducible and auditable — a model is the wrong tool for arithmetic anyone might contest.
- **Production ops I own.** GitHub Actions → Linux VPS deploys behind a health-check gate, database migrations with fail-fast backups, encrypted off-site backups, scheduled workers, rate limiting, OAuth 2.0 (Google / Apple), Sentry and PostHog.

I also deliver LLM agents to small businesses — Telegram-based assistants automating back-office and operations workflows, saving each client around ten hours a week.

---

## Stack

**AI/LLM** — LLM application design, agents & tool use, vision models, streaming, prompt engineering, fallback & cost control, RAG · Gemini, Claude, GPT, Mistral, OpenRouter, Vertex AI
**Languages** — TypeScript, JavaScript, Python, Swift, Kotlin, SQL, PHP
**Backend** — Node.js, Hono, PostgreSQL, Drizzle ORM, MongoDB, MySQL/MariaDB
**Frontend** — React, Next.js, Vue, Tailwind CSS
**Mobile** — Swift/SwiftUI, Kotlin/Jetpack Compose, App Store & Play Store releases
**Infrastructure** — Docker, Linux, GitHub Actions, Nginx, Cloudflare, pm2

---

## Elsewhere

- Portfolio — **[doriel.dev](https://doriel.dev)**
- CV — **[doriel.dev/cv/Doriel-Chiche-CV.pdf](https://doriel.dev/cv/Doriel-Chiche-CV.pdf)**
- LinkedIn — **[linkedin.com/in/doriel](https://www.linkedin.com/in/doriel)**
- Email — **doriel.chiche@gmail.com**

Trained at **École 42** (2016–2020). French (native), English (fluent), Hebrew (professional working proficiency).

> The archived repositories below are coursework from my time at 42 — kept for the record. Current work lives in private product repositories; happy to walk through any of it in a conversation.
