# Project Overview

**Re:Crude** is an internal recruitment automation platform built to reduce manual hiring effort, improve evaluation consistency, and scale recruitment workflows reliably.  
The system automates resume screening, AI-driven evaluation, and interview feedback processing while maintaining full traceability across the candidate lifecycle.

Re:Crude is designed with an **event-driven architecture**, enabling asynchronous processing, fault tolerance, and seamless integration with external systems.

---

## Objectives

The primary objectives of Re:Crude are:

- **Automate Resume Screening**  
  Reduce recruiter effort by automatically evaluating incoming resumes using AI models.

- **Standardize Interview Feedback**  
  Convert unstructured interviewer feedback into consistent, structured insights.

- **Improve Hiring Turnaround Time**  
  Enable faster candidate evaluation through parallel, asynchronous processing.

- **Maintain End-to-End Traceability**  
  Track every candidate action, evaluation, and decision throughout the hiring lifecycle.

---

## System Integrations

Re:Crude integrates with the following systems to deliver a complete hiring workflow:

### Zoho ATS
- Acts as the system of record for candidate data and status 

- Manages the candidate lifecycle from application to offer 

- Receives automated status updates from Re:Crude 

---

### Slack and Email
- Used for recruiter notifications and human-in-the-loop reviews 

- Enables quick validation or override of AI recommendations 

- Provides an audit-friendly communication trail 

---

### LLM Provider
- Performs resume evaluation and skill matching 

- Formats interview feedback into structured outputs 

- Generates hiring recommendations based on defined criteria 

---

## Design Philosophy

Re:Crude is built with the following guiding principles:

- Event-driven and asynchronous processing 

- Idempotent and fault-tolerant workflows 

- Loose coupling between system components 

- Human oversight for AI-driven decisions  

---

## Intended Audience

This documentation is intended for: 

- Backend and platform engineers 

- Machine learning and AI engineers 

- Technical architects 

- Recruitment operations and stakeholders

---
