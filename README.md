Step by step guideline
version: "3.9"

services:
app:
build:
context: .
ports: - "8000:8000"
volumes: - ./app:/app
command: >
sh -c 'python manage.py runserver 0.0.0.0:8000'
environment: - DB_HOST=db - DB_NAME=devdb - DB_USER=devuser - DB_PASSWORD=changeme

db:
image: postgres:13-alpine
volumes: - dev-db-data:/var/lib/postgresql/data
environment: - POSTGRES_DB=devdb - POSTGRES_USER=devuser - POSTGRES_PASSWORD=changeme

volumes:
dev-db-data:
