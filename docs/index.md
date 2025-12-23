# Technical Documentation

Welcome to the **Re:Crude Technical Documentation**.

**Re:Crude** is an internal recruitment automation platform designed to streamline and standardize the **end-to-end hiring workflow**. The system integrates Applicant Tracking Systems (ATS), Large Language Models (LLMs), and communication platforms to reduce manual effort, improve hiring efficiency, and enable scalable recruitment operations.

This documentation provides a comprehensive overview of the system architecture, workflows, integrations, and design principles behind Re:Crude.

---

## Platform Overview

Re:Crude automates the recruitment lifecycle—from resume intake to final hiring decisions—using an **event-driven and modular architecture**. It acts as an orchestration layer over multiple services, ensuring consistent data flow and automation across the hiring process.

The platform integrates the following core components:

### Zoho ATS Integration
Zoho ATS serves as the **system of record** for all recruitment data, including: 

- Candidates and job openings 

- Application stages and interview rounds  

- Hiring decisions and offer statuses   

Re:Crude continuously synchronizes with Zoho ATS to: 

- Fetch resumes and candidate metadata 

- Update candidate status automatically  

- Push structured interview feedback and AI-generated insights back into the ATS  

---

### LLM-Based Resume & Feedback Evaluation
Re:Crude leverages Large Language Models to enhance candidate evaluation by:  

- Parsing and summarizing resumes 

- Extracting skills, experience, and role relevance  

- Generating candidate fit assessments and recommendations  

- Converting unstructured interview feedback into standardized formats   

This ensures **consistency, fairness, and speed** across evaluations while reducing human bias and manual review effort.

---

### Slack & Email Communication
The platform integrates with Slack and Email to enable seamless communication across hiring teams:  

- Real-time notifications for candidate updates 

- Automated interview feedback requests  

- Status change alerts and reminders   

This minimizes manual follow-ups and keeps recruiters and interviewers aligned throughout the hiring process.

---

## Key Capabilities

### Automated Resume Screening
Re:Crude automatically processes incoming resumes by: 

- Ingesting resumes from Zoho ATS  

- Extracting key attributes such as skills, experience, education, and keywords  

- Scoring candidates against predefined job requirements   

This significantly reduces recruiter screening time and ensures uniform evaluation criteria across candidates.

---

### AI-Powered Recommendations 
Using LLM-driven analysis, the system generates: 

- Concise resume summaries for quick review  

- Role-fit recommendations (e.g., Strong Fit, Moderate Fit, Weak Fit)  

- Highlighted strengths, gaps, and potential risks   

These insights assist recruiters and hiring managers in making faster, data-backed decisions. 

---

### Interview Feedback Automation
Re:Crude simplifies post-interview workflows by: 

- Collecting interviewer feedback via Slack or Email  

- Structuring free-text feedback into predefined schemas  

- Summarizing overall interview outcomes using AI   

The processed feedback is automatically pushed to Zoho ATS, ensuring completeness and consistency. 

---

### Scalable Batch Processing
The platform is designed to handle high-volume hiring scenarios by:  

- Supporting batch resume processing  

- Asynchronously evaluating large candidate pools  

- Scaling AI and integration services independently   

This makes Re:Crude suitable for both small hiring cycles and enterprise-level recruitment drives. 

---

## Documentation Scope

This documentation covers:  

- System architecture and data flow  

- API contracts and integrations  

- LLM evaluation pipelines  

- Error handling and scalability considerations  

- Deployment and operational guidelines   

Use the navigation menu to explore each section in detail. 

