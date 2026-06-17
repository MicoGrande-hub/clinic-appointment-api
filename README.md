# Clinic Appointment API
    Document No. LabEx-CS-IT-IT_2344-03
    Eff. Date 18-MAY-2025
    Revision No. 00 Pages 10 of 13
    Building a Clinic Appointment API
    This project is a simple Clinic Appointment API built using FastAPI and Docker.
## Laboratory Context
    This project was developed in an offline Windows 11 laboratory environment.
    Python was not installed directly on the computer. The application was executed using Docker and
    prebuilt Docker image named clinic-fastapi-base:1.0.
## Features
    Create clinic appointments
    - View all appointments
    View one appointment
    Update appointment details
    - Cancel appointments
## Technologies Used
    - Python
    FastAPІ
    Docker
    Git
## How to Run
    docker compose up --build
    
    Open http://localhost:8000/docs.
## Authentication
    This API uses Bearer Token authentication to protect appointment-related endpoints.
    
### Test Account
    Username: admin
    Password: clinic123
    
### Login Endpoint
    POST /login
    
    Example Request:
    {
        "username": "admin",
        "password": "clinic123"
    }
    
    Example Response:
    {
        "access_token": "clinic-secret-token",
        "token_type": "bearer"
    }

### Protected Endpoints
    GET /me
    GET /appointments
    GET /appointments/{appointment_id}
    POST /appointments
    PUT /appointments/{appointment_id}
    DELETE /appointments/{appointment_id}

    To access protected endpoints, include the bearer token in the Authorization header.

### Educational Limitation
    This authentication implementation is for educational purposes only.
    It uses a fixed username, password, and token stored directly in the source code.
    A production system should use secure password hashing, database-backed users,
    token expiration, HTTPS, role-based access control, and secure authentication
    methods such as JWT.