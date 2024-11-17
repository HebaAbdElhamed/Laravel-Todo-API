# To-Do List API with Laravel

This is a RESTful API built with **Laravel** for To Do tasks. The API allows you to perform CRUD operations (Create, Read, Update, Delete) on tasks, which can be consumed by any front-end application or client (e.g., React, Vue, mobile apps, etc.).

## Features

- **Add Tasks**: Add new tasks by providing a name.
- **Edit Tasks**: Edit the name of an existing task.
- **Delete Tasks**: Delete individual tasks.
- **Delete All Tasks**: Delete all tasks in the database.

## Technologies Used

- **Laravel**: PHP framework for building the API.
- **RESTful API**: Standard approach for API design (GET, POST, PUT, DELETE).
- **MySQL** (or any database you configure): Used for storing tasks.

## Setup Instructions

Follow these steps to set up the API on your local machine:

### 1. Clone the repository

Clone the repository to your local machine:

    ```bash
    git clone https://github.com/HebaAbdElhamed/Laravel-Todo-API.git


### 2. Navigate to the project directory

    cd Laravel-Todo-API


### 3. Install dependencies using Composer

Make sure Composer is installed on your machine. If not, you can install it from here.

Install all the PHP dependencies:

    composer install


### 4. Configure your environment


Copy the .env.example file to create a .env file:

    cp .env.example .env

Edit the .env file to configure your database connection:

   
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=task_manager_db
    DB_USERNAME=root
    DB_PASSWORD=

Make sure to replace task_manager_db with your own database name, and update the DB_USERNAME and DB_PASSWORD based on your MySQL settings


### 5.  Run database migrations

To create the necessary tables in your database, run:

    php artisan migrate
    
This will create the tasks table in your database.

### 6. Start the Laravel development server

Run the following command to start the Laravel development server:

    php artisan serve

The server will be running at http://127.0.0.1:8000. You can access the API endpoints through this URL.

### 7. Test the API

You can test the API using tools like Postman, or connect it to any front-end application.

The following are the available API endpoints:

## API Endpoints
- **GET** /api/tasks: Fetch all tasks.
- **POST** /api/tasks: Create a new task (requires name).
- **PUT** /api/tasks/{id}: Update an existing task (requires name).
- **DELETE** /api/tasks/{id}: Delete a specific task.
- **DELETE** /api/tasks: Delete all tasks.

  
### Example of how to use the API:

#### 1. Add a Task (POST request)
**Endpoint:** /api/tasks
**Method:** POST

    
    {
      "name": "Complete Laravel API tutorial"
    }

    
#### 2. Edit a Task (PUT request)
**Endpoint:** /api/tasks/{id}
**Method:** PUT

    {
      "name": "Finish Laravel API tutorial"
    }

    
#### 3. Delete a Task (DELETE request)
**Endpoint:** /api/tasks/{id}
**Method:** DELETE

No request body is needed. Just pass the id of the task to be deleted.

#### 4. Delete All Tasks (DELETE request)
**Endpoint:** /api/tasks
**Method:** DELETE

No request body is needed. This will delete all tasks in the database.

## Front-End Integration
This API can be integrated with any front-end application such as React, Vue, or mobile applications. The front end can send HTTP requests (using libraries like Axios) to interact with this API.

If you want to use this API with React, here's the front-end repository you can check out:

React Front-End ToDo App


Author
Created by Heba AbdElhamed.
