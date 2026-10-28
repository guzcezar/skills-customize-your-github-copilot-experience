# 📘 Assignment: Building REST APIs with FastAPI

## 🎯 Objective

Build a small REST API with FastAPI to practice defining endpoints, modeling data, and using HTTP methods and status codes. You will create an in-memory task tracker and test it through FastAPI's interactive documentation.

## 📝 Tasks

### 🛠️ Create the FastAPI Application

#### Description
Set up a Python application with FastAPI and create endpoints that introduce the task-tracker API.

#### Requirements
Completed program should:

- Install FastAPI and Uvicorn in a Python environment
- Create an `app.py` file with a FastAPI application named `app`
- Define `GET /` to return a short welcome message and `GET /tasks` to return an initially empty list
- Start the application with Uvicorn and confirm the endpoints respond in the browser or an HTTP client


### 🛠️ Add Task Creation and Retrieval

#### Description
Represent tasks as structured data and let API clients create tasks and retrieve them by ID.

#### Requirements
Completed program should:

- Define a Pydantic model for a task with a required, non-empty `title` and an optional `completed` field that defaults to `false`
- Implement `POST /tasks` to create a task, assign it a unique integer ID, store it in memory, and return the created task
- Return HTTP status `201 Created` when a task is created successfully
- Implement `GET /tasks/{task_id}` to return one task, or HTTP status `404 Not Found` when the ID does not exist


### 🛠️ Complete and Test the REST API

#### Description
Add update and delete operations, then use FastAPI's interactive API documentation to test normal and error cases.

#### Requirements
Completed program should:

- Implement `PUT /tasks/{task_id}` to update a task's title and completion state, returning `404 Not Found` for an unknown ID
- Implement `DELETE /tasks/{task_id}` to remove a task and return HTTP status `204 No Content`, or `404 Not Found` if it does not exist
- Ensure invalid task data is rejected with a clear validation response
- Open `/docs` and test creating, listing, retrieving, updating, and deleting tasks, including at least one invalid request and one unknown ID
