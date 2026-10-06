# Facial Recognition Attendance System

A Flask-based attendance system that uses face recognition to automatically mark student attendance. Built as a 4th year project.

## Features

- User signup and login with student / admin roles
- Student registration with webcam face capture
- Face encoding stored in a local SQLite database
- Attendance marking via live face recognition
- Admin dashboard showing attendance records
- Automatic Excel export of attendance history

## Tech Stack

- **Backend:** Flask, SQLite
- **Computer Vision:** OpenCV, dlib, face_recognition
- **Data:** pandas (Excel export)
- **Image handling:** Pillow
- **Frontend:** HTML, CSS (Jinja2 templates)

## Project Structure

capture/
├── main.py # Flask app and all routes
├── attendance.db # SQLite database (created on first run)
├── attendance.xlsx # Attendance export (created on first mark)
├── requirements.txt
├── templates/ # HTML templates
│ ├── signup.html
│ ├── login.html
│ ├── student.html
│ └── admin.html
└── static/
├── styles.css
├── logo.png
└── student_images/ # Captured face images
text

## Setup

### 1. Clone the repo

```bash
git clone https://github.com/Sparrowlen1/Facial-recognition-4thyrremake-.git
cd Facial-recognition-4thyrremake-
2. Create and activate a virtual environment
bash
python -m venv .venv
.venv\Scripts\Activate.ps1        # Windows PowerShell
# source .venv/bin/activate        # macOS / Linux
3. Install dependencies
bash
pip install -r requirements.txt
If face_recognition_models fails to install from PyPI, install it from GitHub:

bash
pip install git+https://github.com/ageitgey/face_recognition_models
4. Run the app
bash
python main.py
Then open http://127.0.0.1:5000/ in your browser.

Usage
Sign up as either a student or admin.

As a student, register your details — the app opens your webcam and captures a photo to generate a face encoding.

Use Mark Attendance to record your attendance via face recognition.

As an admin, view all attendance records on the dashboard.

Notes
A webcam is required for registration and attendance marking.

The database schema is created automatically on first run.

To reset all data, delete attendance.db and restart the app.

License
This project is for academic use.
