# Technical Documentation

Welcome to the **Re:Crude Technical Documentation**.

**Re:Crude** is an internal recruitment automation platform built to streamline and standardize the **end-to-end hiring workflow**.  
The platform integrates Applicant Tracking Systems (ATS), Large Language Models (LLMs), and communication tools to reduce manual effort, improve evaluation consistency, and enable scalable hiring operations.

This documentation serves as the **single source of truth** for understanding the system’s design, architecture, workflows, and integrations.

---

## What Re:Crude Solves

Modern hiring processes involve multiple tools, manual reviews, and fragmented feedback. Re:Crude addresses these challenges by:

- Automating resume intake and screening  
- Applying consistent AI-driven evaluation across candidates  
- Standardizing interview feedback collection and formatting  
- Reducing recruiter coordination and follow-ups  
- Maintaining complete traceability across the candidate lifecycle  

---

## High-Level System Overview

Re:Crude acts as an **orchestration layer** over existing recruitment systems using an **event-driven and modular architecture**.

At a high level, the platform:

- Synchronizes candidate data and application stages from **Zoho ATS**
- Processes resumes and interview feedback using **LLM-based evaluation pipelines**
- Communicates with recruiters and interviewers via **Slack and Email**
- Pushes structured insights, feedback summaries, and status updates back to the ATS

All major workflows are asynchronous and fault-tolerant to support high-volume hiring scenarios.

---

## Core Capabilities

### Automated Resume Screening
- Ingests resumes directly from Zoho ATS  
- Extracts skills, experience, education, and role-specific signals  
- Scores candidates against predefined job requirements  

---

### AI-Driven Candidate Evaluation
- Generates concise resume summaries for quick review  
- Classifies candidates by role fit (e.g., Strong / Moderate / Weak Fit)  
- Highlights strengths, gaps, and potential risks  

---

### Interview Feedback Automation
- Collects interviewer feedback through Slack or Email  
- Converts unstructured input into standardized schemas  
- Produces AI-generated summaries and recommendations  
- Automatically updates Zoho ATS with structured feedback  

---

### Scalable & Asynchronous Processing
- Supports batch processing for large candidate pools  
- Enables parallel evaluation workflows  
- Scales AI and integration services independently  

---

## Design Principles

Re:Crude is built around the following principles:

- Event-driven and asynchronous workflows  
- Idempotent and fault-tolerant processing  
- Loose coupling between services and integrations  
- Human-in-the-loop oversight for AI-driven decisions  

---

## Future Scope

Re:Crude can be enhanced with the following improvements to make recruitment smarter and more efficient:

- **Interview Scheduling**: Automate interview slot booking using calendar integrations.  
- **Multi-Reviewer Consensus**: Aggregate feedback from multiple reviewers for fairer decisions.  
- **Resume Scoring Models**: Use AI/ML to rank candidates based on skills and experience.  
- **Hiring Analytics Dashboard**: Visualize key hiring metrics for data-driven decisions.  
- **Fine-Tuned LLMs per Domain**: Improve resume parsing and recommendations with domain-specific models.

---

## Intended Audience

This documentation is intended for:

- Backend and platform engineers  
- Machine learning and AI engineers  
- Technical architects  
- Recruitment operations and hiring stakeholders  

---

## Documentation Guide

Use the navigation menu to explore detailed sections on:

- System architecture and data flow  
- Functional and non-functional requirements  
- Module-level designs and workflows  
- LLM evaluation pipelines  
- Error handling, scalability, and deployment  
- Planned enhancements and future scope  



