# Resume Processing & Queueing Service

This service is the workhorse of the Re:Crude platform. It's responsible for fetching resumes, validating them, and adding them to a queue for processing by the [LLM Resume Evaluation Service](llm_evaluation.md).

## Core Responsibilities

- **Fetch Resume Files:** The service retrieves resume files from their storage locations, which could be Amazon S3, Google Drive, or another file storage system.

- **Validate Accessibility:** Before adding a resume to the queue, the service checks to make sure that the file is accessible and can be opened. This prevents the processing queue from getting clogged with invalid files.

- **Push Jobs into Async Queue:** Once a resume is validated, the service creates a job and pushes it into an asynchronous queue. This allows for the parallel processing of a large number of resumes, making the system highly scalable.

## Key Features

This service is designed to be robust and resilient, with a number of features to ensure reliable processing:

- **Parallel Processing:** By using a message queue (like RabbitMQ or Redis), the service can process multiple resumes at the same time, significantly speeding up the screening process.

- **Retry with Exponential Backoff:** If a job fails for a transient reason (e.g., a network error), the service will automatically retry it. The retries are scheduled with exponential backoff, which means the time between retries increases with each subsequent failure. This helps to avoid overwhelming a service that may be temporarily down.

- **Failure Tagging for Manual Review:** If a job fails repeatedly, it is tagged for manual review. This ensures that no resume is lost and that any systemic issues can be identified and addressed.