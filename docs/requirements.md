# Requirements

## Functional Requirements

### Resume Screening
The system will automate the initial resume screening process to identify qualified candidates efficiently.

- **Automated Polling:** The system will poll the Zoho ATS daily to identify new candidates who have entered the screening stage.

- **Resume Retrieval:** It will fetch candidate resumes from their storage locations, such as S3 or Google Drive.

- **AI-Powered Matching:** Resumes will be parsed and matched against the requirements outlined in the job profile using an LLM.

- **Structured Output:** A structured summary, including key skills, experience, and a recommendation (e.g., "Good Fit," "Potential Fit," "Not a Fit"), will be generated for each candidate.

### Reviewer Interaction
To streamline the review process, the system will facilitate seamless interaction with hiring managers and reviewers.

- **Multi-Channel Notifications:** Reviewers will receive notifications with the resume summary and recommendation on their preferred platform, either Slack or Email.

- **Effortless Decision Making:** Decisions can be captured directly from the notification. For example, a reviewer can use an emoji reaction in Slack (e.g., :white_check_mark: to proceed, :x: to reject) or reply to the email.

### Interview Feedback
The system will automate the collection and processing of interview feedback to ensure consistency and timeliness.

- **Automated Reminders:** The system will send automated reminders to interviewers who have not yet submitted their feedback.

- **LLM-Powered Formatting:** Unstructured feedback will be processed by an LLM to normalize it and fit it into a standardized format.

- **ATS Synchronization:** The candidate's status in the Zoho ATS will be automatically updated based on the collected feedback and decisions.

## Non-Functional Requirements
- **Scalability:** The system will be designed to handle a growing volume of candidates and jobs through the use of asynchronous task queues.

- **Observability:** Comprehensive logging and auditing will be implemented to ensure traceability and facilitate debugging.

- **Modularity:** The system will have an extensible modular design, allowing for the easy addition of new features and integrations in the future.