# Full-Stack FastAPI and React APP

Welcome to the Full-Stack FastAPI and React template repository. This repository serves as a demo application for interns, showcasing how to set up and run a full-stack application with a FastAPI backend and a ReactJS frontend using ChakraUI.

## Project Structure

The repository is organized into two main directories:

- **frontend**: Contains the ReactJS application.
- **backend**: Contains the FastAPI application and PostgreSQL database integration.

Each directory has its own README file with detailed instructions specific to that part of the application.

## Getting Started

To get started with this template, please follow the instructions in the respective directories:

- [Frontend README](./frontend/README.md)
- [Backend README](./backend/README.md)

## Prerequisites

- Docker and Docker Compose installed on your machine
- Node.js (version 14.x or higher) and npm (version 6.x or higher) for local frontend setup
- Python 3.8 or higher and Poetry for local backend setup
- PostgreSQL for database setup

## Local Setup

### Backend

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

### Frontend

1. **Navigate to the frontend directory**:
    ```sh
    cd frontend
    ```

2. **Install dependencies**:
    ```sh
    npm install
    ```

3. **Run the development server with a specific IP address**:
    ```sh
    npm run dev -- --host 0.0.0.0 --port 3000
    ```

4. **Configure API URL**:
   Ensure the API URL is correctly set in the `.env` file.

## Docker Setup

### Docker Compose

1. **Build and start the services**:
    ```sh
    docker-compose up --build
    ```

2. **Stop the services**:
    ```sh
    docker-compose down
    ```

### Notes

- Ensure the `.env` files in both `frontend` and `backend` directories are correctly configured.
- The `docker-compose.yml` file defines the services for the frontend, backend, PostgreSQL, proxy manager, Adminer, and Nginx.