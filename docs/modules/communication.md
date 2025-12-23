# Communication Service: Slack & Email

The Communication Service is the bridge between the Re:Crude platform and the hiring team. It ensures that resume evaluations and other important updates are delivered promptly and that feedback is captured seamlessly.

## Core Responsibilities

- **Deliver Resume Summaries:** Once a resume has been evaluated by the LLM, this service takes the structured summary and sends it to the designated reviewers.

- **Maintain Contextual Conversations:** To keep the review process organized, the service maintains conversations in Slack threads. All communication related to a single candidate is kept in one place.

- **Capture Reviewer Feedback:** The service listens for responses from the hiring team. It can capture decisions made via:
    - **Slack Reactions:** Simple emoji reactions (e.g., :white_check_mark: for approval, :x: for rejection).
    - **Slack Replies:** More detailed feedback provided in a thread.
    - **Email Replies:** For reviewers who prefer email, the service can parse replies to capture their decisions.

## Smart Fallback Logic

To ensure that no candidate review is missed, the service employs a fallback mechanism:

> **Slack** → **Email** → **Manual Review**

If a notification fails to send on Slack or is not acknowledged within a certain timeframe, the service will automatically try to reach the reviewer via email. If both channels fail, the candidate is flagged for manual review.