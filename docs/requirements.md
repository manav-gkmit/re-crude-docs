# Requirements

This document outlines the **functional** and **non-functional requirements** for the Re:Crude recruitment automation platform.

---

## 2.1 Functional Requirements

### Resume Screening & Evaluation
The platform should automate the evaluation of candidate resumes as follows: 

- **Poll Zoho ATS Daily**  
  Check for candidates in the following stages: 

    - New 
    - Applied 
    - Custom screening required stages  

- **Fetch Resume Links**  
  Retrieve resumes stored in S3 or Google Drive.

- **Match Resumes Against Job Profiles**  
  Use predefined job profiles to evaluate candidate fit.

- **Generate Output**  
  - **Structured Resume Summary**: skills, experience, projects  
  - **AI Recommendation**: 

    - Selected 

    - Not Selected 

    - Needs Manual Review  

- **Send Summaries & Resume Links to Reviewers**  
  Deliver via Slack or Email.  

- **Capture Reviewer Response**  
    - Slack emoji (✅ / ❌) 

    - Slack thread reply 

    - Email reply  

- **Update Candidate Status in Zoho ATS Automatically**  
  Summaries and AI recommendations are visible in Zoho, and users can also update status manually if needed.

---

### Job Profile Management
- Maintain job profiles using Excel sheets with fields: 

  - Job name 

  - Experience level 

  - Domain 

  - Description 

  - Requirements  

- Use job profiles as context for LLM-based resume evaluation.

---

### Interview Feedback Automation
- Send automated Slack/Email reminders to collect feedback after interviews. 

- Normalize feedback into a **standardized structure** using LLM. 

- Save both formatted feedback and original interviewer feedback in **Zoho ATS** and internal database. 

- Update candidate status on Zoho based on interviewer feedback. 

- Generate candidate-facing communication drafts automatically.

---

### Batch & Parallel Processing
- Execute scheduled cron-based batch jobs for resume evaluation (daily). 

- Support high-volume resume processing via asynchronous queues. 

- Persist batch execution results for **auditability and traceability**.

---

## 2.2 Non-Functional Requirements

- **Scalability**: Handle large volumes of resumes efficiently using async queues. 

- **Observability**: Maintain logs, metrics, and batch execution history for monitoring and troubleshooting. 

- **Extensibility**: Allow easy addition of features such as **interview scheduling** and new integrations.

---

This requirements document ensures that Re:Crude is **both functionally robust and technically scalable**, supporting automated, AI-driven recruitment workflows.
