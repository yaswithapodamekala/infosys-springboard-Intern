# Milestone 2 – Advanced User Authentication System
# Project Title
# TextMorph – Advanced Text Summarization and Paraphrasing
# Internship
Infosys Springboard Virtual Internship 6.0 – Batch 13
# Milestone
Milestone 2 – Advanced Authentication Security
________________________________________
# Description
In Milestone 2, the authentication system developed in Milestone 1 was enhanced with advanced security mechanisms to make the system more robust and reliable.
This milestone introduces multiple security layers such as:
•	OTP-based email verification
•	Account lock after multiple failed login attempts
•	Secure password reset mechanism
•	Admin login and monitoring dashboard
•	JWT-based authentication for session security
These enhancements ensure that the authentication system follows industry-level security practices used in real-world applications.
# Technologies Used
The following technologies were used to implement this milestone:
•	Python
•	Streamlit – for building the web interface
•	SQLite Database – for storing user data
•	JWT (JSON Web Token) – for secure authentication
•	SMTP (Gmail Server) – for sending OTP verification emails
•	bcrypt – for secure password hashing
•	Ngrok – to expose the local Streamlit application to the internet
# Features Implemented
1. OTP Based Email Verification
During the signup process, the system sends a One-Time Password (OTP) to the user's email address.
Steps:
1.	User enters registration details.
2.	System generates an OTP.
3.	OTP is sent to the registered email.
4.	User must enter the correct OTP to complete signup.
This ensures that the provided email address is valid and owned by the user.

2. Secure Password Storage
Passwords are stored using bcrypt hashing.
Advantages:
•	Passwords are never stored in plain text.
•	Even if the database is compromised, the original password cannot be retrieved.

3. Account Lock Mechanism
To prevent brute-force login attempts, the system implements an account lock mechanism.
Rules:
•	After 3 incorrect password attempts, the account is locked.
•	The user must wait 5 minutes before attempting to log in again.
This feature significantly improves authentication security.

4. Forgot Password Workflow
If a user forgets their password, they can reset it using a security question verification process.
Process:
1.	User enters their registered email.
2.	System verifies whether the email exists.
3.	Stored security question is displayed.
4.	User must provide the correct answer.
5.	User can then set a new password.
Additional security rule:
•	The system prevents the user from reusing their previous password.

5. Admin Login and Dashboard
An Admin login system was implemented to monitor registered users.
Admin capabilities include:
•	Secure login with admin credentials
•	Viewing all registered users
•	Monitoring authentication activity
The Admin Dashboard displays the list of all registered users in a table format.

6. JWT Based Authentication
JWT (JSON Web Token) is used to secure user sessions.
After successful login:
1.	The system generates a JWT token.
2.	The token is stored in the session state.
3.	Only authenticated users can access protected pages.
JWT ensures secure session management across the application.

# Application Workflow
The authentication workflow follows these steps:
1.	User registers using the Signup Page.
2.	OTP verification confirms the user's email.
3.	User logs in with valid credentials.
4.	Password is verified using bcrypt hashing.
5.	JWT token is generated upon successful login.
6.	User is redirected to the dashboard.
7.	Security features monitor login attempts and password reset requests.

# Pages Implemented
The following pages were developed using Streamlit:
Signup Page
Allows new users to register with OTP verification.
Login Page
Allows existing users to authenticate securely.
Forgot Password Page
Allows users to reset their password using a security question.
User Dashboard
Displays a welcome message after successful login.
Admin Dashboard
Allows admin users to view all registered users.
# How to Run the Application
Follow these steps to run the project.
Step 1 – Install Required Libraries
<img width="890" height="550" alt="image" src="https://github.com/user-attachments/assets/0b1bac6f-ecec-4550-a477-3438a2418084" />
# Conclusion
Milestone 2 significantly enhanced the authentication system by introducing advanced security features such as OTP verification, account locking, password reuse prevention, and admin monitoring.
These improvements strengthen the security foundation of the TextMorph project and prepare the system for the integration of AI-based text summarization and paraphrasing modules in future milestones.


