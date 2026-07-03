=========================================================
               AI-POWERED ATS RESUME SCORER
=========================================================

An intelligent web application that evaluates how well a 
resume matches a job description (JD) and provides 
actionable feedback. This project simulates an Applicant 
Tracking System (ATS), giving job seekers the insights 
they need to optimize their resumes before applying.

---------------------------------------------------------
1. FEATURES
---------------------------------------------------------
* Resume Parsing: Upload resumes in PDF, DOC, or DOCX formats.
* Semantic Matching: Uses spaCy and Sentence Transformers 
  to compare extracted skills and experience against the 
  job description.
* Comprehensive Scoring: Get an overall ATS score and a 
  detailed breakdown by category (Formatting, Keywords, 
  Content, Skill Validation, ATS Compatibility).
* AI-Powered Suggestions: Integrates the Groq API (Llama 3) 
  to generate tailored, actionable suggestions to improve 
  your resume.
* User Accounts & History: Secure login via Supabase to 
  save and revisit past resume analyses.
* Export Reports: Download beautiful PDF reports.

---------------------------------------------------------
2. TECH STACK
---------------------------------------------------------
* Frontend: Streamlit
* Backend: FastAPI (Python)
* NLP Models: spaCy (en_core_web_md), Sentence Transformers
* LLM: Groq API (Llama 3)
* Database/Auth: Supabase

---------------------------------------------------------
3. SETUP & INSTALLATION
---------------------------------------------------------
Step 1: Clone the Repository
  git clone https://github.com/miteshkumrawat441-design/ATS-Scorer-System.git
  cd ATS-Scorer-System

Step 2: Create a Virtual Environment
  python -m venv venv
  (Windows) .\venv\Scripts\Activate.ps1
  (Mac/Linux) source venv/bin/activate

Step 3: Install Dependencies
  pip install -r requirements.txt
  python -m spacy download en_core_web_md

Step 4: Configure Environment Variables
  Duplicate .env.example to .env and fill in your Supabase 
  and Groq API keys. 
  Duplicate frontend/.streamlit/secrets.toml.example to 
  frontend/.streamlit/secrets.toml and fill it in.

---------------------------------------------------------
4. RUNNING THE APPLICATION
---------------------------------------------------------
You will need two separate terminal windows (with the 
virtual environment activated in both).

Terminal 1 (Backend):
  uvicorn backend.main:app --reload --host 0.0.0.0 --port 8000
  (API runs on http://localhost:8000)

Terminal 2 (Frontend):
  streamlit run frontend/streamlit_app.py
  (Web app runs on http://localhost:8501)

---------------------------------------------------------
5. IMPORTANT NOTES
---------------------------------------------------------
* Never commit your .env or secrets.toml files.
* On your first run, the ML model (~80MB) will download.
* If you don't have a Groq API key, scoring still works 
  but the AI suggestions will be empty.

=========================================================
