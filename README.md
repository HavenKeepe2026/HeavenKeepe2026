# HavenKeep

### An Integrated Management and GIS-Based Plot Reservation System for Queen Mary Haven of Peace Memorial Garden

> **Formerly known as QMMemoria**

![Status](https://img.shields.io/badge/Status-In%20Development-yellow)
![Project Type](https://img.shields.io/badge/Project-Capstone%20Project-blue)
![Platform](https://img.shields.io/badge/Platform-Web--Based-green)
![GIS](https://img.shields.io/badge/GIS-Enabled-orange)

---

## 📌 About the Project

**HavenKeep** is a web-based management and GIS-based plot reservation system developed for **Queen Mary Haven of Peace Memorial Garden**.

The system was formerly known as **QMMemoria** and was developed as a capstone project for the **Bachelor of Science in Information Technology** program at **Palawan State University – Quezon Campus**.

HavenKeep is designed to provide a centralized platform for managing memorial garden records, burial plots, reservations, client information, grave records, payments, and administrative activities.

The system incorporates **Geographic Information System (GIS)** functionality to provide a visual representation of burial plots and their locations within the memorial garden.

---

## 🎯 Project Objectives

### General Objective

To develop and implement an integrated management and GIS-based plot reservation system that enhances operational efficiency, improves client services, and supports accurate spatial management of burial plots at Queen Mary Haven of Peace Memorial Garden.

### Specific Objectives

HavenKeep aims to:

* Develop a centralized system for managing client information, plot records, and reservation transactions.
* Implement a GIS-based interface for the spatial representation of burial plots.
* Provide accurate identification of plots using block and plot numbers.
* Support the management of plot reservations.
* Manage client and burial records.
* Track payment information and remaining balances.
* Support grave and burial record management.
* Implement role-based access for authorized users.
* Generate reports related to plots, reservations, payments, and other records.
* Improve the organization, accessibility, and management of memorial garden information.

---

## 🗺️ GIS-Based Plot Management

A major component of HavenKeep is its GIS-based plot management functionality.

The system is designed to represent the actual location of burial plots within the memorial garden.

GIS functionality includes:

* Block identification
* Plot identification
* Geographic coordinates
* Plot boundaries
* Plot availability
* Plot reservation status
* Plot occupancy status
* Grave location tracking
* Visual plot positioning

### Example Plot Structure

```text
Block 36
├── Plot 1
├── Plot 2
├── Plot 3
├── Plot 4
└── Plot 5
```

Each plot may contain spatial information corresponding to its actual location within the memorial garden.

Sensitive client and deceased-person information should not be publicly displayed directly on the GIS map.

---

## 👥 User Roles

HavenKeep uses role-based access to separate administrative functions from staff and client-related functions.

### Administrator

The Administrator manages the overall system and has access to authorized administrative functions such as:

* Staff account management
* Client account management
* Plot management
* GIS management
* Reservation management
* Reservation approval
* Payment management
* Grave record management
* Report generation
* Record restoration
* System settings
* Administrative records

### Staff

Staff assists with the day-to-day operations of the memorial garden.

Staff functions include:

* Creating client accounts upon request
* Recording client information
* Assisting walk-in clients
* Processing reservation requests
* Submitting reservations for administrator approval
* Recording payments
* Managing permitted grave information
* Viewing plot information
* Assisting clients with plot selection
* Accessing applicable reports

### Client

Clients have limited access to the system and may access functions related to their own records and reservations.

Possible client functions include:

* Accessing a verified account
* Viewing available plot information
* Requesting a plot reservation
* Viewing reservation information
* Viewing payment status
* Viewing remaining balance
* Accessing client service information
* Viewing frequently asked questions

---

## 🔐 Authentication and Account Security

HavenKeep incorporates authentication and controlled account access.

The revised system design includes:

* Staff-controlled client account creation
* Email verification
* Account authentication
* Password protection
* Role-based access
* Reservation authentication
* Terms and agreement confirmation
* Controlled access to sensitive records
* Administrative approval for applicable transactions

A client account may be created by authorized staff upon request.

Email verification is required for applicable reservation transactions to help ensure that the registered email belongs to the client.

---

## 📋 Plot Reservation

The plot reservation process is designed to connect the client's information with the selected plot.

A general reservation process includes:

```text
Client Request
      ↓
Staff Assistance
      ↓
Client Account Creation
      ↓
Email Verification
      ↓
GIS Map
      ↓
Plot Selection
      ↓
Reservation Requirements
      ↓
Client Information
      ↓
Payment Information
      ↓
Terms & Agreement
      ↓
Reservation Request
      ↓
Administrator Review
      ↓
Approval / Rejection
```

The system is designed so that sensitive client information is handled separately from the publicly visible plot map.

---

## 💰 Payment Management

HavenKeep supports payment recording and monitoring.

Payment options may include:

* Cash
* Installment

For installment arrangements, the system may record:

* Total amount
* Amount paid
* Remaining balance
* Payment date
* Payment schedule
* Expected end date
* Payment status

### Payment Status Example

```text
Total Amount:       ₱50,000
Amount Paid:        ₱30,000
Remaining Balance:  ₱20,000
Payment Status:     Remaining Balance
```

Once the complete amount has been recorded:

```text
Payment Status: Fully Paid
```

This allows authorized users to monitor the financial status associated with a reservation or plot record.

---

## 🪦 Grave and Burial Record Management

HavenKeep includes functionality for managing grave and burial information associated with designated plots.

Records may include:

* Block number
* Plot number
* Deceased information
* Burial information
* Burial date
* Client/account information
* Plot status

Access to sensitive information is controlled through user roles.

---

## 📊 Reports

The system provides reporting functionality for authorized users.

Possible reports include:

* Plot availability reports
* Reservation reports
* Payment reports
* Client reports
* Grave records
* Weekly reports
* Quarterly reports
* Outstanding balance reports

Reports may be prepared for viewing and printing.

---

## 🗑️ Record Management

HavenKeep is designed to support a trash/archive approach for deleted records instead of immediately permanently removing them.

### Record Workflow

```text
Active Record
      ↓
Delete / Hide
      ↓
Trash
      ↓
Restore
      ↓
Active Record
```

Authorized administrators may restore records when necessary.

---

## ❓ Frequently Asked Questions

The system includes a **Frequently Asked Questions (FAQ)** section intended to provide clients with information about common services and procedures.

Possible FAQ topics include:

* Plot reservation
* Reservation requirements
* Email verification
* Payment methods
* Installment payments
* Remaining balances
* Plot location
* Account access
* Password management
* Memorial garden services

---

## 🏗️ System Architecture

HavenKeep follows a web-based system architecture consisting of the user interface, application logic, database, and GIS components.

```text
                     ┌─────────────────────┐
                     │       CLIENT        │
                     └──────────┬──────────┘
                                │
                     ┌──────────▼──────────┐
                     │     WEB SYSTEM      │
                     └──────────┬──────────┘
                                │
              ┌─────────────────┼─────────────────┐
              │                 │                 │
       ┌──────▼──────┐   ┌──────▼──────┐   ┌──────▼──────┐
       │   ADMIN     │   │    STAFF     │   │     GIS     │
       │ MANAGEMENT  │   │ MANAGEMENT   │   │    MAP      │
       └──────┬──────┘   └──────┬──────┘   └──────┬──────┘
              │                 │                 │
              └─────────────────┼─────────────────┘
                                │
                     ┌──────────▼──────────┐
                     │      DATABASE       │
                     │ Client / Plot /     │
                     │ Reservation /       │
                     │ Payment / Grave     │
                     └─────────────────────┘
```

---

## 🛠️ Technologies

### Web Development

* PHP
* Laravel
* Blade
* HTML
* CSS
* JavaScript

### Database

* MySQL

### GIS / Mapping

* GIS-based mapping
* Geographic coordinates
* Digital plot boundaries
* Map visualization

### Development Tools

* Visual Studio Code
* Git
* GitHub
* XAMPP
* Composer
* Node.js

---

## 📁 Repository Structure

The repository may contain the following project components:

```text
HavenKeep/
│
├── app/
├── bootstrap/
├── config/
├── database/
│   ├── migrations/
│   ├── seeders/
│   └── factories/
│
├── public/
├── resources/
│   ├── css/
│   ├── js/
│   └── views/
│
├── routes/
├── storage/
├── tests/
│
├── documentation/
├── gis/
├── screenshots/
│
├── .env.example
├── .gitignore
├── composer.json
├── package.json
└── README.md
```

---

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/HavenKeepe2026/HavenKeep.git
```

### 2. Open the Project

```bash
cd HavenKeep
```

### 3. Install PHP Dependencies

```bash
composer install
```

### 4. Install Frontend Dependencies

```bash
npm install
```

### 5. Create the Environment File

Windows:

```bash
copy .env.example .env
```

### 6. Generate the Application Key

```bash
php artisan key:generate
```

### 7. Configure the Database

Create a MySQL database and configure the `.env` file.

Example:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=havenkeep
DB_USERNAME=root
DB_PASSWORD=
```

### 8. Run Database Migrations

```bash
php artisan migrate
```

If seeders are available:

```bash
php artisan db:seed
```

### 9. Run the Development Server

```bash
php artisan serve
```

The application can then be accessed at:

```text
http://127.0.0.1:8000
```

---

## 🔒 Security and Privacy

The repository should **never contain confidential or sensitive information**.

Do not upload:

* `.env` files
* Database passwords
* API keys
* Email credentials
* Authentication secrets
* Real client information
* Real deceased-person information
* Private payment information
* Other confidential records

Use `.env.example` for configuration examples.

For development, testing, and demonstration purposes, use sample or anonymized data.

---

## 📚 Capstone Documentation

The repository may contain documentation related to the development and evaluation of HavenKeep.

Possible documentation includes:

* Chapter I – Introduction
* Chapter II – Review of Related Literature/Systems
* Chapter III – Technical Background
* Chapter IV – Methodology
* Chapter V – Results and Discussion
* Chapter VI – Conclusions and Recommendations
* System Requirements
* Use Case Diagram
* User Stories
* Data Flow Diagram
* Entity Relationship Diagram
* System Architecture
* GIS Documentation
* Test Results
* User Guide
* Sample Reports
* Screenshots
* Relevant Source Code

---

## 🎓 Academic Project

**HavenKeep** is a capstone project developed in partial fulfillment of the requirements for the degree of:

**Bachelor of Science in Information Technology**

**Palawan State University – Quezon Campus**

**Palawan, Philippines**

---

## 📌 Project Status

**In Development**

HavenKeep is undergoing major system revisions based on adviser and panel feedback.

Current development areas include:

* Authentication and email verification
* Staff-controlled client accounts
* Role-based access
* GIS plot mapping
* Plot coordinates and boundaries
* Plot reservation workflow
* Payment and balance tracking
* Grave tracking
* Administrative approval
* Reports
* Privacy controls
* User interface improvements

---

## 🔄 Project History

### QMMemoria → HavenKeep

The system was originally developed under the name:

**QMMemoria: An Integrated Management and GIS-Based Plot Reservation System for Queen Mary Haven of Peace Memorial Garden**

The project was subsequently renamed:

**HavenKeep**

The core project purpose remains focused on the management, mapping, reservation, and tracking of memorial garden plots.

---

## 📄 License

This project is developed for academic and educational purposes.

Unauthorized commercial use, redistribution, or reproduction of confidential project information is not permitted without authorization from the project owners and concerned institution.
