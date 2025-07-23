# 💬 Stack Overflow Clone

A full-featured Stack Overflow clone built using Django, PostgreSQL, and Redis. This project replicates the core functionalities of Stack Overflow, including Q&A threads, reputation, badges, bounties, review queues, and markdown previews — providing insights into how a complex Q&A system works behind the scenes.

---

## 🔧 Tech Stack

- **Language**: Python 3.7.x  
- **Framework**: Django 3.2.x  
- **Database**: PostgreSQL 14  
- **Cache/Queue**: Redis 5.x  
- **Frontend**: Bootstrap 4, jQuery 3  
- **Others**: Django ORM, Markdown, Django Admin

---

## ✨ Key Features

- 🛡️ 50+ **Badges** implemented for user achievements  
- 🏆 **Reputation system** based on user activity  
- 🔐 20+ **Privileges** awarded based on reputation  
- 📢 **Activity & Privilege Notifications**  
- 💬 **Live Markdown Preview** for Q&A posts  
- 🔗 User **@mentioning** in comments  
- 🎯 **Bounties**: Create, award, and track with countdown  
- 📝 **Review Queues**:
  - First Question/Answer Reviews  
  - Late Answers  
  - Flagged Posts & Comments  
  - Suggested Edits  
  - Close & ReOpen Votes  
  - Low-Quality Posts

## 🗂️ Setup Instructions

### 1. Clone the Repository
    ```bash
    git clone https://github.com/Yawan-1/StackOverFlow--Clone.git
    cd StackOverFlow--Clone



2. Set Up PostgreSQL Database
Create a new database and user in PostgreSQL shell:

    ```sql
    CREATE DATABASE so_clone;
    CREATE USER so_clone_user WITH PASSWORD 'password';
    GRANT ALL PRIVILEGES ON DATABASE so_clone TO so_clone_user;
3. Update settings.py
Edit the DATABASES section in your settings.py file:

    ```python

    DATABASES = {
      'default': {
          'ENGINE': 'django.db.backends.postgresql_psycopg2',
          'NAME': 'so_clone',
          'USER': 'so_clone_user',
          'PASSWORD': 'password',
          'HOST': 'localhost',
          'PORT': '',
      }
    }
 You can also use SQLite by commenting out the PostgreSQL config and enabling the SQLite one.

4. Install Dependencies
    ```bash

    pip install -r requirements.txt
5. Apply Migrations
    ```bash

    python manage.py makemigrations
    python manage.py migrate


6. Run the Server
    ```bash
    python manage.py runserver
Visit http://127.0.0.1:8000/ in your browser.
