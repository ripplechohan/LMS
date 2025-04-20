Learning Management System (PHP/MySQL)
A comprehensive Learning Management System built with PHP and MySQL, featuring course creation, student enrollment, progress tracking, interactive assessments, and detailed reporting.
Project Overview
This LMS is designed for educational institutions to manage their course offerings, student interactions, and administrative tasks. With separate interfaces for students, instructors, and administrators, the system provides a complete ecosystem for online learning.
Installation

Download the ZIP file from this repository
Extract the contents to your web server directory:

For XAMPP: Extract to C:\xampp\htdocs\LMS
For WAMP: Extract to C:\wamp\www\LMS
For Linux/Mac with LAMP: Extract to /var/www/html/LMS


Set up the database:

Open phpMyAdmin (typically at http://localhost/phpmyadmin)
Create a new database named lms
Import the DATABASE.sql file from the extracted folder


Configure database connection:

Open db_connection.php
Update the database credentials if needed (default is usually username: 'root', password: '')


Start your web server (Apache and MySQL)
Access the system by navigating to:

http://localhost/LMS/login.php



Features

User Management System

Different role types (Admin, Instructor, Student)
Registration and authentication
Profile management


Course Management

Course creation and editing
Content organization
Material uploading and downloading


Assessment System

Quiz creation and management
Assignment submission and grading
Automated and manual grading options


Reporting & Analytics

Student progress tracking
Detailed performance reports
Usage statistics


Communication Tools

Email notifications
Feedback system
AI-generated feedback (using Hugging Face API)


Administrative Features

User administration
Course assignment
System-wide reporting



File Structure
LMS/
├── css/                      # Stylesheets
├── js/                       # JavaScript files
├── fonts/                    # Web fonts
├── images/                   # Image assets
├── uploads/                  # Uploaded course materials
├── PHPMailer-6.9.3/          # Email functionality
├── cache/                    # System cache files
├── feedback_cache/           # Feedback cache
├── logs/                     # System logs
├── DATABASE.sql              # Database schema and initial data
│
├── User Management
│   ├── login.php             # User authentication
│   ├── register.php          # New user registration
│   ├── logout.php            # User logout
│   ├── profile.php           # User profile management
│   ├── add_user.php          # Admin user creation
│   ├── edit_user.php         # User data editing
│   ├── delete_user.php       # User removal
│   └── view_all_users.php    # User listing
│
├── Dashboards
│   ├── admin-dashboard.php   # Administrator interface
│   ├── Instructor-Dashboard.php  # Instructor interface
│   └── student-dashboard.php # Student interface
│
├── Course Management
│   ├── courses.php           # Course listing
│   ├── course-details.php    # Course information
│   ├── create_course.php     # Course creation
│   ├── admin_create_course.php  # Admin course creation
│   ├── edit_course.php       # Course editing
│   ├── admin_edit_course.php # Admin course editing
│   ├── delete_course.php     # Course removal
│   ├── enroll.php            # Student enrollment
│   ├── access-course.php     # Course access
│   ├── dropout.php           # Unenrollment
│   └── change_instructor.php # Instructor assignment
│
├── Assessment
│   ├── create_quiz.php       # Quiz creation
│   ├── manage_questions.php  # Quiz question management
│   ├── attempt_quiz.php      # Student quiz taking
│   ├── grade_quiz.php        # Quiz grading
│   ├── unpublish_quiz.php    # Hide quiz from students
│   ├── post_quiz.php         # Quiz publishing
│   ├── save_quiz_progress.php # Save incomplete quizzes
│   ├── create_assignment.php # Assignment creation
│   ├── Submission.php        # Assignment submission
│   ├── grade_assignment.php  # Assignment grading
│   ├── edit_assignment.php   # Assignment editing
│   └── delete_assignment.php # Assignment removal
│
├── Reports & Communications
│   ├── reports.php           # Reporting system
│   ├── admin_reports.php     # Administrator reports
│   ├── email_system.php      # Email notifications
│   ├── email_utils.php       # Email utilities
│   ├── view_email_logs.php   # Email history
│   ├── feedback.php          # Feedback system
│   ├── view_feedback.php     # Feedback viewing
│   └── generate_ai_feedback.php # AI-assisted feedback
│
└── Utilities
    ├── db_connection.php     # Database connection
    ├── autoload.php          # PHP class autoloader
    ├── download-material.php # File downloads
    ├── deadline_reminder_cron.php # Automated reminders
    ├── run_deadline_check.php # Deadline checking
    └── run_deadline_reminder.bat # Windows scheduled task
System Requirements

PHP 7.4 or higher
MySQL 5.7 or higher
Apache web server
XAMPP, WAMP, LAMP, or similar stack

Setup Notes

The system includes an email notification system using PHPMailer. Set up your SMTP details in the email configuration for this to work.
For the AI-generated feedback, you'll need to set up your Hugging Face API key in huggingface_api.php.
Default admin login credentials can be found in the DATABASE.sql file (but should be changed after installation).

Security Recommendations
For production use, consider implementing:

HTTPS for secure data transmission
Regular backup procedures
Input validation and sanitization (beyond what's already implemented)
Regular security updates

License
This project is provided for educational and demonstration purposes.

