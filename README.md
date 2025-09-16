# Django Authentication Project

A Django project implementing a **complete user authentication system**, including login, logout, signup, password change, and password reset.
This project is beginner-friendly and based on [LearnDjango’s tutorial](https://learndjango.com/tutorials/django-login-and-logout-tutorial), but structured for reuse and easy deployment.

---

## ✨ Features

* 🔑 **User Signup** with form validation
* 🔓 **User Login & Logout**
* 🔒 **Password Change** (with old password confirmation)
* ✉️ **Password Reset via Email** (secure link sent to user email)
* 🖼️ **Customizable Templates** for authentication views
* 🛡️ **Secure authentication system** powered by Django’s built-in `auth` framework

---

## 🛠️ Tech Stack

* **Backend:** Django 5.x / 4.x
* **Database:** SQLite (default, can be swapped for PostgreSQL/MySQL)
* **Authentication:** Django’s `django.contrib.auth`

---

## 📂 Project Structure

```
.
├── accounts/                # Authentication app
│   ├── templates/
│   │   └── registration/    # Login, Signup, Reset, etc.
│   ├── urls.py
│   └── views.py
├── django_project/         # Project settings
│   ├── settings.py
│   ├── urls.py
│   └── ...
├── templates/               # Base templates
├── db.sqlite3               # SQLite database
├── manage.py
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation & Setup

1. **Clone the repository**

   ```bash
   git clone https://github.com/Aalphakeem-Adroit/Django-Trial.git
   cd Django-Trial
   ```

2. **Create and activate a virtual environment**

   ```bash
   python3 -m venv venv
   source venv/bin/activate    # Linux/Mac
   venv\Scripts\activate       # Windows
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Apply database migrations**

   ```bash
   python manage.py migrate
   ```

5. **Create a superuser (for admin access)**

   ```bash
   python manage.py createsuperuser
   ```

6. **Run the development server**

   ```bash
   python manage.py runserver
   ```

7. **Visit the app**

   * Homepage → `http://127.0.0.1:8000/`
   * Login → `http://127.0.0.1:8000/accounts/login/`
   * Signup → `http://127.0.0.1:8000/accounts/signup/`
   * Admin → `http://127.0.0.1:8000/admin/`

---

## 📧 Email Setup for Password Reset

By default, emails are sent to the console.

For production, configure SMTP in `settings.py`:

```python
EMAIL_BACKEND = "django.core.mail.backends.smtp.EmailBackend"
EMAIL_HOST = "smtp.gmail.com"
EMAIL_PORT = 587
EMAIL_USE_TLS = True
EMAIL_HOST_USER = "your_email@gmail.com"
EMAIL_HOST_PASSWORD = "your_app_password"
```

Use [Gmail App Passwords](https://support.google.com/accounts/answer/185833?hl=en) or another provider.

---

## 🔗 Authentication URLs

| URL                          | Description              |
| ---------------------------- | ------------------------ |
| `/accounts/signup/`          | User signup              |
| `/accounts/login/`           | User login               |
| `/accounts/logout/`          | User logout              |
| `/accounts/password_change/` | Change password          |
| `/accounts/password_reset/`  | Reset password via email |
| `/admin/`                    | Django admin panel       |

---

## 🚫 .gitignore

Make sure you don’t push local or sensitive files.
Example `.gitignore` for Django:

```
venv/
__pycache__/
*.pyc
*.sqlite3
.env
.DS_Store
```

---

## 🤝 Contributing

Contributions are welcome!
Fork the repo, create a feature branch, and submit a pull request.

---

## 📜 License

Licensed under the **MIT License** – free to use, modify, and distribute.