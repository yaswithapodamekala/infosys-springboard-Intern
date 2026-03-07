# infosys-springboard-Intern
Milestone 1 – Secure User Authentication System

# Project Title
TextMorph – Advanced Text Summarization and Paraphrasing

# Internship
Infosys Springboard Virtual Internship 6.0 – Batch 13

# Milestone
Milestone 1 – Secure User Authentication System

#Project Overview

In Milestone 1 of the TextMorph project, we designed and implemented a secure User Authentication System that serves as the foundation for future NLP modules such as Text Summarization and Paraphrasing.
This system ensures secure user registration, login, session management using JWT (JSON Web Tokens), and password recovery functionality.

#Objective of Milestone 1
The main objective was to:
- Build a secure Signup & Login system
- Implement JWT-based authentication
- Securely store user credentials in a database
- Implement Forgot Password functionality
- Deploy the application using Ngrok for public access

# Technologies Used

- **Streamlit** – Frontend UI development
- **Python** – Backend logic
- **SQLite Database** – Secure data storage
- **bcrypt** – Password hashing
- **JWT (HS256 Algorithm)** – Token-based authentication
- **Ngrok** – Public URL exposure
- **Google Colab** – Development environment

#Features Implemented
 User Signup Page
- Username field
- Email validation (proper email format)
- Alphanumeric password validation
- Confirm password matching
- Security question dropdown
- Security answer validation
- All fields mandatory
- Password securely hashed using bcrypt

#JWT-Based Authentication
- Token generated after successful login
- HS256 algorithm used for signing
- Token expiration time set
- Secure session handling using Streamlit session_state

# Email & Password verification
- Password comparison using bcrypt
- JWT token generation upon successful login
- Redirect to Dashboard

#Dashboard Page
- Displays logged-in username
- Confirms successful authentication
- Logout functionality
- Foundation for future NLP modules

# Forgot Password Flow
1. User enters registered Email
2. System verifies existence
3. Displays stored security question
4. Validates security answer
5. Allows password reset
6. Updates hashed password in database

#Database Structure

SQLite database (`users.db`) contains:

| Field Name        | Description |
|------------------|-------------|
| username         | User name |
| email            | Primary key |
| password         | Hashed password |
| security_question| Selected question |
| security_answer  | Answer for recovery |

Passwords are stored in encrypted format using bcrypt hashing.

# JWT Implementation Details

- Algorithm Used: **HS256**
- Token contains:
  - Username
  - Email
  - Expiration time
- Token is generated during login
- Token is validated for protected dashboard access


# Ngrok Deployment

The Streamlit app was deployed using Ngrok to generate a public URL.

Steps:
1. Install ngrok
2. Add auth token
3. Run Streamlit app
4. Expose port 8501 using ngrok
5. Generate public URL for demo
 Note: Ngrok auth token removed before GitHub upload.


# How to Run the Application
 Step 1: Install Dependencies
```bash
pip install streamlit bcrypt pyjwt pyngrok
Step 2: Run the Application
streamlit run app.py
Step 3: Expose using Ngrok (if needed)
from pyngrok import ngrok
public_url = ngrok.connect(8501)
print(public_url)

 Security Measures Implemented
•	Password hashing using bcrypt
•	JWT token expiration
•	Email format validation
•	Password strength validation
•	Session-based authentication
•	Protected dashboard access

 Future Scope (Next Milestones)
In upcoming milestones, this authentication system will integrate:
•	Text Summarization Engine
•	Text Paraphrasing Module
•	Model Evaluation
•	Deployment of NLP APIs

 Author
Yashwitha Podamekala
Infosys Springboard Intern – Batch 13


Conclusion
Milestone 1 successfully implements a secure and scalable authentication system using industry-standard practices. This lays the groundwork for integrating advanced NLP capabilities in the TextMorph project.

