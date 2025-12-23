# LLM Resume Evaluation Service

This is the core intelligence of the Re:Crude platform. The LLM Resume Evaluation Service uses a Large Language Model to analyze resumes and provide a comprehensive, structured summary for reviewers.

## Core Responsibilities

- **Inject Job Profile Context:** To ensure a relevant evaluation, the service dynamically injects the job profile and requirements into the LLM's context. This allows the model to assess the candidate's suitability for the specific role.

- **Generate Structured Resume Summary:** The service processes the resume and generates a clean, easy-to-read summary. The summary is broken down into a consistent schema, making it easy for reviewers to find the information they need.

- **Produce AI-Powered Recommendation:** Based on its analysis, the LLM produces a recommendation, such as "Good Fit," "Potential Fit," or "Not a Fit." This provides a quick signal to reviewers, helping them to prioritize their work.

## Output Schema

The output of the evaluation service is a structured JSON object with the following fields:

```json
{
  "skills": ["Python", "FastAPI", "SQL", "Docker"],
  "experience": [
    {
      "company": "Tech Corp",
      "role": "Software Engineer",
      "duration": "2 years"
    }
  ],
  "projects": [
    {
      "name": "Project X",
      "description": "A brief description of the project."
    }
  ],
  "education": [
    {
      "institution": "University of Technology",
      "degree": "B.S. in Computer Science"
    }
  ],
  "recommendation": "Good Fit"
}
```

This structured output is then used by the [Communication Service](communication.md) to generate the notifications for reviewers.