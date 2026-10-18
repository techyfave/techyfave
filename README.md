# Hi, I'm Favour 👋

**AI Engineer · AI Agent Builder · Backend Engineer · Full Stack Developer · Technical Co-Founder**

I build AI agents and LLM-powered products, and the production-grade APIs and systems behind them. Co-founded [FGP Solutions](https://fgpsolutions.co) in 2026, where I serve as Lead Backend Developer and Technical Architect across multiple product lines.

Primary stack is **Python/Django** — also proficient in **Node.js/Express** for full stack delivery. I integrate LLMs (Anthropic Claude, OpenAI) as core product features, not just tooling.

---

## 🌱 Currently Building

### [AgroLens AI](https://github.com/techyfave/AgroLens-AI) — AI-Powered Crop Intelligence

Building an end-to-end platform that turns crop imagery into practical health insights. It brings together applied AI, product engineering, and production-ready delivery—more to come as development progresses.

---

## 🚀 Selected Work

### [Épreuve](https://epreuve.site) — Job-Readiness Assessment & Certification Platform

A live platform where candidates take timed, server-enforced assessments across 10 skill areas (cognitive, technical, coding and workplace), get AI grading and coaching, and earn proctored certificates that employers can verify.

**[Try it live](https://epreuve.site) · [Public API docs](https://epreuve.site/api/docs) · [View source](https://github.com/techyfave/epreuve)**

- AI coach: one structured LLM call per attempt grades written answers against a hiring rubric and builds a study plan, with provider fallback (OpenRouter → Gemini → Ollama) so every attempt is still scored if a model is down
- Sandboxed Python code runner (scrubbed environment, audit hooks, resource limits) scoring hidden tests with partial credit
- Proctored certification: integrity signals (tab switches, full-screen exits, second screens, pasting) become a risk level; high-risk attempts go to a human review queue; certificates verify publicly by code
- Company assessment invites, admin dashboard, Paystack payments verified server-side with signed webhooks, email confirmation codes
- 200+ automated tests on SQLite and PostgreSQL · Alembic migrations · public and admin-only API docs
- **Stack:** FastAPI · SQLAlchemy · PostgreSQL (Neon) · React + TypeScript · Gemini / OpenRouter · Paystack · Resend · Render

### [FGP Hiring Signal](https://fgpsolutions.co) — AI-Native Hiring Tool

An AI-native hiring tool that extracts structured, cited hiring signals from job descriptions and candidate materials — with a human-in-the-loop review queue before any decision is acted on.

- 6-step AI reasoning chain (signals → strengths → risks → counter-hypotheses → follow-up questions → synthesis)
- Pydantic schema validation + auto-repair logic + immutable audit log
- CI-enforced eval gates: ≥85% signal accuracy · ≥95% citation grounding rate · <2% schema violations
- **Stack:** Django Ninja · Anthropic Claude API · Redis/RQ · PostgreSQL · HTMX · TailwindCSS

### [LiveHomeTour API](https://livehometour-api.onrender.com/docs/) — Real Estate Video Tour Backend

A real estate platform enabling live agent-guided property video tours with agent-controlled playback, real-time client chat, and automated agent assignment by proximity.

**[Explore the API reference](https://livehometour-api.onrender.com/docs/) · [View backend source](https://github.com/techyfave/livehometour-api)**

- Multi-role auth (CLIENT / AGENT / ADMIN) · tour booking & assignment engine · VideoAsset state machine
- AI-powered property search with voice support (OpenAI + SimplyRETS/MLS data cache)
- Real-time agent-to-client sessions via Cloudflare Stream + Daily.co
- Public read-only OpenAPI documentation for reviewing the production API contract
- **Stack:** Node.js/Express · PostgreSQL (Prisma) · Socket.io · Cloudflare Stream · Cloudflare R2 · Daily.co · Next.js

---

## 🛠 Tech Stack

**Backend**
Python · FastAPI · Django · Django REST Framework · Django Ninja · Node.js · Express.js · WebSockets (Django Channels · Socket.io)

**AI & LLMs**
AI Agents · Anthropic Claude API · OpenAI API · Google Gemini · OpenRouter · Prompt Engineering · Structured Output Validation · LLM Workflow Design · Multi-Provider Fallback

**Databases**
PostgreSQL · MySQL · Redis · Prisma ORM

**Frontend**
React.js · Next.js · HTMX · JavaScript (ES6+) · TailwindCSS · HTML5 · CSS3

**Infrastructure & Tools**
Docker · Celery · RQ · Render · Vercel · Cloudflare Stream · Cloudflare R2 · Git & GitHub · Postman

---

## 👨🏽‍🏫 Teaching & Mentorship

I've trained **500+ students** in web development — HTML, CSS, JavaScript, Node.js, Django, and backend architecture fundamentals. My approach: understand the fundamentals, build real things, write code that lasts.

Previously mentored a developer cohort under the **Ekiti State Government Partnership (Managet)** — guiding trainees through complete project lifecycles from design to production deployment.

---

## 🤝 Connect

- 🌐 [fgpsolutions.io](https://fgpsolutions.io)
- 💼 [linkedin.com/in/favour-ronald-enu](https://www.linkedin.com/in/favour-ronald-enu)
- 📧 favourronenu@gmail.com

Open to full-time remote AI engineering and backend engineering roles.
