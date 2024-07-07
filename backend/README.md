# Backend - FastAPI with PostgreSQL

This directory contains the backend of the application built with FastAPI and PostgreSQL.

## Prerequisites

- Python 3.8 or higher
- Poetry (for dependency management)
- PostgreSQL (ensure the database server is running)

### Installing Poetry

To install Poetry, follow these steps:

```sh
curl -sSL https://install.python-poetry.org | python3 -
```

Add Poetry to your PATH (if not automatically added):

```sh
export PATH="$HOME/.poetry/bin:$PATH"
```

## Setup Instructions

### Local Setup

1. **Navigate to the backend directory**:
    ```sh
    cd backend
    ```

2. **Install dependencies using Poetry**:
    ```sh
    poetry install
    ```

3. **Set up the database with the necessary tables**:
    ```sh
    poetry run bash ./prestart.sh
    ```

4. **Run the backend server with a specific IP address**:
    ```sh
    poetry run uvicorn app.main:app --host 0.0.0.0 --port 8000 --reload
    ```

5. **Update configuration**:
   Ensure you update the necessary configurations in the `.env` file, particularly the database configuration.

### Docker Setup

1. **Build the Docker image**:
    ```sh
    docker build -t fastapi-backend .
    ```

2. **Run the Docker container**:
    ```sh
    docker run -d --name fastapi-backend-container -p 80:80 fastapi-backend
    ```

3. **Check the logs** (optional):
    ```sh
    docker logs -f fastapi-backend-container
    ```

4. **Stop the Docker container**:
    ```sh
    docker stop fastapi-backend-container
    ```

### Notes

- Ensure your PostgreSQL database is running and accessible from the application.
- Update the `.env` file with the correct database connection details and other configurations.
- The `prestart.sh` script should handle database migrations and any initial setup required by the application.