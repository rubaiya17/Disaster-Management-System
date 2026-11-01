# Disaster Management System 

**A Web-Based Disaster Reporting, Relief Coordination & Resource Management Platform**

## Overview

Disaster Management System (DMS) is a web-based application developed to facilitate disaster reporting, emergency assistance requests, volunteer coordination, and relief resource management through a centralized platform.

The system provides separate interfaces and functionalities for three types of users: **Admin, Victim, and Volunteer**. It aims to organize disaster-related information and simplify coordination between affected individuals and relief management authorities.

The application is developed using PHP and MySQL, following a modular, database-driven approach.

## Core Modules & Functionalities

### 1. Admin Module
- Manage registered users and system information.
- Review and manage disaster reports.
- Monitor emergency resource requests.
- Manage available relief resources.
- Coordinate volunteers and delivery operations.
- Oversee relief management activities.

### 2. Victim Module
- User registration and authentication.
- Submit disaster reports with relevant information.
- Request emergency resources.
- Provide affected location and resource requirements.
- Monitor request-related updates.

### 3. Volunteer Module
- Volunteer registration and authentication.
- Manage volunteer profile information.
- Maintain availability status.
- Participate in relief activities.
- Handle assigned delivery operations.

## Technology Stack

| Layer | Technologies |
|---|---|
| Frontend | HTML5, CSS3, JavaScript |
| Backend | PHP |
| Database | MySQL |
| Database Connectivity | MySQLi |
| Icons | Font Awesome |
| Local Environment | XAMPP, Apache, phpMyAdmin |

## System Architecture

The application follows a client-server architecture with a PHP-based application layer and a relational database.

```text
                  CLIENT
                    |
                    v
           Web Browser / UI
          (HTML, CSS, JavaScript)
                    |
                    v
             Apache Server
                    |
                    v
              PHP Backend
                    |
          +---------+---------+
          |         |         |
          v         v         v
        Admin     Victim   Volunteer
        Module    Module    Module
          |         |         |
          +---------+---------+
                    |
                    v
             MySQL Database
                    |
                    v
          Query Processing & Data
                 Retrieval
                    |
                    v
            Application Response
                    |
                    v
               User Interface
```

## Application Workflow

The general application flow is organized as follows:

```text
Application Entry Point
        |
        v
    User Access
        |
        v
 Registration / Login
        |
        v
 Authentication
        |
        v
 Role Identification
        |
        +-----------------------+
        |           |           |
        v           v           v
      Admin       Victim     Volunteer
        |           |           |
        v           v           v
   Management   Disaster     Volunteer
   Operations   Reporting    Operations
        |           |           |
        |           v           |
        |     Resource Request  |
        |           |           |
        +-----------+-----------+
                    |
                    v
             Database Operations
                    |
                    v
            Response / Status Update
                    |
                    v
                 Dashboard
```

## Database Design

The project uses a MySQL database named `disaster`.

The database contains entities responsible for user management, disaster reporting, resource handling, and relief delivery.

| Table | Purpose |
|---|---|
| `users` | Stores user account information and roles |
| `admin` | Administrator-related information |
| `victim` | Victim-specific information |
| `volunteer` | Volunteer information and availability |
| `disaster_report` | Disaster incident records |
| `resource` | Relief resource inventory |
| `request` | Emergency assistance requests |
| `resource_request` | Resource request records |
| `delivery` | Relief delivery information |

**Database source:** `disaster.sql`

## Project Structure

```text
Disaster-Management-System/
│
├── admin/             # Administrator functionalities
├── config/            # Database configuration
├── css/               # Stylesheets
├── includes/          # Shared PHP components
├── js/                # Client-side scripts
├── victim/            # Victim functionalities
├── volunteer/         # Volunteer functionalities
│
├── disaster.sql       # Database schema and sample data
├── index.php          # Application entry point
├── login.php          # Authentication
├── register.php       # User registration
├── logout.php         # Session termination
└── README.md
```

## Installation & Setup

### Prerequisites

- PHP 8.0 or later
- MySQL / MariaDB
- Apache Web Server
- XAMPP
- Modern web browser

### 1. Clone the Repository

```bash
git clone https://github.com/rubaiya17/Disaster-Management-System.git
```

### 2. Configure the Local Environment

Move the project directory into the XAMPP `htdocs` folder.

Start **Apache** and **MySQL** from the XAMPP Control Panel.

### 3. Create and Import Database

1. Open `http://localhost/phpmyadmin`.
2. Create a database named `disaster`.
3. Select the database.
4. Import the `disaster.sql` file.

### 4. Configure Database Connection

Update the database credentials in:

```text
config/database.php
```

Configure the hostname, username, password, and database name according to your local environment.

### 5. Run the Application

Open the following URL in your browser:

```text
http://localhost/Disaster-Management-System/
```

## Security Considerations

The application includes basic authentication and account-management mechanisms. For production deployment, the following security measures should also be enforced:

- Prepared SQL statements.
- Server-side input validation.
- Secure session management.
- Role-based authorization checks.
- CSRF protection.
- Secure error handling.

## Future Enhancements

- Real-time disaster alerts and notifications.
- Interactive map-based disaster visualization.
- SMS and email notification integration.
- Advanced resource allocation and tracking.
- Improved reporting and analytical dashboards.
- Enhanced security and mobile responsiveness.

## Repository

**Source Code:** https://github.com/rubaiya17/Disaster-Management-System

---

*Developed as an academic project to implement practical concepts of web application development, relational database management, and software engineering in the context of disaster relief coordination.*
