# E-Bus Management System

This is a web-based Bus Management System built using Flask and Firebase Firestore for real-time database storage. The system has different user roles, including **admin**, **driver**, and **user**, and allows drivers to post bus information, users to view the information, and admins to manage the system.

## Features
- **User Registration**: Register a new user with an email and password.
- **User Login**: Log in to the system based on user role (admin, driver, user).
- **User Roles**: Depending on the role, users are redirected to respective dashboards.
  - **Admin Dashboard**: Admins can manage the system.
  - **Driver Dashboard**: Drivers can post bus information.
  - **User Dashboard**: Users can view relevant information.
- **Post Bus Info**: Drivers can post bus information like bus number, bus type, and contact details.

## Technology Stack
- **Backend**: Flask (Python)
- **Database**: Firebase Firestore
- **Authentication**: Firebase Authentication
- **Frontend**: HTML, CSS (Flask templates)
- **Logging**: Python's built-in logging module

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/bus-management-system.git
    cd bus-management-system
    ```

2. Set up a virtual environment (optional but recommended):
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # For Linux/macOS
    venv\Scripts\activate  # For Windows
    ```

3. Install required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

4. Set up Firebase:
    - Create a Firebase project at [Firebase Console](https://console.firebase.google.com/).
    - Enable Firebase Authentication and Firestore in the project.
    - Download the `firebase_admin_config.json` service account key file and place it in the root directory of the project.

5. Set a secret key for Flask in the `app.py` file:
    ```python
    app.secret_key = 'your_secret_key'
    ```

6. Run the Flask application:
    ```bash
    python app.py
    ```

7. Access the app in your browser at `http://127.0.0.1:5001`.

## File Structure
```bash
├── app.py                  # Main Flask app
├── templates/
│   ├── index.html           # Home page template
│   ├── admin_dashboard.html # Admin dashboard template
│   ├── driver_dashboard.html# Driver dashboard template
│   ├── user_dashboard.html  # User dashboard template
│   ├── register.html        # User registration page template
│   ├── login.html           # User login page template
│   ├── post_bus_info.html   # Driver post bus information page template
├── firebase_admin_config.json # Firebase service account key (not included in repo)
├── requirements.txt         # Project dependencies
├── README.md                # Project documentation (this file)
└── app.log                  # Log file for application
