# Technology Stack

This document provides an overview of the **technology stack** used in Re:Crude, detailing backend frameworks, databases, infrastructure components, and third-party services.

---

## Backend
The backend of Re:Crude is built for **high-performance API handling, asynchronous tasks, and modular service design**:

- **Python** – Primary programming language for core logic, integrations, and AI pipelines.  
- **FastAPI** – Web framework for building RESTful APIs with automatic OpenAPI documentation.  
- **Celery / RQ** – Asynchronous task queues for batch processing, background jobs, and periodic tasks.

---

## Database
The platform uses **PostgreSQL** as the primary relational database:

- Stores structured candidate data, resumes, and evaluation results.
- Supports transactional integrity and complex queries.
- Ensures reliability and scalability for enterprise workloads.

---

## Infrastructure
The infrastructure components provide **scalability, reliability, and scheduling capabilities**:

- **Redis / RabbitMQ** – In-memory data store and message broker for queuing, caching, and task coordination.  
- **Cron-based Schedulers** – For automated polling of Zoho ATS, periodic reporting, and scheduled tasks.  

---

## Third-Party Services
Re:Crude leverages several external services to enhance functionality and integrations:

- **Zoho ATS API** – For retrieving resumes, updating candidate statuses, and managing applications.  
- **Slack API** – To send notifications and capture reviewer interactions.  
- **SES / SendGrid** – For sending emails, reminders, and notifications to interviewers and recruiters.  
- **OpenAI / Azure OpenAI** – For resume parsing, candidate evaluation, recommendation generation, and formatting interview feedback.

---

This technology stack allows Re:Crude to provide a **robust, scalable, and AI-enabled recruitment automation platform** while maintaining modularity and integration flexibility.

