# Online Course App (Django)

An online course web application built with Django. Users can browse courses, enroll, view lessons, take an exam at the end of a course, and see their exam results.

## Features

- User registration, login, and logout
- Course list and course details pages
- Lessons displayed for each course
- Exam with multiple-choice questions for each course
- Exam submission and automatic grading
- Exam result page showing the score and correct, wrong, and missed answers
- Admin site for managing courses, lessons, questions, and choices

## Project Improvements

1. Created `Question`, `Choice`, and `Submission` models
2. Created a new course with exam-related models using the admin site
3. Updated the course details template to show questions and choices
4. Created a new exam result template to show the result of a submission
5. Created a new exam submission view
6. Created a new view to display and evaluate the exam result

## Models

| Model | Description |
|-------|-------------|
| `Course` | A course with a name, description, and image |
| `Lesson` | A lesson that belongs to a course |
| `Enrollment` | Links a user to a course |
| `Question` | An exam question for a course, with a grade value |
| `Choice` | A possible answer to a question, marked correct or not |
| `Submission` | The choices a user selected for an enrollment |

## Tech Stack

- Python 3
- Django
- SQLite
- HTML, Bootstrap

## Getting Started

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd <your-repository-folder>
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Apply migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

### 4. Create an admin user

```bash
python manage.py createsuperuser
```

### 5. Run the server

```bash
python manage.py runserver
```

Open `http://127.0.0.1:8000/onlinecourse/` in your browser. The admin site is at `http://127.0.0.1:8000/admin/`.

## Usage

1. Log in to the admin site and create a course, lessons, questions, and choices.
2. Sign up or log in as a learner and enroll in the course.
3. Open the course details page and select **Start Exam**.
4. Select your answers and submit.
5. View your score and answer review on the exam result page. A score above 80 passes.

## License

This project is for learning purposes.
