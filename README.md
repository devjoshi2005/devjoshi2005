# Dev Joshi

**Cloud Security, FDE & Full Stack Engineer**  
Chennai, India • [LinkedIn](https://linkedin.com/in/devjoshi2005) • [Portfolio](https://devvjoshi.vercel.app) 

Computer Science & Engineering undergraduate (Anna University, 2023–2027) building high-throughput backend systems, cloud IAM/GRC tooling, and MCP-gated AI security workflows across AWS, GCP, and Azure. Contributor to Open Policy Agent (OPA) and experienced in production observability and scoped engineering sprints.

---

## Core Systems & Security Projects

### [Multi-Cloud GRC Compliance & Remediation Engine](https://github.com/devjoshi2005/Grc-Compliance-Engine)
*Automated compliance mapping, FAIR financial risk quantification, and policy-gated MCP remediation.*
- Covers **232 controls** across SOC 2, ISO 27001:2022, and NIST CSF 2.0, achieving **93.3% Recall@5** and **94.0% page-hit@5** across 150 real-PDF queries plus **56.0% top-3 framework mapping** over 384 Prowler-derived checks at **7.27 ms/finding**.
- Built a read-only **MCP remediation server** exposing **4 tools** and **3 resources** for retrieval, control mapping, and optional GPT-5-nano patch synthesis, backed by **53 passing tests**.
- Enforced **OPA policy checks**, citation grounding, and fail-closed Terraform validation, achieving **20/20** AWS/Azure remediation patches validated identically across deterministic runs and integrates **FAIR (ALE)** financial risk scoring to cut compliance triage from **30 → 6 minutes per finding (80% reduction)**.


### [AuthMap — Cloud IAM Attack-Path & Graph ML Analyzer](https://github.com/devjoshi2005/AuthMap)
*Multi-cloud IAM attack path analyzer using FastAPI, Neo4j, and graph anomaly detection.*
- Ingests AWS & GCP IAM configurations into a Neo4j property graph (**13 node types**) to run Cypher traversals across **29 privilege-escalation patterns** on a 1,000-principal environment in **~5s (~30s end-to-end)**.
- Combines deterministic checks with **Node2Vec embeddings** and **Local Outlier Factor (LOF)** scoring plus a Next.js explorer (**391 nodes in ~1.5s**), achieving **100% recall** and **0 false positives** across benchmark test sets.

### [Up — Real-Time Alerting & Escalation Engine](https://github.com/devjoshi2005/Up)
*Event-driven notification and escalation platform built for resilience under chaos conditions.*
- Built with Django, Channels (ASGI), Celery, Redis, and PostgreSQL using `SELECT FOR UPDATE SKIP LOCKED` escalation sweepers and HMAC-signed acknowledgement links.
- Benchmarked via k6 on a single `t3.micro`: sustained **~30 events/s (560ms p95)** and **500 concurrent WebSockets (~1.0s p95 end-to-end delivery)**.
- Maintained zero lost or duplicate messages across **1,300 chaos events** via a transactional outbox and replayable DLQ; resolved an ASGI sync-ORM leak to drop HTTP 5xx rates from **6.88% to 0%**.

### [ResilienceOps — Cloud-Native SOAR Engine](https://github.com/devjoshi2005/ResilienceOps)
*Log anomaly detection, Neo4j blast-radius mapping, and OPA-gated automated containment.*
- Trains an **Isolation Forest** model over 30K real AWS CloudTrail events across 7 behavioral features (**13ms p95** inference latency; **54% recall**, **0.19 F1**, **1.9% FPR**).
- Maps detected anomalies across a Neo4j graph (**142 principals → 232 resources**) for 4-hop blast-radius analysis, gating automated Terraform remediation behind **OPA/Rego** policies for sub-35s MTTD/MTTR.

### [ReconFlow — High-Throughput Payment Reconciliation](https://github.com/devjoshi2005/ReconFlow)
*3-way financial reconciliation engine built with Java 21, Spring Boot & Spring Batch.*
- Normalizes Razorpay, PhonePe, and bank CSV statements using Spring Batch checkpointing and PostgreSQL `SKIP LOCKED`.
- Async pipeline (`Next.js → Spring Boot → S3 → SQS`) processes **100K+ rows at ~850 rows/s** on an EC2 `t3.micro` with **~120ms p95** API query latency.

### [DevSecOps Container Remediation Engine](https://github.com/devjoshi2005/Dev-Portfolio) & [GCP Zero Trust Reference](https://github.com/devjoshi2005/Dev-Portfolio)
- **DevSecOps Pipeline:** 4-stage GitHub Actions workflow enforcing SonarQube (SAST), Trivy (SCA/container), OWASP ZAP (DAST), and Terraform IaC gates in **3.5 min/build**, paired with AWS Bedrock SARIF-to-patch synthesis (**2.3s/CVE**, **83.3% / 25/30** first-pass CI pass rate). *(Update links if hosted in dedicated repos.)*
- **GCP Zero Trust & DLP:** Reference architecture across IAM, VPC isolation, Cloud Armor WAF, KMS encryption, and Cloud DLP PII/PCI redaction aligned to GDPR and DPDPA.

---

## Open Source, Deployments & Freelance / Sprints

- **Open Policy Agent (OPA — CNCF Graduated):** Contributed fixes and deterministic regression tests for AST negative-number text-location parsing and REPL implicit function body evaluation (`#9558`, `#9553`) in Go/Rego.
- **Production Telemetry Deployment (The Nest School):** Instrumented Sentry observability across a Next.js admin portal and Expo mobile apps with real-time crash-rate, p95 latency (`>5,000 ms`), and failure-rate alert routing.
- **Targeted Engineering Sprints & Roles:** Actively looking for **FDE, Cloud Security, Backend/SDE, and Applied AI** roles, and open to **scoped technical sprints** (MCP/RAG guardrails & evals, cloud/IAM & OPA hardening, backend/webhook/reconciliation reliability, or stabilizing AI-generated codebases). Reach out at `devvjoshi2005@gmail.com` or via [Calendly](https://calendly.com/devvjoshi/15min) once live.
- **Problem Solving:** **997 LeetCode** problems solved (118 Hard, 665 Medium).

---

## Technical Stack

- **Languages:** Python, Java (21), Go, Rego, TypeScript, JavaScript (ES6+), SQL, Cypher, HTML5/CSS3, Bash
- **Applied AI & LLM Engineering:** MCP (Model Context Protocol), Agentic Workflows (LlamaIndex, CrewAI), RAG Pipelines, Hybrid Search (BM25 + Vector), ChromaDB, pgvector, Eval Harnesses, Node2Vec, scikit-learn (Isolation Forest, LOF), OpenAI / Gemini / AWS Bedrock APIs
- **Backend & Systems:** FastAPI, Django REST Framework, Django Channels (ASGI/Daphne), Spring Boot, Spring Batch, Spring Security, Celery, Next.js, React, Node.js, Express, WebSockets, GraphQL, OAuth2, JWT
- **Cloud Security & DevSecOps:** AWS (IAM, Security Hub, GuardDuty, CloudTrail, S3, SQS, KMS, Secrets Manager, ECS, WAF, Inspector, CloudWatch), Azure (Entra ID, Sentinel, Defender for Cloud, NSGs, Log Analytics, Key Vault), GCP (IAM, Cloud Armor, Cloud DLP, SCC, VPC), OPA/Rego, Terraform, Docker, Podman, Kubernetes, GitHub Actions, Trivy, OWASP ZAP, Prowler, SonarQube
- **Data Stores, Messaging & Observability:** PostgreSQL, Redis (Caching, Pub/Sub), Neo4j, AWS SQS, Kafka, OpenTelemetry, Grafana, Sentry

---

## Certifications & Credentials

- **Microsoft Certified:** Azure Security Engineer Associate (`AZ-500`) & Security, Compliance & Identity Fundamentals (`SC-900`)
- **Coursera / Cloud:** Google Cloud Security Engineer Associate Specialization, Google Cybersecurity Professional, AWS Cloud Technical Essentials, IBM Application Security & DevSecOps

---

## Outside of Engineering

Travelling • Music • Watching films • Hackathons & CTFs
