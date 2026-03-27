
# FastAPI Issue Tracker

A REST API built with FastAPI for managing and persisting issues to a JSON-based storage system. This project demonstrates CRUD operations, data validation with Pydantic, and modular routing.

## Features

* **CRUD Operations:** Create, Read, Update, and Delete issues.
* **Data Persistence:** Stores data in `data/issues.json`.
* **Validation:** Data validation and serialization using Pydantic schemas.
* **Documentation:** Auto-generated API documentation via Swagger UI.

## Project Structure


.
├── app/
│   ├── routes/
│   │   └── issues.py
│   ├── schemas.py
│   └── storage.py
├── data/
│   └── issues.json
├── main.py
├── .gitignore
└── LICENSE


## Installation

1.  Clone the repository:
    ```bash
    git clone <repository-url>
    cd <project-directory>
    ```

2.  Create and activate a virtual environment:
    ```bash
    python -m venv venv
    # Windows:
    venv\Scripts\activate
    # macOS/Linux:
    source venv/bin/activate
    ```

3.  Install dependencies:
    ```bash
    pip install fastapi uvicorn
    ```

## Usage

Start the server using Uvicorn:

```bash
uvicorn main:app --reload
```




## Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/issues` | Create a new issue |
| GET | `/issues/{id}` | Retrieve a specific issue |
| PUT | `/issues/{id}` | Update an existing issue |
| DELETE | `/issues/{id}` | Remove an issue |

