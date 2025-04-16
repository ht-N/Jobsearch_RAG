```markdown
# CV Job Matcher

A RAG-based system that automatically matches your CV with relevant job listings.

## Overview

CV Job Matcher uses Retrieval Augmented Generation (RAG) to find the most suitable job opportunities based on your CV. The system extracts key information from your resume and matches it against a curated database of job listings, ranking results by relevance score.

## How It Works

### Job Data Collection

The system crawls TopCV to gather job listings:
- Uses Selenium to navigate job listing pages
- Extracts detailed information (job descriptions, requirements, salary, location)
- Processes and structures data in CSV format

### CV Parsing

When a CV is uploaded, the system:
- Processes PDF/DOCX files using the ResumeManager
- Extracts candidate information, skills, education, and experience
- Uses LLM models to interpret and structure resume data

### RAG Implementation

The matching process uses:
- Vector embeddings via HuggingFace models (thenlper/gte-large)
- FAISS for efficient similarity search
- Semantic matching between CV content and job requirements
- Score-based ranking of results

## How to Use

### Requirements

```
pandas
numpy
torch
faiss-cpu
sentence-transformers
pdfplumber
streamlit
selenium
msedge-selenium-tools
webdriver-manager
requests
beautifulsoup4
lxml
```

### Installation

1. Clone the repository
2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

### Running the Application

Launch with:
```
streamlit run app.py
```

The web interface will:
1. Load in your browser
2. Allow you to upload your CV
3. Process your CV using LLM-based parsing
4. Display matching jobs sorted by relevance score

## Acknowledgements

[Title]
[Link]
```
