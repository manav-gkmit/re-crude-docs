# Welcome to Re:Crude

Re:Crude is an internal recruitment automation platform designed to reduce manual hiring effort and improve evaluation consistency. It streamlines the hiring process by integrating with existing tools and leveraging AI to automate key tasks.

---

## Key Features

Re:Crude is designed to support the recruitment workflow, from initial resume screening to final feedback collection.

### Automated Resume Screening
*   **Daily Polling:** Automatically polls Zoho ATS every day to find new candidates in the screening stages.
*   **AI-Powered Evaluation:** Leverages Large Language Models (LLMs) to read and understand resumes, matching them against job profiles.
*   **Structured Summaries:** Generates concise, structured summaries of resumes, including skills, experience, and a recommendation.

### Seamless Reviewer Interaction
*   **Instant Notifications:** Delivers resume summaries and recommendations directly to reviewers via Slack or Email.
*   **Effortless Decisions:** Allows reviewers to record their decisions (e.g., "proceed" or "reject") with a simple emoji reaction or email reply.

### Streamlined Interview Feedback
*   **Automated Reminders:** Sends automated reminders to interviewers to ensure timely feedback submission.
*   **Consistent Formatting:** Uses LLMs to format unstructured feedback into a standardized, consistent format.
*   **ATS Integration:** Automatically updates the candidate's status in Zoho ATS based on the collected feedback.

## How it Works: A High-Level View

The platform operates as an event-driven system, ensuring that each step of the process is handled efficiently and reliably.

1.  **Poll & Batch:** A scheduled job polls Zoho ATS for new candidates and groups them into batches for processing.
2.  **Queue & Process:** Resumes are fetched and placed into a queue for parallel processing.
3.  **Evaluate & Summarize:** The LLM evaluation service picks up resumes from the queue, generates a summary and a recommendation.
4.  **Notify & Review:** The summary is sent to the designated reviewers on Slack or Email.
5.  **Update & Close Loop:** The reviewer's decision is captured, and the candidate's status is updated in Zoho ATS, completing the cycle.

## Technology Stack

Re:Crude is built on a modern, scalable technology stack:

*   **Backend:** Python, FastAPI, Celery / RQ
*   **Database:** PostgreSQL
*   **Infrastructure:** Redis / RabbitMQ, Cron-based schedulers, Containerized services
*   **Third-Party Services:** Zoho ATS API, Slack API, SES / SendGrid, OpenAI / Azure OpenAI

## Future Scope


- Interview scheduling (Calendly / Calendar APIs)
- Multi-reviewer consensus
- Resume scoring models
- Hiring analytics dashboard
- Fine-tuned LLMs per domain
