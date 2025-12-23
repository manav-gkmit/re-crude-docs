# Technology Stack

This document provides an overview of the **technology stack** used in Re:Crude, detailing backend frameworks, databases, infrastructure components, and third-party services.

---

## Technology Overview

| Layer | Technology | Purpose |
|------|-----------|---------|
| **Backend Language** | Python | Core business logic, integrations, and AI pipelines |
| **Web Framework** | FastAPI | RESTful API development with automatic OpenAPI documentation |
| **Async Task Processing** | Celery / RQ | Background jobs, batch processing, and scheduled tasks |
| **Relational Database** | PostgreSQL | Persistent storage for candidates, resumes, and evaluation data |
| **Message Broker / Cache** | Redis / RabbitMQ | Task queuing, caching, and inter-service communication |
| **Scheduling** | Cron-based Schedulers | Periodic polling of Zoho ATS and automated workflows |

---

## Third-Party Integrations

| Service | Technology | Responsibility |
|-------|-----------|----------------|
| **ATS** | Zoho ATS API | Resume ingestion, candidate lifecycle management, and status updates |
| **Communication** | Slack API | Notifications, feedback collection, and reviewer interactions |
| **Email Service** | SES / SendGrid | Interview reminders, recruiter notifications, and alerts |
| **LLM Provider** | OpenAI / Azure OpenAI | Resume parsing, candidate evaluation, recommendations, and feedback formatting |

---

## Stack Characteristics

| Attribute | Description |
|---------|-------------|
| **Scalability** | Supports asynchronous and batch processing for high-volume hiring |
| **Reliability** | Uses durable message queues and transactional databases |
| **Modularity** | Loosely coupled services enable independent scaling and maintenance |
| **AI Enablement** | Integrated LLM pipelines for evaluation and decision support |

---

This technology stack enables Re:Crude to operate as a **robust, scalable, and AI-driven recruitment automation platform** while maintaining flexibility for future enhancements.


