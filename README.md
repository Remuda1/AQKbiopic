# AQKbiopic
Soliciting scripts for a biopic about Abdul Qadeer Khan

Script Editor & Biopic Submission Portal
This is a simple, single-page web application that serves as a script editor and a submission portal for a biopic script. The project is designed to be easily hosted as a static website on platforms like GitHub Pages.

The app is built with a minimalist design using Tailwind CSS and pure JavaScript, with Firebase Firestore handling the secure storage of user submissions.

Features
Live Script Editor: A clean, intuitive text area with automatically updating line numbers, perfect for drafting or pasting script content.

User Information Form: Collects the submitter's name, email, and phone number.

Secure Data Storage: User scripts and information are securely saved to a private Firebase Firestore database. Submissions are only accessible by you, the site owner.

Biopic-Specific Instructions: Provides clear guidance for writers on what to include in a script for a biopic about Dr. A. Q. Khan, including thematic considerations and basic screenwriting do's and don'ts.

How It Works
The website is a single index.html file that includes all HTML, CSS, and JavaScript.

Frontend: The user interface is built with standard HTML and styled with the Tailwind CSS framework.

Backend (Database): The application uses Firebase Authentication for anonymous sign-in and Firebase Firestore for a secure, cloud-based database. User submissions are written to a private document associated with their anonymous user ID.

Project Setup
To get this project running, you will need to:

Set up a Firebase Project:

Go to the Firebase Console.

Create a new project.

Enable Firestore Database and Authentication (specifically, the Anonymous sign-in method).

Configure the Code:

The script in script_editor.html uses environment variables for the Firebase configuration and authentication token. These variables (__app_id, __firebase_config, and __initial_auth_token) are typically provided by hosting platforms like Canvas.

For local testing, you will need to manually replace these variables with your Firebase project's credentials.

Deploy:

Upload the script_editor.html file to a static hosting service. GitHub Pages is a great free option for this.

Accessing Submissions
Submissions are saved to your Firebase Firestore database. To view them:

Go to your Firebase project in the Firebase Console.

Navigate to Firestore Database.

The submitted data will be located in the artifacts > [your_app_id] > users > [user_id] collection path.
