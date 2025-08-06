# task_manager_api

A simple Ruby on Rails API to manage tasks with CRUD operations.

---

## API Endpoints

### 1. Create a Task

- **URL:** `POST /tasks`
- **Request Body:**

```json
{
  "title": "Buy groceries",
  "description": "Milk, Bread, Eggs",
  "completed": false
}
Response:

Returns the created task with its ID.

2. Read Tasks
URL: GET /tasks

Description: Lists all tasks.

URL: GET /tasks/:id

Description: Gets a single task by its ID.

3. Update a Task
URL: PUT /tasks/:id or PATCH /tasks/:id

Request Body: (Only include fields to update)

json
Copy
Edit
{
  "title": "Buy groceries and snacks",
  "completed": true
}
Response: Returns the updated task.

4. Delete a Task
URL: DELETE /tasks/:id

Description: Deletes the task with the given ID.

Example Using curl
Create
bash
Copy
Edit
curl -X POST http://localhost:3000/tasks \
-H "Content-Type: application/json" \
-d '{"title": "Test Task", "description": "My first task", "completed": false}'
List all tasks
bash
Copy
Edit
curl http://localhost:3000/tasks
Update task with ID 1
bash
Copy
Edit
curl -X PATCH http://localhost:3000/tasks/1 \
-H "Content-Type: application/json" \
-d '{"completed": true}'
Delete task with ID 1
bash
Copy
Edit
curl -X DELETE http://localhost:3000/tasks/1
