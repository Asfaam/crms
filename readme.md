# CRMS – Campus Resource Management System

## Overview
The **Campus Resource Management System (CRMS)** is a web-based application designed to manage **institutional resource booking workflows** within a university or campus environment. The system provides a centralized platform for **students** to request shared resources and for **resource managers** to review, approve, or reject those requests efficiently.

CRMS focuses specifically on **resource allocation, approval workflows, and automated notifications**, eliminating the need for manual emails, paper forms, or informal communication channels.

---

## Problem Statement
In many campus environments, shared resources (such as rooms, equipment, or facilities) are managed manually through emails, spreadsheets, or verbal approvals. This often results in:

- Lost or untracked booking requests
- Delayed approval decisions
- Lack of transparency for students
- No centralized record of approved or rejected bookings

CRMS solves these issues by introducing a **structured, role-based digital system** for managing campus resources.

---

## Key Features

### 1. Role-Based User Access
CRMS implements strict role-based access control to ensure that users only interact with features relevant to their responsibilities.

- **Students**
  - Submit resource booking requests
  - View booking status (Pending, Approved, Rejected)
  - Receive email notifications on request decisions

- **Resource Managers**
  - View all incoming booking requests
  - Approve or reject requests
  - Trigger automated email responses

- **Administrators** (optional extension)
  - Manage system users
  - Configure system settings

---

### 2. Resource Booking Workflow
- Students submit booking requests with required details
- Requests are stored in the database with a default `Pending` status
- Resource managers review requests from a dedicated dashboard
- Each request can be approved or rejected with a single action

---

### 3. Approval & Rejection Handling
- Approved or rejected requests update instantly in the system
- Decision status is persisted for audit and tracking purposes
- Managers can optionally include remarks or reasons

---

### 4. Automated Email Notifications
- Email notifications are sent automatically upon request approval or rejection
- Emails use a **No Reply** sender identity
- Email content is dynamically generated (student name, resource name, decision status)

---

## System Architecture

CRMS follows a **modular PHP-based architecture**:

- **Frontend**
  - HTML
  - CSS / Tailwind CSS
  - JavaScript

- **Backend**
  - PHP
  - Modular function-based structure

- **Database**
  - MySQL
  - Relational schema for users, resources, and bookings

---

## Project Structure

```
crms/
│
├── student/              # Student booking views and logic
├── resource_manager/     # Approval dashboards and actions
│
├── includes/             # Shared backend logic (DB connection, helpers)
├── layout/               # Reusable UI components (header, sidebar)
├── logs/                 # PHP and system error logs
│
├── assets/               # CSS, JS, images
├── config/               # Configuration and environment files
├── .htaccess             # Server-level configuration
├── index.php             # Application entry point
└── README.md             # Project documentation
```

---

## Database Design

The database is centered around the following core entities:

- Users
- Roles
- Resources
- Booking Requests
- Booking Status History

Each booking request maintains a lifecycle from submission to final decision.

---

## Security Considerations

- Session-based authentication
- Role-based authorization
- Server-side validation of user input
- Restricted access to approval endpoints
- Centralized error logging

---

## Installation & Setup

1. Clone or download the project repository
2. Place the project folder inside your web server root (e.g., `htdocs`)
3. Create a MySQL database and import the provided SQL schema
4. Configure database credentials in the config directory
5. Ensure the `/logs` directory is writable
6. Start Apache and MySQL services
7. Access the system through your browser

---

## Future Enhancements

- Resource availability calendar
- File uploads for booking justification
- Multi-level approval workflows
- REST API for mobile integration
- Advanced reporting and analytics

---

## Academic Context

CRMS was developed as a **computer science academic project**, with emphasis on:

- Backend system design
- Secure role-based workflows
- Real-world campus resource management
- Maintainable and scalable code structure

---

## Author

**CRMS Project Developer**  
Computer Science Student

---

## License

This project is intended strictly for academic and educational purposes.

