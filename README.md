# Task-Management-fastapi
# TaskManagement API – FastAPI Project

A simple Task Management REST API built using **Python FastAPI**.  
This project supports user management, task assignment, status updates, and filtering.

---

## Tech Stack

- Python 3.8+
- FastAPI
- SQLAlchemy
- SQLite (local database)
- Swagger (auto-generated docs)

---

## How to Run This Project

### 1. Clone or Unzip this folder  
Make sure you're inside the `TaskManagementApi/` folder.

### 2. Create a virtual environment:


python -m venv venv


### 3. Activate the environment:



venv\Scripts\activate


### 4. Install dependencies:


pip install -r requirements.txt


### 5. Create the database:


python create_db.py


###  6. Start the server:


uvicorn main:app --reload




## API Access

- Root: [http://127.0.0.1:8000](http://127.0.0.1:8000)



## Sample Test Case

### Create a User

`POST /api/users`

```json
{
  "name": "LAHARI",
  "email": "lahari@example.com"
}
```

---

### Create a Task

`POST /api/tasks`

```json
{
  "title": "Submit API Project",
  "description": "Send working demo to HR",
  "due_date": "2025-07-20T17:00:00",
  "status": "Pending",
  "priority": "High",
  "user_id": 1
}
```

---

### Get All Tasks

`GET /api/tasks`

Response:

```json
[
  {
    "id": 1,
    "title": "Submit API Project",
    "description": "Send working demo to HR",
    "due_date": "2025-07-20T17:00:00",
    "status": "Pending",
    "priority": "High",
    "user_id": 1
  }
]
```

## Folder Structure

```
TaskManagementApi/
├── main.py
├── create_db.py
├── database.py
├── models/
├── schemas/
├── services/
├── routers/
├── requirements.txt
└── README.md
```
