# 🚫 Custom 404 Page - Flask App

This is a lightweight, production-ready **Flask application** that displays a **beautiful custom 404 error page** with a redirect button to a home URL.

![screenshot](https://user-images.githubusercontent.com/your-image-path/404-preview.png)

---

## 🔧 Features

- Clean and responsive 404 design
- Simple and customizable HTML/CSS
- Production-ready using Gunicorn
- Lightweight Docker container (`python:3.12-slim`)
- Enhanced with essential security headers

---

## 🔗 Redirect Button Target

> Clicking "Go Home" redirects the user to:
```
https://192.168.187.202/dkp/kommander/dashboard
```

---

## 📁 Project Structure

```
flask_404_app/
├── app.py
├── requirements.txt
├── Dockerfile
├── templates/
│   └── 404.html
└── static/
    └── css/
        └── style.css
```

---

## 🚀 Setup (Development)

```bash
# Clone the repository
git clone https://github.com/your-username/flask-404-app.git
cd flask-404-app

# Create virtual environment
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt

# Run the app locally
python app.py
```

Visit `http://127.0.0.1:5000/nonexistent` to see the 404 page in action.

---

## 🐳 Docker Build

```bash
docker build -t flask-404-app .
```

> ⚠️ The image is built using `python:3.12-slim` with Gunicorn for better performance in production.

---

## 🛡️ Security Features

- **X-Frame-Options**: Deny clickjacking
- **X-XSS-Protection**: Enable browser XSS filter
- **X-Content-Type-Options**: Prevent MIME sniffing
- **Content-Security-Policy**: Basic CSP rule
- **Referrer-Policy**: No referrer leakage

---

## 📄 License

This project is licensed under the MIT License. Feel free to use and customize.
