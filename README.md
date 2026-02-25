<div style="font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; line-height:1.6;">

# Easy JobPortal 🚀

[![Python](https://img.shields.io/badge/Python-3.11-blue)](https://www.python.org/)
[![Django](https://img.shields.io/badge/Django-5.2.11-green)](https://www.djangoproject.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow)](LICENSE)

**Easy JobPortal** is a professional web-based job portal built with **Django**, designed for job seekers and employers.

---

## 🌟 Key Features

### Job Seekers
- Register, login, and verify account.
- Upload and manage resume.
- Search and apply for jobs.
- Track application status.

### Employers / Admin
- Post, edit, and delete jobs.
- View applicants and make hiring decisions.
- Search and manage posted jobs.

### General
- Fully modular structure (`accounts`, `jobs`, `common`).
- Responsive templates and reusable components.
- Secure authentication & email verification.
- Fully tested with **pytest**.

---

## ⚡ Professional Highlights
1. **Clean Startup:** Old company names replaced with `Easy JobPortal` — portfolio-ready.  
2. **Tested & Modular:** Demonstrates Django best practices, full-stack skills.  
3. **Production-Ready Features:** Authentication, CRUD, email verification, password reset.  
4. **Step-by-Step Setup:** Easy for recruiters to run locally and explore.

---

## 🛠 Setup (Quick)

<div style="font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; font-size:16px; background-color:#f8f8f8; padding:10px; border-radius:5px;">
<pre>
git clone https://github.com/krishnalimahajan35/easy-jobportal.git
cd easy-jobportal
python -m venv venv

# Activate venv
# Windows (PowerShell): .\venv\Scripts\Activate.ps1
# Linux/Mac: source venv/bin/activate

pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
</pre>
</div>

Open [http://127.0.0.1:8000/](http://127.0.0.1:8000/) in your browser.

---

## ✅ Testing

<div style="font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; font-size:16px; background-color:#f8f8f8; padding:10px; border-radius:5px;">
<pre>
pytest  # All tests passed ✅
</pre>
</div>

---

## 🌀 Celery Worker & Flower Dashboard

<div style="font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; font-size:16px; background-color:#f8f8f8; padding:10px; border-radius:5px;">
<pre>
# Start Celery worker for handling background tasks
celery -A talent_base worker --loglevel=info

# Start Flower dashboard to monitor Celery tasks
celery -A talent_base flower --port=5555
</pre>
</div>

Open Flower dashboard in your browser at: [http://127.0.0.1:5555](http://127.0.0.1:5555)

---

## 📁 Project Structure

easy-jobportal/
├── accounts/ # User registration, login, password management
├── jobs/ # Job postings & applications
├── common/ # Reusable utilities & templates
├── templates/ # HTML templates
├── manage.py
└── requirements.txt
