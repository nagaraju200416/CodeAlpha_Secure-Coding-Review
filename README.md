# Secure Code Audit Project

## Overview
This project demonstrates a security-focused code audit of a Python Flask web application.

The audit covers:
- Manual code review
- Static analysis with Bandit
- Dependency checking with pip-audit
- Identification and documentation of security vulnerabilities
- Secure coding recommendations
- Remediation of identified issues

## Application
**Language:** Python 3  
**Framework:** Flask  
**Application:** Secure Notes Web Application

## Project Structure
```text
Secure_Code_Audit_Project/
├── app.py
├── requirements.txt
├── requirements-audit.txt
├── requirements-secure.txt
├── run.py
├── vulnerable_app/
│   └── app.py
├── secure_app/
│   └── app.py
├── audit/
│   ├── SECURITY_AUDIT_REPORT.md
│   ├── FINDINGS.md
│   └── remediation_notes.md
├── tests/
│   └── test_security.py
├── .gitignore
└── LICENSE
```

## Setup
```bash
python -m venv venv
```

Windows:
```bash
venv\Scripts\activate
```

Linux/macOS:
```bash
source venv/bin/activate
```

Install dependencies:
```bash
pip install -r requirements-secure.txt
```

Run:
```bash
python run.py
```

Open:
```text
http://127.0.0.1:5000
```

## Security Audit Tools

Install audit tools:
```bash
pip install bandit pip-audit
```

Run Bandit:
```bash
bandit -r vulnerable_app secure_app
```

Run dependency audit:
```bash
pip-audit -r requirements-secure.txt
```

Run tests:
```bash
python -m unittest discover -s tests -v
```

## Main Vulnerabilities Demonstrated

The intentionally vulnerable application demonstrates common issues for educational auditing:

1. Hard-coded secret key
2. Debug mode enabled
3. SQL injection risk
4. Cross-site scripting risk through unsafe HTML rendering
5. Weak password handling
6. Missing CSRF protection
7. Missing security headers
8. Excessive error information

The secure version demonstrates safer alternatives.

## Important
The vulnerable application is intentionally insecure and should only be run locally for educational testing. Do not deploy it to the public internet.

## GitHub
Suggested repository name:

`secure-code-audit-python-flask`

Example commands:
```bash
git init
git add .
git commit -m "Initial secure code audit project"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/secure-code-audit-python-flask.git
git push -u origin main
```
