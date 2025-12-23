# Feedback Collection & Formatting Service

This service is responsible for one of the most critical parts of the hiring process: collecting and making sense of interview feedback. It ensures that all feedback is captured, standardized, and stored correctly.

## Core Responsibilities

- **Collect Interviewer Feedback:** The service gathers feedback from various sources, whether it's from a structured form, an email, or a Slack message.

- **Normalize with LLM:** Raw, unstructured feedback can be inconsistent and hard to compare. This service uses a Large Language Model (LLM) to normalize the feedback, extracting key information and aligning it with a standard format.

- **Store Both Raw and Structured Data:** To ensure no information is lost, the service saves both the original, raw feedback and the newly structured version. This provides a complete record for auditing and future reference.

- **Update Zoho ATS:** Once feedback is processed, the service automatically updates the candidate's profile in the Zoho ATS, ensuring that the hiring workflow can proceed without manual intervention.

## The Power of Normalized Feedback

By using an LLM to normalize feedback, we can:

> - **Ensure Consistency:** All feedback is presented in the same format, making it easier to compare candidates.
> - **Reduce Bias:** By focusing on the substance of the feedback, we can reduce the impact of unconscious bias.
> - **Improve Searchability:** Structured feedback is easier to search and analyze, helping us to identify trends and improve our hiring process over time.