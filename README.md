# Sample flask auth

## Overview

This Flask API provides basic functionality for managing users, including registration, login, reading, updating, and deleting users. Authentication is managed using Flask-Login, and passwords are encrypted with bcrypt.

## Features

- **User Registration**: Create a new user with a username and password. Passwords are securely hashed before storage.
- **User Login**: Authenticate users with their username and password. A successful login establishes a session.
- **User Logout**: End the session of the currently logged-in user.
- **View User Profile**: Retrieve information about a user by their ID, including username.
- **Update User Profile**: Modify user details, including updating passwords (only the user themselves can update their own password).
- **Delete User**: Remove a user from the system. Only administrators can delete users, and users cannot delete their own accounts.

## Requirements

- Python 3.x

## Installation

1. Clone the repository:
   ```bash
   git clone

2. Navigate to the project directory::
   ```bash
   cd sample-flask-auth
   
3. Install Python requirements:
    ```bash
   pip install -r requirements.txt

4. Set up the database using Docker Compose:
    ```bash
   docker-compose up -d

5. Initialize the database schema:
    ```bash
    flask shell
    db.create_all()
    db.session.commit()
    exit()

## Usage

To run the application, execute the following command in your terminal:

  ```bash
  python app.py