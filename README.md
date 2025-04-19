# JDMatcher

AI-powered recruitment tool to automate JD parsing, resume analysis, candidate shortlisting, and interview invitation via email using NLP and data intelligence.

 # Features
✅ Job Description Parsing from CSV

✅ Resume Extraction from PDF using PyMuPDF

✅ Named Entity Recognition with spaCy

✅ Fuzzy Matching to score candidate-job fit

✅ Candidate Shortlisting based on thresholds

✅ Automated Email Invitations via SMTP

✅ SQLite DB Integration for data persistence

# Tech Stack
Python 🐍

SQLite 🗃️

spaCy (NLP) 🧠

fuzzywuzzy (matching) 🔍

PyMuPDF (PDF parsing) 📄

smtplib (email automation) 📧

pandas (data handling) 🐼

# Project Structure

/
│
├── job_description.csv         # Input file containing job roles and descriptions
├── CVs1/                       # Folder with resume PDFs
├── recruitment.db              # SQLite database (created at runtime)
├── main.py                     # Core logic for processing, matching & emailing
├── README.md                   # Project documentation

# System Architecture


[CSV File] --> [JD Processor] ---------\
                                        \
                                         --> [SQLite DB] <--> [Matcher + Scorer] --> [Shortlister] --> [Email Sender]
                                        /
[PDF Resumes] --> [Text Extractor] ----/
