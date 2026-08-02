# Hemnaath Balasubramani

**AI/ML engineer. I build LLM systems and then try to break them.**

<p>
  <a href="https://www.hemnaath.tech"><img alt="Portfolio" src="https://img.shields.io/badge/Portfolio-e3b341?style=flat-square&logo=safari&logoColor=0d1117" /></a>
  <a href="https://linkedin.com/in/hemnaath04"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-30363d?style=flat-square&logo=linkedin&logoColor=e6edf3" /></a>
  <a href="mailto:balasubramani.h@northeastern.edu"><img alt="Email" src="https://img.shields.io/badge/Email-30363d?style=flat-square&logo=gmail&logoColor=e6edf3" /></a>
</p>

> 🟢 **Looking for a Spring 2027 co-op (January to June).** Applied AI, LLM engineering, evals and reliability.
> Boston, MA · MS CS @ Northeastern Khoury · Co-op works on CPT, so no sponsorship needed.

---

### Hey, I'm Hemnaath

I got into AI sideways. I spent about a year and a half at EPAM writing test automation for a ride-hailing fares engine, and near the end of it I was put on an internal agent that generated test cases from requirements docs. It was the first thing I'd worked on that *wrote* the artifacts instead of checking mine, and I couldn't stop thinking about it. So I moved into AI/ML full time.

The testing instinct came with me, and honestly it's the most useful thing I brought. Most LLM products put "be accurate" in the system prompt and hope for the best. I don't trust that. I'd rather write the check in code and let it fail loudly.

That's most of what I build now: agents that do real work, plus the scaffolding that catches them when they make things up. Everything below is deployed and running somewhere, not sitting in a notebook.

---

## What I've built

### 💼 job-os
**A job tracker whose resume agent isn't allowed to lie about you.**

You track applications, it tailors your resume per job. The catch is that every claim the agent writes has to trace back to something you already verified. After generation, unverified numbers get stripped, entities that never appeared in your source facts get rejected outright, and a resume version can't be finalized until it clears a deterministic score with zero blocking issues.

*The part I'd talk about in an interview:* prompting the model to stay grounded didn't work reliably, so grounding became a validation pass the output has to survive. Same idea as a test suite gating a deploy, just pointed at a model.

`Python` `FastAPI` `LangGraph` `PostgreSQL + pgvector` `Docker`
**[Try it ↗](https://jobs.hemnaath.tech)** · [Code ↗](https://github.com/hemnaath04/job-os)

<!-- TODO: one number here. Resumes generated, users, or hallucination rate before/after the validator. Even a small real number beats none. -->

---

### 🔍 RoleReveal
**Chrome extension that scores any job posting against your resume, inline.**

Open a posting, see a fit score and a breakdown without leaving the page. Your name, email, phone and address get masked out before anything is sent to the model, so the scoring happens on skills and experience only.

*The part I'd talk about in an interview:* the privacy layer wasn't a feature request, it was the constraint that made me redesign what actually gets sent. Turns out the model scores better without the PII anyway.

`JavaScript` `Chrome Extensions API` `LLM APIs`
**[Install it ↗](https://chromewebstore.google.com/detail/oplfnlcnahoijcflpjjncplkoakdpobb)** · [Code ↗](https://github.com/hemnaath04/rolereveal)

---

### 🌾 ClaimFarm
**A smallholder farmer sends a photo of a damaged crop on WhatsApp. It comes out the other end as a filed insurance claim.**

The pipeline cross-checks the claim against weather data for that location and date, runs photo forensics to catch reused or edited images, and hands a human adjuster a scored case instead of a raw photo.

*The part I'd talk about in an interview:* the whole thing is a fraud-detection problem wearing a UX costume. The interesting work was deciding what the model is allowed to decide versus what a deterministic check has to settle before a human ever sees it.

`Python` `Vision models` `Weather APIs` `Vercel`
**[Live ↗](https://claimfarm-dashboard.vercel.app)** · [Code ↗](https://github.com/hemnaath04/claimfarm)

---

### 🗺️ BedRocked
**Which of Somerville's 2,404 combined-sewer segments should the city dig up first?**

Joins municipal GIS sewer data to street-scan road-condition data, then scores every segment for dig-readiness so the city can sequence repaving and sewer work together instead of tearing up the same street twice. Built at a 2026 hackathon.

*The part I'd talk about in an interview:* two datasets that don't share a key. Getting a defensible spatial join between them was 80% of the work, and the scoring was the easy part after that.

`Python` `pandas` `GeoPandas` `scikit-learn` `Vercel`
**[Live ↗](https://sewershed-bedrocked.vercel.app)** · [Code ↗](https://github.com/hemnaath04/bedrocked)

---

## What I actually use

**Every day** Python · FastAPI · LangGraph · PostgreSQL (+ pgvector) · Docker
**AI/ML** LLM orchestration · agentic systems · RAG and vector retrieval · evaluation harnesses · embeddings
**Comfortable with** Java · MongoDB · async SQLAlchemy · Appwrite · Cloudflare R2 · Vercel / Render

---

## Before this

**EPAM Systems** — Test Automation Engineer on a ride-hailing fares platform, 2024 to 2025. Built CI-grade automation suites end to end in Go and Java, finished on that test-generation agent that started all this.

**Northeastern University** — MS Computer Science, Khoury College, Jan 2026 to May 2028. Currently in reinforcement learning and NLP.

---

## Talk to me

I'm after a **Spring 2027 co-op** in applied AI or LLM evaluation. If that's something you're hiring for, or you just want to argue about whether prompt-based guardrails count as guardrails, email me.

📧 **balasubramani.h@northeastern.edu** · [LinkedIn ↗](https://linkedin.com/in/hemnaath04) · [hemnaath.tech ↗](https://www.hemnaath.tech)
