# Student ERP System

A simple web-based Student ERP (Enterprise Resource Planning) system built using Django and MariaDB. This project was created as a learning exercise to understand how Django works with a real relational database, covering models, views, templates, and forms.

## Features

- Add, view, edit, and delete student records
- Manage courses
- Mark and view student attendance
- Basic dashboard showing total students, courses, and attendance records
- Django admin panel for quick data management

## Tech Stack

- **Backend:** Python, Django
- **Database:** MariaDB (via PyMySQL)
- **Frontend:** HTML, Bootstrap 5 (CDN)

## Project Structure

student_erp/
├── manage.py
├── student_erp/ # Project settings, URLs
├── students/ # Main app (models, views, forms, urls)
├── templates/ # HTML templates
└── requirements.txt


## Setup Instructions

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/student-erp-django.git
cd student-erp-django
```

### 2. Create and activate a virtual environment
```bash
python -m venv menv
menv\Scripts\activate      # Windows
source menv/bin/activate   # Mac/Linux
```

### 3. Install dependencies
```bash
python -m pip install -r requirements.txt
```

### 4. Set up environment variables
Create a `.env` file in the project root:

SECRET_KEY=your-secret-key
DB_NAME=student_erp_db
DB_USER=root
DB_PASSWORD=your_mariadb_password
DB_HOST=localhost
DB_PORT=3306


### 5. Create the MariaDB database
```sql
CREATE DATABASE student_erp_db;
```

### 6. Run migrations
```bash
python manage.py makemigrations
python manage.py migrate
```

### 7. Create a superuser (for admin access)
```bash
python manage.py createsuperuser
```

### 8. Run the development server
```bash
python manage.py runserver
```

Visit `http://127.0.0.1:8000/` in your browser.

> **Note:** Add at least one Course via `/admin/` before adding students, since each student must be linked to a course.

## Future Improvements

- User authentication for students/teachers
- Search and filter functionality
- Export attendance/reports as PDF or Excel
- Improved UI/UX

## License

This project is for learning purposes and is free to use or modify.
