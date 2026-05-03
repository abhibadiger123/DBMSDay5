# 🍹 APIRD: Drinks Management API

A robust RESTful API built with **Django 5.1** and **Django REST Framework** for managing a catalog of drinks. This project is structured for global scalability with extensive localization support.

---

## 📁 Project Structure
```text
APIRD/
├── APIRD/              # Project Configuration
│   ├── settings.py     # Global Settings
│   ├── urls.py         # Root URL Routing
│   ├── asgi.py         # ASGI configuration for deployment
│   └── wsgi.py         # WSGI configuration for deployment
├── Drinks/             # Main Application Logic
│   ├── migrations/     # Database Evolution files
│   ├── templates/      # HTML templates (e.g., index.html)
│   ├── models.py       # Database Schema
│   ├── serializers.py  # Data Serialization logic
│   ├── views.py        # API Request/Response Handling
│   └── admin.py        # Admin interface registration
├── venv/               # Virtual Environment & Django i18n Files
├── manage.py           # Django Admin Utility
└── db.sqlite3          # Local SQLite Database
