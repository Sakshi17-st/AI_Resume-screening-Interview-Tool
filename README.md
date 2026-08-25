 AI Resume Screening & Interview Prep Tool

An intelligent web-based application built with **Python and Flask** to analyze resumes against job descriptions. The system extracts resume content, calculates a resume-job similarity score using **TF-IDF and Cosine Similarity**, identifies skill gaps, and generates technical and behavioral interview questions.

 Project Overview

Recruiters and job seekers often need to determine how well a resume matches a particular job role. Manually comparing resumes with job descriptions can be time-consuming.

This project automates the initial screening process by allowing users to upload their resume and provide a job description. The application analyzes both documents and provides a detailed result including:

- Resume-to-job match score
- Matched skills
- Missing skills
- Extra skills
- Technical interview questions
- Behavioral interview questions

The project is implemented as a lightweight Flask web application and is suitable for academic projects, demonstrations, and portfolio use.

---

 Features

 Resume Parsing

Supports multiple resume formats:

- PDF
- DOCX
- TXT

The application extracts text automatically from the uploaded file.

📊 Resume Matching

The system compares the extracted resume text with the provided job description using:

- Text preprocessing
- TF-IDF vectorization
- Cosine similarity

The similarity result is converted into a percentage-based match score.

Skill Gap Analysis

The application uses a predefined skill database covering programming, web development, AI/ML, databases, cloud, DevOps, mobile development, computer science fundamentals, and soft skills.

It identifies:

- **Matched Skills** – Skills available in both the resume and job description.
- **Missing Skills** – Skills mentioned in the job description but not detected in the resume.
- **Extra Skills** – Skills detected in the resume but not mentioned in the job description.

🎯 Match Verdict

The system provides a simple verdict based on the calculated score:

| Score | Verdict |
|---|---|
| 75% and above | Excellent Match |
| 50% – 74.99% | Good Match |
| 30% – 49.99% | Fair Match – Resume Needs Improvement |
| Below 30% | Poor Match – Resume Needs Significant Tailoring |

💻 Interview Preparation

Based on the matched skills, the system generates technical interview questions.

It also provides behavioral interview questions covering topics such as:

- Self introduction
- Teamwork
- Leadership
- Failure and learning
- Career goals
- Hiring-related questions

---

 Technology Stack

| Technology | Purpose |
|---|---|
| Python | Backend development |
| Flask | Web application framework |
| PyPDF2 | PDF text extraction |
| python-docx | DOCX text extraction |
| Scikit-learn | NLP and similarity calculation |
| TF-IDF | Text feature extraction |
| Cosine Similarity | Resume-JD similarity measurement |
| HTML5 | Frontend structure |
| CSS3 | Custom styling |
| Bootstrap 5 | Responsive UI |

---

 System Workflow

```text
             Resume Upload
                   ↓
             File Validation
                   ↓
            Resume Parsing
          PDF / DOCX / TXT
                   ↓
          Text Preprocessing
                   ↓
        Job Description Input
                   ↓
          TF-IDF Vectorization
                   ↓
          Cosine Similarity
                   ↓
            Match Score
                   ↓
            Skill Analysis
       ┌───────────┼───────────┐
       ↓           ↓           ↓
    Matched      Missing      Extra
     Skills      Skills      Skills
       └───────────┬───────────┘
                   ↓
        Interview Question
             Generation
                   ↓
             Result Page

Project Structure

AI-Resume-Screening-Interview-Prep-Tool-main/
│
├── app.py
├── resume_parser.py
├── matcher.py
├── question_bank.py
├── index.html
├── result.html
├── style.css
├── requirements.txt
├── README.md
└── .gitignore

