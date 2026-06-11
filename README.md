# Resume_Analyzer_AI


A simple Python-based Resume Analyzer built without any external AI APIs.  
This project extracts and analyzes resume content using basic text processing, regex, and keyword matching. Designed as an internship screening task for BSCS students.

## 📋 Project Objective
To analyze a resume PDF and generate a report containing:
1. Resume Score out of 100
2. Extracted Email & Phone Number  
3. Skills Found from predefined database
4. Missing Skills from database
5. Suggestions for resume improvement

**Note:** This version uses rule-based logic only. No LLM, OpenAI, or Gemini API is used.

## 🛠 Technologies Used
| Component | Technology |
| --- | --- |
| Language | Python 3.10+ |
| PDF Parsing | PyPDF2 |
| Web UI | Streamlit |
| Data Handling | Pandas |
| Logic | Regex + Keyword Matching |

## 📁 Project Structure
Resume_Analyzer_AI/
├── http://resume_analyzer.ipynb             # Main Streamlit application
├── http://skills.txt          # Skills database for matching
├── Python dependencies
├── http://README.md           # Project documentation
└── sample_resume.pdf   # Test file

## 🚀 How to Run

### 1. Setup Environment
```bash
pip install -r requirements.txt
### 2. Run Application
streamlit run app.py
Browser will open automatically at `http://localhost:8501`

### 3. Test the App
1. Upload any resume in PDF format
2. View extracted text, score, skills, and suggestions

## 📊 Scoring Logic
The resume score is calculated using rule-based points:
- *20 points* - If valid email found
- *20 points* - If phone number found  
- *4 points per skill* - For each skill matched from `skills.txt`
- *Max Score* - 100

### Skills Database
`skills.txt` contains 15+ technical skills like Python, SQL, Machine Learning, React, Git, etc. You can add/remove skills as needed.

## 📈 Sample Output
Resume Score: 84/100

Email: ['abc@gmail.com']
Phone: ['03001234567']

Skills Found:
['Python', 'SQL', 'HTML', 'Git']

Missing Skills:
['Power BI', 'Machine Learning', 'React']

Suggestions:
• Add more technical skills.
• Add projects section.
• Add certifications.

## ✅ Key Features
1. *No API Key Required* - Works offline
2. *Fast Processing* - Instant results for PDF < 5MB
3. *Customizable Skills* - Edit `skills.txt` to change skill list

## 👨‍💻 Developed By
Warda Ejaz | BSCS Undergraduate | AI/ML Enthusiast
Internship Screening Task  
Date: 11-June-2026

## 📜 Disclaimer
This is a rule-based analyzer for educational purposes. For advanced NLP-based analysis, LLM APIs can be integrated in future versions.


