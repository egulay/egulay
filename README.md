# Emre Gülay

**Software Architect | Data Platform Engineer**

I am a Software Architect with 20+ years of experience designing enterprise software, distributed systems, and modern data platforms.

My public projects focus on software architecture, distributed data processing, AI-assisted analytics, AI-powered ETL, and secure data engineering. They include both open-source and source-available reference implementations emphasizing maintainability, scalability, security, and practical engineering. A single thesis runs through all of them: **AI proposes, deterministic validators decide, trusted code executes.**

---

## Featured Projects

### 🥚 Kozmik Lahmacun
**A governed conversational analytics and machine-learning platform for non-technical business users.**

Kozmik Lahmacun translates natural-language requests into validated, versioned execution orders for trusted Apache Spark processing. Corporate datasets remain inside the controlled execution environment and are never processed by the LLM.

The LLM works only with authorized metadata and bounded result facts. It helps interpret user requests, proposes governed execution orders, and produces management-friendly explanations after processing is complete — the AI proposes, deterministic validators decide, trusted code executes.

**Why it matters**
- **AI without data exposure** — no arbitrary SQL, generated Python, or executable code ever reaches the data plane; the LLM sees metadata and bounded result contracts, never the datasets
- **Analytics for everyone** — natural-language reporting, predictive modeling with automatic algorithm comparison and tuning, and privacy-safe executive summaries (opt-out on request, in either language), in English and Turkish
- **From answer to analysis in one click** — completed results and trained ML models open directly in the corporate Jupyter environment as generated, bilingual starter notebooks (pandas and Spark ready, model re-scoring included) over short-lived presigned links; data moves server-to-server, never through the user's machine, and every handoff is audited. Jupyter is an output door, never an input door: only governed execution outputs are shared, never source data
- **Enterprise-grade governance** — role-based, owner-scoped workspaces where administrators manage without reading other users' data, backed by an immutable audit trail covering every management, deletion, import, ingestion, and notebook-handoff action
- **Corporate identity, built in** — Keycloak-based identity with AD/LDAP federation support: directory-managed users appear automatically, with app-side role assignment and lifecycle sync
- **Governed data intake** — manual CSV, object-event, and Kafka streaming ingestion into append-only Parquet, with schema-quality quarantine refusing what it cannot safely interpret
- **Live by default** — real-time grids, workspace tabs, audit log, and service health over SSE, designed against a production-inspired event-driven architecture
- **Your model, your hardware** — the language model is a choice per deployment: a remote OpenAI-compatible endpoint (your own inference server or a cloud API), or the platform's bundled model server on your cluster with the default evaluation model or any single-file Hugging Face model, NVIDIA-accelerated where GPUs are present. A strict mode keeps result data away from the model entirely
- **Installs like a product, not a project** — one guided, question-and-answer installer for a laptop evaluation or a corporate Kubernetes cluster: every answer is verified from inside the cluster before it is used (identity provider, secret store, database, message broker, notebook server, mail relay, registry, certificates from a private corporate CA), the install is health-gated, and an as-built record is written. Several instances — Finance, Marketing, an evaluation — run side by side on one cluster, each keyed and isolated, sharing corporate services without mixing anything. Air-gapped sites install from the delivery alone: every image the platform needs ships in the package or is mirrored into the customer's registry
- **Operable afterwards** — nothing decided at install is final: the same installer reconfigures one instance by name, credentials rotate the same way, a property helper changes single settings with validation and awaited restarts, redelivered images roll out under a tag of their own, and licensing is an offline signed file renewed with one command — lockout on expiry, never shutdown

**Stack:** Spring Boot control plane · Python/PySpark execution plane · SvelteKit + shadcn-svelte UI · PostgreSQL · Kafka · MinIO · Redis · Keycloak · HashiCorp Vault · JupyterLab integration · Helm chart with a guided installer for Kubernetes

**Repository:** Private *(as the project has grown beyond an early prototype, the source is no longer publicly available)*

> Kozmik Lahmacun is proprietary software. It is not currently source-available. Please reach out directly if you'd like to discuss evaluation or collaboration access.

---

### 🚀 Schema Serpent
**An AI-powered Spring Boot service that maps messy vendor price files into PostgreSQL and exposes governed reporting through MCP.**

Schema Serpent tackles one of integration's oldest headaches: every vendor describing the same data with different column names, units, currencies, and file formats. Built around a fictional pharmacy retailer, it sends only a small file preview to an LLM, which proposes a deterministic transformation scenario; Java then validates, dry-runs, and executes that scenario locally — keeping every import auditable, repeatable, and inexpensive.

**Why it matters**
- **AI maps once, Java executes forever** — the LLM sees a preview, not the file; the resulting scenario is validated, dry-run, and replayed deterministically, with automatic repair when validation fails
- **Built for messy reality** — watches an import directory for CSV, TSV, XLS, and XLSX; streaming, chunked, concurrent ingestion with retry and resumability
- **Financially correct by design** — full price history in PostgreSQL, converted to TRY using dated, historical TCMB exchange-rate bulletins
- **Governed reporting, no raw SQL** — 10 parameterized MCP tools for price reporting, import history, and currency conversion, usable directly from Claude Desktop as a local MCP server
- **Runs on your terms** — works with local LLMs (LM Studio) or OpenAI

**Stack:** Java · Spring Boot · PostgreSQL · Model Context Protocol · LM Studio / OpenAI-compatible APIs

**Repository:**
https://github.com/egulay/schema-serpent

> Schema Serpent is source-available under the PolyForm Noncommercial License 1.0.0. Commercial use requires written permission from the copyright holder.

---

### 😈 Dark Journal
**A private, encrypted Android diary where one of the seventy-two spirits of the Ars Goetia answers a sealed entry — in words from an LLM that runs entirely on the phone.**

Dark Journal (Karanlık Günlük in Turkish) is a personal project: the diary I wanted on my own phone. Entries are sealed with AES-256-GCM under a key that exists only on the device and as a 24-word recovery phrase. When an entry is sealed, deterministic code reads its themes and chooses the court, the spirit, and the tone; a small on-device model is asked only to speak in that voice. The thesis in miniature: code decides, the model only speaks — and nothing the user writes ever leaves the phone.

**Why it matters**
- **Code decides, the model only speaks** — themes, spirit, and tone are chosen deterministically from keyword themes in English and Turkish; the LLM receives a bounded brief and writes the answer, nothing more
- **Safety in code, not in the prompt** — a crisis check runs before the model is asked anything; when an entry reads like a crisis, no spirit answers and the app points to real help
- **Private by construction** — Gemma 4 E2B runs on the phone's CPU through LiteRT-LM; no accounts, no servers, no analytics, no ads
- **A vault, not a notes app** — AES-256-GCM for every entry and for the index, a keystore-wrapped key, and a BIP-39 recovery phrase shown once; nothing on disk is plaintext, not even file names
- **Backups without a cloud project** — one sealed file written to any place the user picks through Android's own file picker, Google Drive included; no OAuth, no API keys; restores merge and never delete
- **Built for curious eyes** — an optional veil blurs what was written in the list and leaves no picture of the journal among the recent apps
- **Motion as a design language** — a monochrome interface under a randomized night sky, where every piece assembles and nothing simply appears

**Stack:** Flutter · Dart · Kotlin platform channels · Gemma 4 E2B via LiteRT-LM · AES-256-GCM · Android Keystore · BIP-39 · Google Play Billing

**Repository:** Private

> Dark Journal is on its way to Google Play, with a closed test first. If you have an Android phone and would like to join the test, please reach out.

---

## More Projects

### ⚡ Kebab Storm
**A secure distributed ETL framework for Apache Spark.**

Kebab Storm provides schema-driven data processing for large-scale analytics while protecting sensitive information end to end — the sensitive fields are encrypted inside the pipeline itself, not bolted on at the storage layer.

**Why it matters**
- **Field-level protection at scale** — AES-256-GCM encryption applied per field within distributed Spark processing, so sensitive values stay protected throughout the pipeline
- **Schema-driven discipline** — declared schemas govern transformation and validation instead of ad-hoc pipeline code
- **Keys where they belong** — HashiCorp Vault integration keeps cryptographic material out of code and configuration
- **Analytics-ready output** — governed Apache Parquet, structured for downstream large-scale processing

**Stack:** Apache Spark · Apache Parquet · HashiCorp Vault

**Repository:**
https://github.com/egulay/kebab-storm

---

### 🛠 Helpdesk
**A modern Spring Boot reference application demonstrating enterprise backend engineering practices.**

A compact, production-inspired backend showing how contemporary Spring patterns fit together in one coherent codebase.

**Why it matters**
- **Three API styles, one domain** — REST, gRPC, and Model Context Protocol served side by side, with OpenAPI documentation
- **AI as a component** — Spring AI integrated as a scoped capability within the service, not as the architecture
- **Tested like production** — Testcontainers-backed integration testing against real PostgreSQL, with Vault-managed secrets

**Stack:** Spring Boot · Spring AI · gRPC · MCP · PostgreSQL · HashiCorp Vault · Testcontainers · OpenAPI

**Repository:**
https://github.com/egulay/helpdesk

---

## Areas of Interest

- Software Architecture
- Distributed Data Processing
- Conversational Analytics & Machine Learning Platforms
- AI-powered ETL
- Secure Data Engineering
- Event-driven Systems
- JVM Ecosystem
- Open-source and Source-available Software

---

## Technology Stack

### Languages

- Java
- Python
- SQL
- TypeScript

### Frameworks & Platforms

- Spring Boot
- Spring AI
- Apache Spark
- FastAPI
- SvelteKit

### Data Technologies

- PostgreSQL
- MySQL
- Apache Kafka
- RabbitMQ
- Apache Parquet
- Redis
- MinIO

### Identity, Security & AI

- HashiCorp Vault
- Keycloak
- OpenID Connect
- LM Studio
- OpenAI-compatible APIs

### Infrastructure

- Docker
- Docker Compose
- Google Cloud Platform (GCP)

### Testing & Quality

- JUnit 5
- Testcontainers
- pytest
- Playwright
- Vitest

---

## Engineering Philosophy

- Design software for long-term maintainability.
- Keep architectures understandable, scalable, and secure.
- Build security into the architecture from the beginning.
- Protect data through explicit trust boundaries and least-privilege access.
- Separate control-plane and execution-plane responsibilities.
- Prefer governed, validated operations over arbitrary generated code.
- Treat LLMs as a component within a larger system, not the system itself — scoped to the parts of a process that genuinely benefit from non-deterministic reasoning.
- Automate repetitive engineering and verification tasks.
- Prefer practical engineering over unnecessary complexity.

---

## About This Profile

I enjoy building public software projects that explore practical software architecture, distributed data processing, conversational analytics, secure data engineering, and modern backend technologies.

The projects in this profile are intended to serve as production-inspired reference implementations for engineers, architects, and platform teams interested in scalable systems, governed data processing, security-focused design, and modern engineering practices.

---

## Connect

**LinkedIn**
https://www.linkedin.com/in/emre-gulay/
