# Task Management App - Laravel Machine Test
## Overview
This is a simple Task Management Application built using
**Laravel**
. The application allows users to perform basic CRUD (Create, Read, Update, Delete) operations on tasks stored in a
**MySQL**
database.
## Features
-
**Add a Task**
: Users can add new tasks with a title and description.
-
**List Tasks**
: All tasks are listed on the main page.
-
**Edit a Task**
: Users can edit an existing task's title or description.
-
**Delete a Task**
: Users can delete tasks from the list.
## Technology Stack
-
**Backend**
: Laravel (PHP Framework)
-
**Database**
: MySQL (or any SQL database)
-
**Frontend**
: Blade templates, HTML5, CSS (basic styling)
-
**Database Queries**
: Eloquent ORM for database operations
## Prerequisites
Before running this application, ensure the following are installed:
-
**PHP**
: Version 8.1+ recommended ([Download PHP](https://www.php.net/))
-
**Composer**
: Dependency manager for PHP ([Download Composer](https://getcomposer.org/))
-
**MySQL**
: Database server ([Download MySQL](https://www.mysql.com/))
## Setup Instructions
1.
**Clone the Repository**
:
  ```bash
  git clone
https://github.com/your-repo/task-management-laravel.git
  cd task-management-laravel
2.
Install Dependencies
:
composer install

3.
Environment Setup
:
• Copy the .env.example file to .env:
cp .env.example .env

• Update the .env file with your database credentials:
DB_DATABASE=task_management
DB_USERNAME=your_mysql_username
DB_PASSWORD=your_mysql_password

4.
Database Setup
:
• Create a new MySQL database called task_management.
• Run the migrations to create the necessary tables:
php artisan migrate

5.
Serve the Application
:
php artisan serve
The application will be accessible at http://localhost:8000.

Database Structure

The tasks table will be created using Laravel migrations with the following structure:
Schema::create('tasks', function (Blueprint $table) {
   $table->id();
   $table->string('title', 255);
   $table->text('description')->nullable();
   $table->timestamps();
});

Usage

• Navigate to
http://localhost:8000
to access the application.
• Use the “Add Task” form to create new tasks.
• View all tasks on the main page.
• Edit or delete tasks as needed.

Example SQL for Tasks Table

If you prefer to create the table manually, you can use the following SQL:
CREATE TABLE tasks (
   id INT AUTO_INCREMENT PRIMARY KEY,
   title VARCHAR(255) NOT NULL,
   description TEXT,
   created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
   updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
);
