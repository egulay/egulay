# Emre Gülay

**Software Architect | Data Platform Engineer**

I am a Software Architect with 20+ years of experience designing enterprise software, distributed systems, and modern data platforms.

My public projects focus on software architecture, distributed data processing, AI-assisted analytics, AI-powered ETL, and secure data engineering. They include both open-source and source-available reference implementations emphasizing maintainability, scalability, security, and practical engineering.

---

## Featured Projects

### 🥚 Kozmik Lahmacun
**A governed conversational analytics and machine-learning platform for non-technical business users.**

Kozmik Lahmacun translates natural-language requests into validated, versioned execution orders for trusted Apache Spark processing. Corporate datasets remain inside the controlled execution environment and are never processed by the LLM.

The LLM works only with authorized metadata and bounded result facts. It helps interpret user requests, proposes governed execution orders, and produces management-friendly explanations after processing is complete.

**Key Features**
- Natural-language reporting and predictive analysis
- Governed JSON execution orders
- No arbitrary SQL, generated Python, or executable code
- Apache Spark reporting and machine-learning pipelines
- Automatic model comparison and parameter tuning
- Privacy-safe management summaries
- Batch MinIO and event-driven Kafka ingestion
- Spring Boot control plane
- Python execution plane
- SvelteKit and shadcn-svelte product interface
- PostgreSQL, Redis, Kafka, MinIO, Keycloak, and HashiCorp Vault
- English and Turkish user experience
- Security-focused, production-inspired architecture

**Repository:** Private *(as the project has grown beyond an early prototype, the source is no longer publicly available)*

> Kozmik Lahmacun is proprietary software. It is not currently source-available. Please reach out directly if you'd like to discuss evaluation or collaboration access.

---

### 🚀 Schema Serpent

**An AI-powered Spring Boot service that maps messy vendor price files into PostgreSQL and exposes flexible reporting through MCP.**

Schema Serpent is a training project built around a fictional pharmacy retailer, designed to tackle a common integration problem: different vendors describing the same data with different column names, units, currencies, and file formats. A small file preview is sent to an LLM, which proposes a deterministic transformation scenario; Java then validates, dry-runs, and executes that scenario locally, keeping every import auditable, repeatable, and inexpensive. Prices are converted to TRY using historical TCMB exchange-rate bulletins, and results are exposed through governed Model Context Protocol (MCP) tools that never accept raw SQL.

**Key Features**

- Watches an import directory and handles CSV, TSV, XLS, and XLSX
- AI proposes the schema mapping once per file; Java performs the deterministic row-by-row transformation
- Automatic scenario repair on validation or dry-run failure
- Full price history stored in PostgreSQL, converted to TRY using dated TCMB bulletins
- Streaming, chunked, concurrent ingestion with retry and resumability
- Safe, parameterized MCP reporting — no arbitrary SQL
- 10 MCP tools covering price reporting, import history, and currency conversion
- Usable directly from Claude Desktop as a local MCP server
- Works with local LLMs (LM Studio) or OpenAI

**Repository:**  
https://github.com/egulay/schema-serpent

> Schema Serpent is source-available under the PolyForm Noncommercial License 1.0.0. Commercial use requires written permission from the copyright holder.

---

### ⚡ Kebab Storm

**A secure distributed ETL framework for Apache Spark.**

Kebab Storm provides schema-driven data processing for large-scale analytics while protecting sensitive information through field-level encryption and secure processing pipelines.

**Key Features**

- Apache Spark
- Schema-driven ETL
- AES-256-GCM field-level encryption
- Apache Parquet
- HashiCorp Vault integration
- Secure data processing
- Production-oriented architecture

**Repository:**  
https://github.com/egulay/kebab-storm

---

### 🛠 Helpdesk

**A modern Spring Boot reference application demonstrating enterprise backend engineering practices.**

**Highlights**

- Spring Boot
- REST APIs
- gRPC
- Model Context Protocol (MCP)
- Spring AI
- PostgreSQL
- HashiCorp Vault
- Testcontainers
- OpenAPI

**Repository:**  
https://github.com/egulay/helpdesk

---

## Areas of Interest

- Software Architecture
- Distributed Data Processing
- Conversational Analytics
- Machine Learning Platforms
- AI-powered ETL
- Data Engineering
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
- Automate repetitive engineering and verification tasks.
- Prefer practical engineering over unnecessary complexity.
- Treat LLMs as a component within a larger system, not the system itself — scoped to the parts of a process that genuinely benefit from non-deterministic reasoning.

---

## About This Profile

I enjoy building public software projects that explore practical software architecture, distributed data processing, conversational analytics, secure data engineering, and modern backend technologies.

The projects in this profile are intended to serve as production-inspired reference implementations for engineers, architects, and platform teams interested in scalable systems, governed data processing, security-focused design, and modern engineering practices.

---

## Connect

**LinkedIn**  
https://www.linkedin.com/in/emre-gulay/
