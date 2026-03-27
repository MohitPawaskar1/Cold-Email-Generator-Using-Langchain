# Cold Email Generator using LangChain

## Overview
This project is an AI-powered application that generates personalized cold emails based on job postings. Given a job URL, the system extracts relevant job information and generates a tailored outreach email using Large Language Models (LLMs).

The application leverages LangChain for prompt orchestration, ChromaDB for portfolio retrieval, and Streamlit for an interactive user interface.

---

## Features
- Extracts job details directly from a provided URL
- Parses structured information such as role, experience, skills, and description
- Matches job requirements with portfolio data using vector search
- Generates personalized cold emails using LLMs
- Interactive web interface built with Streamlit

---

## Tech Stack
- Python
- LangChain
- ChromaDB
- Streamlit
- Groq LLM API
- Pandas

---

## Project Structure
```
app/
│── main.py              # Streamlit application
│── chains.py            # LLM chains and prompt logic
│── portfolio.py         # ChromaDB integration for portfolio retrieval
│── utils.py             # Text cleaning utilities
│── resource/
│    └── my_portfolio.csv
```

---

## How It Works
1. User provides a job posting URL  
2. WebBaseLoader extracts raw job content  
3. Text is cleaned and processed  
4. LangChain extracts structured job data  
5. Skills are used to query ChromaDB for relevant portfolio links  
6. LLM generates a personalized cold email using job context and portfolio data  

---

## Installation

### Clone the repository
```
git clone https://github.com/MohitPawaskar1/Cold-Email-Generator-Using-Langchain.git
cd Cold-Email-Generator-Using-Langchain
```

### Install dependencies
```
pip install -r requirements.txt
```

### Set environment variables
Create a `.env` file:
```
GROQ_API_KEY=your_api_key_here
```

---

## Running the Application
```
streamlit run app/main.py
```

Then open:
```
http://localhost:8501
```

---

## Example Workflow
- Input: Job URL from a careers page  
- Output: AI-generated personalized cold email tailored to the job role  

---

## Future Improvements
- Convert to FastAPI backend for production deployment  
- Introduce LangGraph for multi-step agent workflows  
- Improve retrieval pipeline for true RAG implementation  
- Add resume-based personalization  
- Deploy as a scalable web service  

---

## Security Note
API keys are managed using environment variables and are not stored in the repository.

---

## Author
Mohit Santosh Pawaskar