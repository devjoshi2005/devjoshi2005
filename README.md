# Dev Joshi

**Cloud Security & Full Stack Developer**  
Chennai, India • [LinkedIn](https://linkedin.com/in/devjoshi2005) • [Portfolio](https://devvjoshi.vercel.app) • [LeetCode](https://leetcode.com/u/its_devj/)

Security-minded software engineer specializing in automated cloud security, applied graph ML, high-concurrency backend pipelines, and AI system security. Driven by first-principles problem solving—moving beyond finding security gaps to building high-throughput, self-remediating infrastructure.

---

## ⚡ Core Systems & Security Projects

### [AuthMap — Cloud IAM Attack-Path & Graph ML Analyzer](https://github.com/devjoshi2005/AuthMap)
*Engineered a multi-cloud IAM attack path analyzer using FastAPI, Neo4j, and Node2Vec anomaly detection.*
- Ingests AWS & GCP IAM permission models into a Neo4j graph (13 node types) to execute Cypher queries across **29 privilege-escalation patterns**.
- Combined deterministic rule checks with **Node2Vec embeddings** and **Local Outlier Factor (LOF)** graph-anomaly scoring; scanned a 1,000-principal environment in **~5s (~30s end-to-end)** with zero false positives across test sets.
- Interactive Next.js graph rendering handles 391 nodes in **~1.5s**.

### [Multi-Cloud GRC Engine](https://github.com/devjoshi2005/Grc-Compliance-Engine)
*Automated multi-cloud compliance and financial risk quantification engine built on hybrid RAG.*
- Ingests live AWS/Azure telemetry into a hybrid **BM25 + vector search** RAG pipeline (LlamaIndex + ChromaDB) over 6 regulatory frameworks (**232 controls** across SOC 2, ISO 27001, NIST CSF 2.0).
- Automates control mapping and remediation drafting, cutting compliance triage from **30 → 6 minutes per finding (80% reduction)**.
- Integrates the **FAIR framework (ALE)** to quantify technical findings into executive exposure ($180K / INR 1.6 Cr).

### [Up — Real-Time Alerting & Escalation Engine](https://github.com/devjoshi2005/Up)
*Production-tested event-driven notification platform built for resilience and zero data loss under chaos conditions.*
- Built using Django, Channels (ASGI), Celery, Redis, and PostgreSQL with `SELECT FOR UPDATE SKIP LOCKED` escalation sweepers and HMAC-signed acknowledgement links.
- Benchmarked via k6 on a single `t3.micro`: sustained **~30 events/s (560ms p95)**, **500 concurrent WebSockets**, and **~1.0s p95** delivery.
- Maintained zero lost or duplicated messages across **1,300 chaos events** using transactional outbox and jittered backoffs; fixed an ASGI sync-ORM leak, cutting HTTP 5xx rates from **6.88% to 0%**.

### [ResilienceOps — Cloud-Native Log Anomaly & SOAR Engine](https://github.com/devjoshi2005/ResilienceOps)
*Automated incident response engine utilizing unsupervised ML and Graph-based blast radius mapping.*
- Trains an **Isolation Forest** pipeline over 30K real AWS CloudTrail log events across 7 behavioral features (**13ms p95** inference latency).
- Maps detected anomalies inside Neo4j to evaluate 4-hop attack blast radius paths, gating automated Terraform remediation behind **OPA/Rego** policy checks to cut sub-35s MTTD/MTTR.

### [ReconFlow — High-Throughput Payment Reconciliation](https://github.com/devjoshi2005/ReconFlow)
*3-way financial reconciliation workbench built using Java 21 & Spring Batch.*
- Processes **100K+ transaction rows at ~850 rows/s** on an EC2 `t3.micro` using Spring Batch checkpointing and PostgreSQL `SKIP LOCKED`.
- Asynchronous ingestion pipeline (Next.js → Spring Boot → S3 → SQS) sustains **~120ms p95 API latency**.

---

## Technical Stack

- **Languages:** Python, TypeScript, Java (21), SQL, Cypher, Bash
- **Applied AI & ML:** RAG Pipelines, LlamaIndex, ChromaDB, Hybrid Search (BM25 + Vector), OpenAI / LLM APIs, Node2Vec, scikit-learn (Isolation Forest, LOF)
- **Backend & Systems:** FastAPI, Django REST Framework, Django Channels (Daphne/ASGI), Spring Boot, Spring Batch, Celery, WebSockets, REST APIs
- **Security & Cloud:** AWS (EC2, S3, SQS, CloudTrail, GuardDuty), Azure, GCP, Docker, Terraform (IaC), OPA/Rego, OWASP ZAP, SonarQube, Trivy, Prowler
- **Data Stores & Messaging:** PostgreSQL, Redis (Pub/Sub & Caching), Neo4j, SQLite, AWS SQS

---

## Certifications & Credentials

- **Microsoft Certified:** Azure Security Engineer Associate (`AZ-500`)
- **Microsoft Certified:** Security, Compliance & Identity Fundamentals (`SC-900`)
- **Coursera / Professional:** Security in Google Cloud Specialization | AWS Cloud Technical Essentials

---

## Open Source & Active Focus

- **Open Source:** Active contributor to security and cloud tooling repos (currently engaging with OWASP nettacker security modules & others).
- **Current Focus:** Building production-grade AI Agent guardrails, optimizing asynchronous RAG pipelines, and practicing LeetCode.
- **Goal:** Seeking SDE, Applied AI, or Cloud Security / DevSecOps engineering roles at product-first tech firms and GCCs.

---

## Outside of Engineering

Travelling • Music • Watching films • Tech Hackathons & CTFs
