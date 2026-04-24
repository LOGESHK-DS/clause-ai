## What Problem Does This Solve?

Legal contracts are long and complex, making manual review time-consuming and error-prone.

ClauseAI automates contract analysis by identifying risks, missing clauses, and suggesting improvements using AI.

## System Architecture

```mermaid
flowchart TD
    A[Contract PDF DOCX] --> B[Parser]
    B --> C[Text Extraction]
    C --> D[Classification Node]
    D --> E[Contract Type and Industry]

    E --> F[Vector DB ChromaDB]
    C --> F

    F --> G[Retrieve Similar Clauses]
    G --> H[Clause Analysis LLM]
    
    H --> I[Risk Detection]
    H --> J[Missing Clause Detection]
    H --> K[Improvement Suggestions]

    I --> L[Multi Agent Review]
    J --> L
    K --> L

    L --> M[Final Report Generation]