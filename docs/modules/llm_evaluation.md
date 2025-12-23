# LLM Resume Evaluation Service

This document describes the **LLM Resume Evaluation Service** in Re:Crude, which leverages Large Language Models to parse, analyze, and generate structured insights from candidate resumes.

---

## Responsibilities

The LLM Resume Evaluation Service is responsible for:

- **Inject Job Profile Context**  
  Provide the AI with the job description and requirements to ensure relevance during evaluation.  

- **Generate Structured Resume Summary**  
  Extract and organize key information from the candidate’s resume, including skills, experience, projects, and education.  

- **Produce AI Recommendation**  
  Generate an assessment of the candidate’s suitability for the role (e.g., Strong Fit, Moderate Fit, Weak Fit).

---

## Output Schema

The service outputs a **standardized, structured format** for each candidate, which can be consumed by downstream systems like batch processors or ATS integrations:

- **Skills** – Core technical and soft skills extracted from the resume.  
  *Example:* `["Python", "FastAPI", "Machine Learning"]`  

- **Experience** – Work history, including roles, companies, and duration.  
  *Example:*  
  ```json
  [
    {"role": "Software Engineer", "company": "ABC Corp", "duration": "2 years"},
    {"role": "Intern", "company": "XYZ Ltd", "duration": "6 months"}
  ]
  ```

