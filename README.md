# 🧠 Django REST Framework Social API

A simple yet powerful **Django REST Framework (DRF)** project that implements user authentication and CRUD functionality for **Posts** and **Comments**.  
This project can serve as a starter template for building any social-media-like backend.

---

## 🚀 Features

- 🔐 **User Authentication** (JWT / Token based)
- 🧍 **User Registration & Login APIs**
- 📝 **CRUD operations for Posts**
- 💬 **CRUD operations for Comments**
- 🌐 RESTful API endpoints with Django REST Framework
- ⚙️ Built with Django 5+ and DRF 3+

---

## 🏗️ Project Structure

social_api/
│
├── feed/ # App for managing posts & comments
├── users/ # App for managing user authentication
├── social_api/ # Project settings and configurations
├── manage.py
└── requirements.txt

yaml
Copy code

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the repository
```bash
git clone https://github.com/PraneetNS/django_rest_framework.git
cd django_rest_framework
2️⃣ Create and activate a virtual environment
bash
Copy code
python -m venv venv
venv\Scripts\activate     # On Windows
# source venv/bin/activate   # On macOS/Linux
3️⃣ Install dependencies
bash
Copy code
pip install -r requirements.txt
4️⃣ Apply migrations
bash
Copy code
python manage.py makemigrations
python manage.py migrate
5️⃣ Create a superuser
bash
Copy code
python manage.py createsuperuser
6️⃣ Run the development server
bash
Copy code
python manage.py runserver
🔑 Authentication (Example using DRF’s Token Auth)
Obtain a token:

bash
Copy code
POST /api/token/
{
    "username": "your_username",
    "password": "your_password"
}
Use the token in requests:

makefile
Copy code
Authorization: Bearer <your_access_token>
📘 API Endpoints Overview
HTTP Method	Endpoint	Description
POST	/api/register/	Register new user
POST	/api/token/	Obtain access token
GET	/api/posts/	List all posts
POST	/api/posts/	Create a post
GET	/api/posts/<id>/	Retrieve a post
PUT	/api/posts/<id>/	Update a post
DELETE	/api/posts/<id>/	Delete a post
GET	/api/comments/	List all comments
POST	/api/comments/	Create a comment

🧠 Example JSON Body for POST
Create Post
json
Copy code
POST /api/posts/
{
    "title": "My First Post",
    "content": "This is an example post created via Django REST API."
}
Create Comment
json
Copy code
POST /api/comments/
{
    "post": 1,
    "text": "This is a comment on the first post."
}
🧰 Tech Stack
Backend: Django 5.x

API Framework: Django REST Framework (DRF)

Database: SQLite (can easily switch to PostgreSQL)

Auth: JWT / Token Authentication

Language: Python 3.13+

💡 Future Enhancements
🔁 Add Like/Unlike functionality for posts

🧾 Add pagination and filtering

📸 Add media upload (images for posts)

🌍 Add deployment on Render or Heroku

👨‍💻 Author
Praneet N.S
📍 Django Developer | AI Enthusiast
🌐 GitHub Profile

🧩 License
This project is open-source under the MIT License — feel free to fork, modify, and use it for your own learning or projects!

java
Copy code
MIT License
Copyright (c) 2025 Praneet
✅ Quick Commands Summary
Command	Purpose
python manage.py runserver	Start Django server
python manage.py createsuperuser	Create admin user
python manage.py makemigrations	Prepare model changes
python manage.py migrate	Apply database changes
pip freeze > requirements.txt	Export dependencies
