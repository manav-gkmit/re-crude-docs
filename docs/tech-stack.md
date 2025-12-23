# Technology Stack

This section outlines the core technologies and services utilized in Re:Crude. We strive to use stable and secure releases to ensure reliability and maintainability.

| Category              | Technology                   | Description                                                                                                                               |
| --------------------- | ---------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **Backend**           | Python (3.14.2)              | The primary programming language, chosen for its readability, extensive libraries, and strong community support.                            |
|                       | FastAPI (0.127.0)            | A modern, fast (high-performance) web framework for building APIs with Python 3.7+, based on standard Python type hints.                      |
|                       | Celery (5.6)                 | An asynchronous task queue/job queue based on distributed message passing, used for handling background tasks and scheduled jobs.         |
|                       | RQ (Redis Queue) (2.6.1)     | A simple Python library for queueing jobs and processing them in the background with Redis. Used for simpler, lighter background processing. |
| **Database**          | PostgreSQL (18.1)            | A powerful, open-source object-relational database system known for its reliability, feature robustness, and performance.                   |
| **Infrastructure**    | Redis (8.4.0)                | An open-source, in-memory data structure store, used as a database, cache, and message broker (often with RQ).                            |
|                       | RabbitMQ (4.2.2)             | A widely used open-source message broker, enabling asynchronous processing and communication between microservices (often with Celery). |
|                       | Cron-based schedulers        | Used for time-based job scheduling, particularly for tasks like polling Zoho ATS.                                                       |
|                       | Containerized services       | Applications are deployed in containers (e.g., Docker) for consistency across environments and easier scaling.                          |
| **Third-Party Services** | Zoho ATS API               | For integrating with Zoho Applicant Tracking System to manage candidate data. (Utilizing current, secure versions)                          |
|                       | Slack API                    | For sending notifications and interacting with reviewers via Slack. (Utilizing current, secure versions)                                     |
|                       | SES / SendGrid               | Email service providers for sending automated emails (e.g., reminders, notifications). (Utilizing current, secure versions)                   |
|                       | OpenAI / Azure OpenAI        | Large Language Model providers used for resume evaluation and feedback formatting. (Utilizing current, secure versions)                        |