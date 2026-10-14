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