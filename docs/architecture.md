# System Architecture

## High-Level Flow

Zoho ATS → Batch Manager → Resume Queue → LLM Evaluation
↓
Slack / Email Review
↓
Zoho ATS Update
↓
PostgreSQL


## Architectural Principles
- Event-driven processing
- Idempotent updates
- Loose coupling between modules
