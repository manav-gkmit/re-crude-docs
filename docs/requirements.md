# Requirements

## Functional Requirements

### Resume Screening
- Poll Zoho ATS daily
- Fetch resumes from S3 / Drive
- Match resumes against job profiles
- Generate structured summary & recommendation

### Reviewer Interaction
- Slack / Email notifications
- Capture decisions via emojis, replies, or email

### Interview Feedback
- Automated reminders
- LLM-based formatting
- ATS status update

## Non-Functional Requirements
- Scalability via async queues
- Observability and audit logs
- Extensible modular design
