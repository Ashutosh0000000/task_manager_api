# task_manager_api
Task Manager API
A simple RESTful API built with Ruby on Rails to manage tasks, including task title, description, and completion status.

Features
Create, read, update, and delete tasks

Task attributes: title, description, and completed (boolean)

Stores timestamps for creation and updates

Getting Started
Prerequisites
Ruby 3.4.x

Rails 8.0.x

PostgreSQL database

Setup
Clone the repository:

bash
Copy
Edit
git clone https://github.com/yourusername/task_manager_api.git
cd task_manager_api
Install dependencies:

bash
Copy
Edit
bundle install
Setup the database:

Make sure PostgreSQL is running, then run:

bash
Copy
Edit
rails db:create
rails db:migrate
Start the Rails server:

bash
Copy
Edit
rails server
Usage
You can interact with the API endpoints using tools like curl, Postman, or through your frontend app.

Example: Create a Task
bash
Copy
Edit
curl -X POST http://localhost:3000/tasks \
-H "Content-Type: application/json" \
-d '{"title": "Test Task", "description": "My first task", "completed": false}'
Example: List Tasks
bash
Copy
Edit
curl http://localhost:3000/tasks
Database Schema
The tasks table includes the following columns:

Column	Type	Description
id	integer	Primary key
title	string	Task title
description	text	Task description
completed	boolean	Task completion status
created_at	datetime	Timestamp for creation
updated_at	datetime	Timestamp for last update

Notes
Make sure to check migrations for column duplication issues.

Ruby warnings related to fiddle can be silenced by adding the fiddle gem to your Gemfile.

If you want, I can generate a markdown file you can save directly. Would you like that?




Ask ChatGPT


Attach

Search

Voice

ChatGPT can make mistakes. Check 
