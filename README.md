# IS601 Module 10: FastAPI Secure User Model and CI/CD Pipeline

## Objective
For this assignment, I enhanced my FastAPI application by implementing a secure user model using SQLAlchemy and Pydantic. I also integrated password hashing, write tests, and configure a full CI/CD pipeline with GitHub Actions and Docker Hub.

## My Github Repository
https://github.com/DesRoca/module10_assignment

## My Github Actions Workflow
https://github.com/DesRoca/module10_assignment/actions/runs/42560190279

## My DockerHub Image
https://hub.docker.com/r/desroca/601_module9/tags

# Instructions

## Running Tests Locally

### Prerequisites
- Python 3.12
- PostgreSQL
- Docker Desktop
- Git

1. Clone the repository

git clone https://github.com/DesRoca/module10_assignment.git
cd module10_assignment

2. Create and activate a virtual environment

python3 -m venv venv
source venv/bin/activate

3. Install dependencies

python -m pip install --upgrade pip
pip install -r requirements.txt

4. Configure the database

Make sure your PostgreSQL database is running and the DATABASE_URL environment variable is configured correctly.

Example database connection string:

DATABASE_URL=postgresql://postgres:postgres@localhost:5432/fastapi_db

Update the connection string to match your local PostgreSQL configuration.

5. Run the tests

Run the complete test suite:

pytest

To run individual test categories:

Unit tests:

pytest -vv --tb=short tests/unit/

Integration tests:

pytest -vv --tb=short tests/integration/

End-to-end tests:

pytest -vv -s --tb=short tests/e2e/

Integration and end-to-end tests require the appropriate database and application dependencies to be running.

### Docker Hub

The Docker image is automatically built and deployed to Docker Hub through the GitHub Actions workflow after successful testing and security scanning on the main branch.

### Docker Hub Repository:

https://hub.docker.com/r/desroca/601_module9

Pull the latest image using:

docker pull desroca/601_module9:latest

