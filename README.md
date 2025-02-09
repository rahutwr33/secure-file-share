# Secure file share

system requirements:

- docker

## Description

This is a simple project that uses React for the frontend and FastAPI for the backend. It is containerized using Docker.

## Installation

1. Clone the repository

```bash
git clone https://github.com/rahutwr33/secure-file-share.git
```

To run the project, navigate to the root directory and run the following command:

```bash
cd react-fastapi-docker

Set admin credentials in server/.env file for admin user


# Admin Email: abc@yopmail.com
# Admin Password: Admin@123!


docker-compose up --build
```

to access the frontend, navigate to `http://localhost:3000`

Functionality covered:

# https added in server side

Authentication:

- Secure http only cookie
- User can signup and login with email and password and 2 factor authentication uisng email
- User can logout
- admin can login with email and password with 2 factor authentication using email

User Role:

- User can upload file securely
- User can download file file securely
- User can view list of files
- User can share file with other users with expiry date

Admin Role:

- Admin can view all users
- Admin can view all files
- Admin can delete any file
- Admin can delete any file

Share File:

- User can shared files with other users and that user will get link in the email. the link have expiry date
- User can download or view shared files if permission is granted

Security Practice

- MFA using email
- http only cookie authentication
- Rate limiting
- Https url backend
- 2 layer encryption when upload file
- block user for 15 minute attempt if login attempt too much ex 100 time

Test Case

- admin can login with email and password with 2 factor authentication using email
- admin can view all users
- admin can view all files
- admin can delete any file
- admin can delete any file

# Unit Test 
Backend Coverage 73%
