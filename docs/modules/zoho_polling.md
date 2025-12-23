# Zoho ATS Polling & Batch Manager

This document describes the **Zoho ATS Polling and Batch Manager** component of Re:Crude, which is responsible for fetching candidate data and managing batch processing for automated resume screening.

---

## Responsibilities

The Zoho ATS Polling & Batch Manager handles the following key responsibilities:

- **Poll Zoho ATS for Candidates**  
  Continuously fetches new or updated candidate records from Zoho ATS.  

- **Identify Screening-Required Stages**  
  Determines which candidates are in stages that require automated screening and AI evaluation.  

- **Create Batch Execution Records**  
  Organizes candidates into batches for processing, enabling structured and traceable execution.

---

## Key Design Considerations

The component is designed with reliability, scalability, and traceability in mind:

- **Cron-Based Execution**  
  Periodically polls Zoho ATS using scheduled cron jobs or task schedulers to ensure timely updates.  

- **Idempotent Polling**  
  Ensures that repeated polling does not create duplicate batch records or cause inconsistent processing.  

- **Batch-Level Traceability**  
  Maintains detailed logs and metadata for each batch, including:
  - Candidate IDs 

  - Execution timestamps 

  - Processing status 

  This allows for auditing, debugging, and monitoring of batch execution.

---

By implementing these design principles, the Zoho ATS Polling & Batch Manager ensures **reliable, scalable, and auditable candidate intake and batch processing** for the Re:Crude platform.

