# AWS-hosted Virtual Classroom and Learning Platform

## Project Overview

The AWS-hosted Virtual Classroom and Learning Platform is a cloud-based educational web application developed using Flask and AWS cloud services. The project demonstrates how cloud computing and web technologies can be integrated to create a scalable, secure, and flexible online learning environment.

The application allows users to register, log in, upload course materials, and access learning content stored on AWS cloud infrastructure.

This project was developed as part of the Cloud Practitioner program under Smart-Internz.

---

## Features

* User Registration and Login Authentication
* Secure Password Hashing
* Cloud File Storage using AWS S3
* User Data Management using AWS RDS (MySQL)
* Flask-based Backend
* Responsive Frontend UI
* Session Management and Logout Functionality
* File Upload Validation
* Cloud Deployment using AWS EC2
* GitHub Version Control Integration

---

## Technologies Used

### Frontend

* HTML
* CSS
* JavaScript
* Bootstrap

### Backend

* Python
* Flask

### Database

* MySQL
* AWS RDS

### Cloud Services

* AWS EC2
* AWS S3
* AWS IAM

### Libraries

* boto3
* pymysql
* werkzeug

### Version Control

* Git
* GitHub

---

## AWS Services Used

### Amazon EC2

Used for deploying and hosting the Flask application.

### Amazon S3

Used for storing uploaded course materials such as PDFs and images.

### Amazon RDS (MySQL)

Used for storing user credentials and application-related data.

### AWS IAM

Used for managing secure access permissions and policies.

---

## Project Architecture

```text
User
   ↓
Flask Web Application
   ↓
AWS EC2 Instance
   ↓
--------------------------------
|                              |
AWS RDS                    AWS S3
(MySQL Database)          (Cloud Storage)
```

---

## Project Structure

```text
project/
│
├── app.py
├── templates/
│   ├── home.html
│   ├── register.html
│   ├── login.html
│   └── content.html
│
├── static/
│
├── requirements.txt
│
└── README.md
```

---

## Application Workflow

1. User registers on the platform.
2. Password is encrypted using hashing.
3. User logs into the system.
4. Flask validates credentials using MySQL database.
5. User uploads files through the web interface.
6. Flask uploads files to AWS S3 using boto3.
7. Uploaded files are stored securely in the S3 bucket.
8. Application fetches and displays uploaded files dynamically.

---

## Setup Instructions

### 1. Clone Repository

```bash
git clone https://github.com/36bhaskar2004/Aws-hosted-virtual-classroom-and-learning-platform.git
```

### 2. Move to Project Directory

```bash
cd Aws-hosted-virtual-classroom-and-learning-platform
```

### 3. Install Required Packages

```bash
pip install -r requirements.txt
```

### 4. Configure AWS Credentials

```bash
aws configure
```

Provide:

* AWS Access Key
* AWS Secret Key
* Region Name

---

## Database Setup

Create a MySQL database in AWS RDS and create the users table:

```sql
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(255) UNIQUE NOT NULL,
    password VARCHAR(255) NOT NULL
);
```

---

## S3 Bucket Setup

Create an S3 bucket with the same name used in the application:

```python
S3_BUCKET = 'aws-project-virtualclassroom'
```

Allowed upload types:

* PDF
* JPG/JPEG
* PNG

---

## Run the Application

```bash
python app.py
```

The application will run on:

```text
http://127.0.0.1:5000
```

---

## Security Features

* Password Hashing
* Session Timeout Management
* File Type Validation
* File Size Restriction
* Secure AWS IAM Access

---

## User Scenarios

### Student Registration and Login

Users can register and securely log into the platform.

### Admin Upload of Course Materials

Admins can upload PDFs and images to AWS S3.

### Accessing Course Materials

Users can access uploaded content dynamically from cloud storage.

---

## Challenges Faced

* AWS IAM policy configuration
* Flask and AWS integration
* Managing AWS credentials securely
* EC2 deployment setup
* RDS connection configuration

---

## Future Enhancements

* Video Lecture Upload Support
* Role-based Authentication
* Course Management Dashboard
* Live Classroom Integration
* AI-based Learning Recommendations
* Notification System
* File Download Analytics

---

## Screenshots

* Landing Page
* Registration Page
* Login Page
* Course Materials Page

---

## Demo Video

Demo Link:
https://drive.google.com/file/d/1Ype_dllwboTtSh1pTE5Ax1EfnfqIRZfx/view

---

## GitHub Repository

GitHub Link:
https://github.com/36bhaskar2004/Aws-hosted-virtual-classroom-and-learning-platform.git

---

## Author

Bhaskar Jaysing Paymal

D Y Patil Agriculture and Technical University, Talsande

---

## Conclusion

This project demonstrates the integration of cloud computing and web application development using AWS services and Flask. The platform provides secure authentication, cloud storage, scalable deployment, and an effective virtual learning environment.
