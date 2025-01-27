
# Rust CRUD API with Docker
A simple CRUD (Create, Read, Update, Delete) API built with Rust and PostgreSQL, containerized using Docker.


## Features

- RESTful API endpoints for user management
- PostgreSQL database integration
- Docker containerization
- Basic user operations:
  - Create new user records
  - Retrieve user information
  - Update existing user details
  - Delete user records

## Prerequisites

- Docker and Docker Compose
- Rust (if running locally)
- PostgreSQL (if running locally)

## Tech Stack

- Rust
- PostgreSQL
- Docker
- Docker Compose

## Project Structure
```
rust-crud-api/
├── src/
│   └── main.rs
├── Cargo.toml
├── Dockerfile
├── docker-compose.yml
└── README.md
```

## Getting Started

1. Clone the repository:
```
git clone <repository-url>
cd rust-crud-api
```

2. Start the application using Docker Compose:
```
docker compose up -d
```

## API Endpoints

### Users

- **POST /users** - Create a new user
  ```
  {
    "name": "John Doe",
    "email": "john@example.com"
  }
  ```

- **GET /users** - Retrieve all users
- **GET /users/{id}** - Retrieve a specific user
- **PUT /users/{id}** - Update a user
- **DELETE /users/{id}** - Delete a user


## Docker Configuration

The project uses two services:
- `rustapp`: The Rust application
- `db`: PostgreSQL database


## Running the Application

There are two ways to run this CRUD application:

### 1. Local Development
1. Install dependencies:
```
cargo build
```

2. Set up PostgreSQL database locally and configure the database URL in `.env`:
```
DATABASE_URL=postgres://postgres:postgres@localhost:5432/postgres
```

3. Run the application:
```
cargo run
```

### 2. Using Docker (Recommended)
1. Ensure Docker and Docker Compose are installed

2. Build and start the containers:
```
docker compose build
docker compose up -d
docker compose up rustapp
```

This will:
- Start the PostgreSQL database container
- Build and run the Rust application container
- Set up networking between containers
- Configure environment variables automatically

The application will be accessible at `localhost:8080` in both cases.

# Was Trying to learn something new on the go!


