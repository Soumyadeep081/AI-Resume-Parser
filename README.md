# AI Resume Matcher

An **LLM-powered resume parsing and job matching system** that analyzes resumes against job descriptions to evaluate candidate–job compatibility.

The project extracts structured information from resumes, identifies important skills and requirements from a job description, and uses an LLM to generate a **match score and detailed feedback**.

## 🚀 Features

* 📄 **Resume Parsing**

  * Extracts relevant information from PDF and DOCX resumes.
  * Converts unstructured resume content into structured data.

* 🎯 **Job Description Analysis**

  * Identifies important technical skills, qualifications, and requirements from a job description.
  * Extracts relevant keywords such as programming languages, frameworks, tools, and domain-specific skills.

* 🤖 **LLM-Powered Matching**

  * Compares the candidate's resume with the job description.
  * Evaluates alignment between candidate skills and job requirements.
  * Generates a compatibility score between **0 and 100**.

* 📊 **Candidate Evaluation**

  * Provides feedback on:

    * Matching skills
    * Missing skills
    * Relevant experience
    * Areas for improvement

* 🔄 **Batch Resume Processing**

  * Processes multiple resumes from a designated resume directory.

## 🏗️ Project Workflow

```text
                 Job Description
                       │
                       ▼
              ┌─────────────────┐
              │  JD Processing  │
              └────────┬────────┘
                       │
                       ▼
                Required Skills
                       │
                       │
Resume (PDF/DOCX) ────►│
                       ▼
              ┌─────────────────┐
              │ Resume Parsing  │
              └────────┬────────┘
                       │
                       ▼
                Structured Data
                       │
                       ▼
              ┌─────────────────┐
              │  LLM Evaluation │
              └────────┬────────┘
                       │
                       ▼
              Match Score (0-100)
                       │
                       ▼
             Detailed Feedback
```

## 🛠️ Technologies Used

* **Python**
* **Large Language Models (LLMs)**
* **Pydantic**
* **python-docx**
* **PDF parsing**
* **Pathlib**
* **JSON**

## 📁 Project Structure

```text
AI-Resume-Matcher/
│
├── resume_parser.py       # Main application
├── resumes/               # Resume files for processing
│   ├── resume1.pdf
│   ├── resume2.pdf
│   └── ...
│
├── requirements.txt       # Python dependencies
├── .gitignore
└── README.md
```

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/AI-Resume-Matcher.git
cd AI-Resume-Matcher
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it on Windows:

```powershell
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

## ▶️ Usage

Place the resumes you want to analyze inside the `resumes` directory.

```text
resumes/
├── candidate1.pdf
├── candidate2.pdf
└── candidate3.docx
```

Then run:

```bash
python resume_parser.py
```

The application processes each resume and generates a compatibility score based on the selected job description.

Example:

```text
Processing: candidate1.pdf

Score: 82.0
```

## 📊 Example Evaluation

The system evaluates candidates based on factors such as:

| Category         | Evaluation                                           |
| ---------------- | ---------------------------------------------------- |
| Technical Skills | Programming languages, frameworks, tools             |
| Domain Skills    | Relevant industry/domain knowledge                   |
| Experience       | Relevant projects and professional experience        |
| Job Requirements | Alignment with required qualifications               |
| Missing Skills   | Skills required by the JD but absent from the resume |
| Overall Fit      | Combined candidate–job compatibility                 |

The final result is represented as a score between **0 and 100** along with qualitative feedback.

## 🔐 Environment Variables

If your LLM provider requires an API key, store it in an environment variable rather than committing it to GitHub.

For example:

```env
OPENAI_API_KEY=your_api_key_here
```

Do **not** commit `.env` files or API keys to the repository.

Make sure `.gitignore` contains:

```gitignore
.venv/
__pycache__/
.env
*.pyc
```

## ⚠️ Limitations

The match score is an **LLM-generated evaluation**, so it should be treated as an intelligent screening aid rather than an objective hiring decision.

The quality of the result can depend on:

* Resume formatting
* Quality of extracted text
* Job description completeness
* LLM interpretation
* Prompt design

The system should therefore be used to **assist human evaluation**, not replace it.

## 🔮 Future Improvements

* [ ] Add a web interface using Streamlit
* [ ] Support more resume formats
* [ ] Add semantic similarity using embeddings
* [ ] Improve skill normalization
* [ ] Add weighted scoring for critical skills
* [ ] Generate candidate ranking tables
* [ ] Store evaluation results in a database
* [ ] Add recruiter dashboard
* [ ] Compare multiple candidates against the same JD
* [ ] Add explainable scoring with category-wise scores
* [ ] Improve evaluation consistency using structured scoring criteria

## 🎯 Use Cases

This project can be used as a foundation for:

* Automated resume screening
* Candidate–job matching
* Recruitment assistance
* Resume analysis
* Skill-gap analysis
* Applicant ranking systems

## 👨‍💻 Author

**Your Name**

If you found this project useful, consider giving the repository a ⭐.

---

## 📜 License

This project is available for educational and personal use.
