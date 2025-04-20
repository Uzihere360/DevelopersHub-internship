# Cybersecurity Internship Project - Strengthening Security Measures for a Web Application

## 📌 Overview

This project was completed as part of a cybersecurity internship program.  
The objective was to identify vulnerabilities in a web application, fix them, and implement core security measures.

The mock web application used for testing is **OWASP Juice Shop**.

---

## 🛡️ Tasks Completed

### Week 1: Security Assessment
- Set up OWASP Juice Shop locally.
- Performed vulnerability assessment using:
  - OWASP ZAP
  - Browser Developer Tools (manual XSS tests)
  - Basic SQL Injection attempts
- **Findings:**
  - Input fields vulnerable to XSS.
  - Weak password storage using outdated hashing.
  - SQL Injection possibilities in login.
  - Lack of secure HTTP headers.

### Week 2: Implementing Security Measures
- **Input Validation:**  
  Used the `validator` library to validate and sanitize email/password fields in `login.ts`.
- **Password Hashing:**  
  Switched from weak hashing to `bcrypt` for secure password comparison.
- **Authentication:**  
  Implemented **JWT-based token authentication** using `jsonwebtoken`.
- **SQL Injection Prevention:**  
  Replaced raw SQL queries with Sequelize ORM queries with parameterized inputs.
- **Helmet.js Integration:**  
  Created a separate secure server setup with `helmet` middleware.
- **Logging with Winston:**  
  Set up `winston` logging to log important application events to console and a file (`security.log`).

### Week 3: Advanced Security and Final Reporting
- **Basic Penetration Testing:**  
  Manual tests using Browser Developer Tools and simulated SQL/XSS attacks after security fixes.
- **Logging:**  
  Winston configured in `Server.ts`.
- **Checklist Created:**  
  - [x] Validate all user inputs.
  - [x] Secure password storage using hashing and salting.
  - [x] Secure HTTP headers using Helmet.
  - [x] Use parameterized queries to prevent SQL Injection.
  - [x] Implement token-based authentication.

---
