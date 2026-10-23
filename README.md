# Hi, I'm Pedro Guerra 👋

**Software Engineer · Backend & AI Integration** — Recife, Brazil · open to remote and relocation

I build backend systems and put LLMs to work inside real products: retrieval, agents, evaluation and the guardrails that keep them honest. Currently a Software Engineer at **Coopanest-PE**, working on the company ERP (PHP/Laravel/MySQL), where I shipped an OCR pipeline with the Gemini API that automates billing documents. Postgraduate student in **Deep Learning**; B.Sc. in Computer Science (CESAR, Recife).

**Stack** &nbsp; Python · FastAPI · PHP/Laravel · TypeScript/Node.js · PostgreSQL + pgvector · Supabase · MongoDB · Docker · AWS · Terraform · LLMs (OpenAI, Anthropic, Gemini) · LangChain · LangSmith

---

## Featured projects

### [Flyer](https://github.com/Warpedro1/flyer-back) — event discovery with an AI taste agent · [live](https://flyer-inky.vercel.app)
FastAPI + Supabase backend and React frontend for finding and joining local events.
- LLM "taste agent" turns free-text answers and event descriptions into pt-BR keywords; **pgvector embeddings** match people to events, with a deterministic fallback when the model fails
- Waitlist with "call next", **JWT-signed QR check-in**, trophies, moderation, rate limiting (Upstash Redis), Postgres RLS
- Apify ETL for the event catalog, LangSmith tracing, deployed as serverless on Vercel
- **~1,050 automated tests** (669 pytest + 381 Vitest) · [frontend repo](https://github.com/Warpedro1/flyer)

### [actually](https://github.com/Warpedro1/actually) — live fact-checking for a presidential debate
Monorepo (Next.js, TypeScript) that listens to a live broadcast, extracts checkable claims and publishes short alerts — **always with a source**.
- Pipeline: streaming STT (Deepgram) → claim extraction → hybrid retrieval over fact-checks, official indicators and documents (pgvector + full-text, RRF) with a penalized web fallback → verification → scoring
- Human-in-the-loop editor approval; DB-level guarantee that a correction without a verified source can't be published
- Labeled **eval set** measuring precision, false alarms and p50/p95 latency; threshold sweep without calling models

### [agentic-sdr](https://github.com/Warpedro1/agentic-sdr) — WhatsApp SDR bot that books meetings
Deterministic lead qualification and scheduling over WhatsApp (Twilio, Meta Cloud API, Z-API), built as the measurable baseline for a future AI agent.
- Pure state machine (`handle()` does no I/O, enforced by tests) with an engine that executes effects; every reply comes from a reviewed message catalog
- Multi-tenant Postgres with tenant isolation in the schema, double-booking prevented by row locks plus a partial unique index, outbox delivery to a Laravel CRM
- **456 tests** (pytest)

### [tf-eks-k8s](https://github.com/Warpedro1/tf-eks-k8s) — CI/CD to Amazon EKS with Terraform
Infrastructure as code for CodePipeline → CodeBuild → ECR → EKS, building and deploying a containerized app on every push.

### [DL-classes](https://github.com/Warpedro1/DL-classes) — recorded lectures → study kits
Turns Deep Learning lecture transcripts into summaries, active-recall flashcards and a podcast per class: *4h of lecture into 20 min of reading.*

---

## Let's talk
[LinkedIn](https://www.linkedin.com/in/pedro-o-guerra) · warpedro1@gmail.com · English (full professional) · Portuguese (native)
