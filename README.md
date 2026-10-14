# ATS Resume Analyser

A Django-based web application that analyses PDF resumes, identifies technical skills, calculates a rule-based resume score, and compares resume skills against a job description.

Built with Python, Django, Django REST Framework, SQLite, HTML, CSS, and Bootstrap.

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Django](https://img.shields.io/badge/Django-4.2-green)
![Django REST Framework](https://img.shields.io/badge/Django%20REST%20Framework-DRF-red)
![Database](https://img.shields.io/badge/Database-SQLite-blue)
![UI](https://img.shields.io/badge/UI-Responsive-purple)
![Project](https://img.shields.io/badge/Project-Educational-lightgrey)

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Application Workflow](#application-workflow)
- [ATS Scoring Approach](#ats-scoring-approach)
- [User Interface](#user-interface)
- [Limitations](#limitations)
- [Future Improvements](#future-improvements)
- [Author](#author)

---

## Overview

ATS Resume Analyser is a web application designed to help job seekers evaluate their resumes and identify relevant skills for a target job.

Users can create an account, upload a resume in PDF format, extract resume text, identify recognized technical skills, and receive a rule-based score. The application also compares recognized resume skills against skills identified in a job description.

The application provides a dashboard where users can access their saved resume analyses and review detailed results.

This project demonstrates full-stack web development, file handling, PDF text extraction, authentication, database integration, and rule-based text analysis using Django.

## Features

- **User Authentication:** Register and log in to access the application.
- **PDF Resume Upload:** Upload resumes in PDF format.
- **Text Extraction:** Extract text from supported PDF documents.
- **Skill Detection:** Identify recognized technical skills using a predefined skill list and regular expressions.
- **Rule-Based Resume Scoring:** Calculate a score using predefined resume criteria.
- **Job Description Matching:** Compare recognized resume skills with skills found in a job description.
- **Matched Skills:** Display skills detected in both the resume and job description.
- **Missing Skills:** Highlight job-description skills not detected in the resume.
- **Resume Section Checks:** Check for selected resume sections and keywords.
- **Personal Dashboard:** View saved resume analyses.
- **Resume Details:** Review individual analysis results.
- **PDF Report Download:** Download analysis reports where supported by the application.
- **Responsive Interface:** Use the application on desktop and mobile-sized screens.

## Technology Stack

### Backend

- Python
- Django
- Django REST Framework

### Frontend

- HTML5
- CSS3
- Bootstrap 5

### Database

- SQLite

### PDF Processing

- PyPDF
- ReportLab for PDF report generation

### Development Tools

- Git
- GitHub
- Visual Studio Code

---

## Project Structure

```text
ats-resume-analyser/
├── accounts/
├── analysis/
├── authentication/
├── backend/
├── resumes/
│   ├── migrations/
│   ├── static/
│   │   └── resumes/
│   │       └── css/
│   │           └── app.css
│   ├── templates/
│   │   ├── base.html
│   │   ├── dashboard.html
│   │   ├── login.html
│   │   ├── my_resumes.html
│   │   ├── register.html
│   │   ├── results.html
│   │   ├── resume_detail.html
│   │   └── upload.html
│   ├── models.py
│   ├── serializers.py
│   ├── urls.py
│   ├── utils.py
│   └── views.py
├── .gitignore
├── manage.py
├── requirements.txt
└── README.md
```
## Getting Started

Follow these steps to run the project locally.

### Prerequisites

- Python 3.9 or later
- pip
- Git

### Installation

**1. Clone the repository**

```bash
git clone https://github.com/Aysha486/ats-resume-analyser.git
cd ats-resume-analyser
```

**2. Create a virtual environment**

For macOS/Linux:

```bash
python3 -m venv venv
source venv/bin/activate
```

For Windows:

```bash
python -m venv venv
venv\Scripts\activate
```

**3. Install dependencies**

```bash
pip install -r requirements.txt
```

**4. Apply database migrations**

```bash
python manage.py migrate
```

**5. Start the development server**

```bash
python manage.py runserver
```

Open http://127.0.0.1:8000/ in your browser.

## Application Workflow

1. Register for an account or log in.
2. Upload a resume in PDF format.
3. Enter or provide a job description, if supported by the application.
4. The application extracts text from the uploaded resume.
5. The system identifies relevant skills and compares them with the job requirements.
6. An ATS-style score and analysis are displayed.
7. Review the results to identify skills that may need improvement.

## ATS Scoring Approach

The application uses rule-based analysis to evaluate resume content.

The analysis may include:

* Skill identification: Detects predefined skills in extracted resume text.
* Job description matching: Identifies skills shared between the resume and the job description.
* Score calculation: Generates an ATS-style score using predefined matching rules.
* Results: Presents the analysis to help users understand how closely their resume matches the specified job requirements.
Note: The score is an estimate produced by this application. It is not an official score from an applicant tracking system, and actual recruitment systems may use different criteria.

## User Interface

The application provides a redesigned interface for its resume analysis workflow.

The interface includes pages for account access, resume upload, and displaying analysis results, according to the implemented features.

## Limitations

* Skill detection depends on the predefined skill list and matching rules.
* Resume text extraction may be affected by PDF formatting or scanned documents.
* The scoring system is rule-based and does not represent the evaluation criteria of every ATS.
* Results depend on the content and quality of the uploaded resume and job description.
* The application should not be treated as a guarantee of interview selection.

## Future Improvements

Potential enhancements include:

* Expanding the skill database.
* Improving skill matching using natural language processing.
* Supporting additional resume formats.
* Improving analysis of resume structure and readability.
* Adding more detailed suggestions for improving resumes.
* Enhancing deployment, testing, and security.

## Author

**Aysha Nuha**

GitHub: [Aysha486](https://github.com/Aysha486)

## Disclaimer

This project is intended for educational and resume-improvement purposes.
The scores are estimates and do not guarantee recruitment outcomes.