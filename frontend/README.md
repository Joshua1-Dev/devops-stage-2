# Frontend - ReactJS with ChakraUI

This directory contains the frontend of the application built with ReactJS and ChakraUI.

## Prerequisites

- Node.js (version 14.x or higher)
- npm (version 6.x or higher)

## Setup Instructions

### Local Setup

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

### Docker Setup

1. **Build the Docker image**:
    ```sh
    docker build -t react-frontend .
    ```

2. **Run the Docker container**:
    ```sh
    docker run -d --name react-frontend-container -p 80:80 react-frontend
    ```

3. **Check the logs** (optional):
    ```sh
    docker logs -f react-frontend-container
    ```

4. **Stop the Docker container**:
    ```sh
    docker stop react-frontend-container
    ```

### Notes

- Ensure your backend API URL is correctly set in the `.env` file to enable proper communication between the frontend and backend.
- The Docker setup uses a multi-stage build to first compile the React app and then serve it with Nginx for a production-ready deployment.