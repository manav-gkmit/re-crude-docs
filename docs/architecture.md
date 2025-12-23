# System Architecture

This document describes the **high-level system architecture** of **Re:Crude**, outlining its components, execution flow, and interactions between internal services and external integrations.

---

## 1. Architecture Overview

Re:Crude is an **event-driven, modular recruitment automation platform** designed to automate resume screening, candidate evaluation, and interview feedback workflows.

The architecture is built around:

- A **scheduled or event-based trigger** to initiate hiring workflows  
- Zoho ATS as the **system of record**  
- Asynchronous processing using queues for scalability  
- LLM-based services for resume and feedback evaluation  
- Slack and Email for human-in-the-loop communication  

This design ensures **scalability, traceability, fault tolerance, and extensibility** across high-volume hiring scenarios.

---

## 2. High-Level Architecture Diagram

```mermaid
flowchart LR
    %% Start Trigger
    Start([Scheduled Poll / Hiring Event])

    %% External Systems
    Zoho[Zoho ATS]
    Slack[Slack]
    Email[Email Service]
    LLM[LLM Provider]

    %% Core Services
    Poller[Zoho ATS Polling Service]
    ResumeQ[Resume Processing & Batch Manager]
    Eval[LLM Resume Evaluation Service]
    Comm[Slack & Email Communication Service]
    Feedback[Feedback Collection & Formatting Service]
    Reminder[Interview Feedback Reminder Service]

    %% Infrastructure
    Queue[Async Queue]
    DB[(PostgreSQL)]

    %% Primary Flow (Resume Evaluation)
    Start --> Poller
    Poller --> Zoho
    Zoho --> Poller
    Poller --> ResumeQ
    ResumeQ --> Queue
    Queue --> Eval
    Eval --> LLM
    Eval --> DB
    Eval --> Comm

    %% Communication Flow
    Comm --> Slack
    Comm --> Email

    %% Feedback Flow
    Slack --> Feedback
    Email --> Feedback
    Feedback --> DB
    Feedback --> Zoho

    %% Reminder Flow
    DB --> Reminder
    Reminder --> Slack
    Reminder --> Email
```