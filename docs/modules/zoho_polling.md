# Zoho ATS Polling & Batch Manager

This service is the entry point for the entire Re:Crude workflow. It's responsible for polling the Zoho Applicant Tracking System (ATS) to find new candidates and organizing them into batches for processing.

## Core Responsibilities

- **Poll Zoho ATS for New Candidates:** On a regular schedule (e.g., every hour), this service connects to the Zoho ATS API to look for new candidates.

- **Identify Screening-Required Stages:** The service is configured to only pull candidates who are in specific, screening-required stages of the hiring process. This ensures that we are only processing relevant candidates.

- **Create Batch Execution Records:** To ensure traceability, the service groups candidates into batches and creates a record for each batch. This allows us to track the progress of a group of candidates as they move through the system.

## Key Design Principles

The design of this service is guided by the following principles:

- **Cron-Based Execution:** The polling process is triggered by a cron-based scheduler, which ensures that it runs at regular, predictable intervals.

- **Idempotent Polling:** The service is designed to be idempotent, which means that running it multiple times will not create duplicate records. It keeps track of the candidates it has already processed to avoid re-processing them.

- **Batch-Level Traceability:** By creating batch records, we can easily trace the journey of each candidate through the system. This is crucial for auditing, debugging, and generating analytics.