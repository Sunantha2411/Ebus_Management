eBus Management System
Overview
The eBus Management System is a web-based application designed to simplify the management of bus transportation services. It offers an admin dashboard for managing bus schedules and driver assignments, a driver dashboard for posting bus information, and a user dashboard for passengers. The project leverages Flask for backend development and Firebase Firestore for real-time database management.

Features
Admin Dashboard: Manage users, view bus information, and oversee operations.
Driver Dashboard: Post bus information such as bus number, type, and contact details.
User Dashboard: View and manage personal account details.
Authentication: User registration and login functionalities with role-based access (admin, driver, user).
Real-time Database: Store and retrieve data in Firestore.
Session Management: Handle user sessions to manage roles and actions.
Error Logging: Logs errors and user activities for tracking purposes.
Technologies Used
Flask: Python web framework for the backend.
Firebase:
Firestore for real-time database management.
Firebase Authentication for user registration and login.
HTML/CSS: For rendering frontend templates.
Logging: Used to track system errors and user activities.
Installation
Prerequisites
Python 3.x installed.

Flask installed (pip install Flask).

Firebase Admin SDK:

bash
Copy code
pip install firebase-admin
Create a Firebase project and download your serviceAccountKey.json file. Save it as firebase_admin_config.json in your project directory.

Steps
Clone the repository:

bash
Copy code
git clone https://github.com/your-username/eBus-Management-System.git
cd eBus-Management-System
Install dependencies:

bash
Copy code
pip install -r requirements.txt
Replace 'your_secret_key' in app.secret_key with a real secret key for production environments.

Replace 'firebase_admin_config.json' with the path to your Firebase Admin SDK configuration file.

Run the application:

bash
Copy code
python app.py
The application will be accessible at http://127.0.0.1:5001.

Firebase Setup
Set up a Firebase project and Firestore database.
In Firebase Console:
Enable Firestore and create a database.
Set up Firebase Authentication to manage users.
Add the required roles (admin, driver, user) when registering users.
Usage
Registration: New users can register with an email, password, and role (admin, driver, or user).
Login: Users can log in using their credentials. Based on their role, they are redirected to their respective dashboards.
Admin Dashboard: Admins can manage the system, view user data, and monitor buses.
Driver Dashboard: Drivers can post bus information such as bus number, type, and contact details.
User Dashboard: Users can view and manage their account information.
Project Structure
graphql
Copy code
.
├── app.py                  # Main Flask application file
├── templates/              # HTML templates for rendering pages
├── firebase_admin_config.json # Firebase Admin SDK credentials file
├── static/                 # Static files like CSS and JavaScript
├── app.log                 # Log file for error and activity logging
└── README.md               # Project readme file
License
This project is licensed under the MIT License. See the LICENSE file for more details.

This README.md should give clear instructions on how to set up, run, and contribute to the project. Let me know if you need any other modifications!
