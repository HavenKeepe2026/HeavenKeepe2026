# QMMemoria

### An Integrated Management and GIS-Based Plot Reservation System for Queen Mary Haven of Peace Memorial Garden

![Status](https://img.shields.io/badge/Status-In%20Development-yellow)
![Project Type](https://img.shields.io/badge/Project-Capstone%20Project-blue)
![Platform](https://img.shields.io/badge/Platform-Web--Based-green)
![GIS](https://img.shields.io/badge/GIS-Enabled-orange)

---

## 📌 Project Overview

**QMMemoria** is a web-based management and GIS-based plot reservation system developed for **Queen Mary Haven of Peace Memorial Garden**.

The system is designed to help organize and manage memorial garden operations by providing a centralized platform for managing client information, burial plots, reservations, payments, and grave records.

The system integrates **Management Information System (MIS)** functions with **Geographic Information System (GIS)** features to provide a visual representation of burial plots and their corresponding locations.

The project aims to improve record organization, plot monitoring, reservation management, and the overall management of memorial garden information.

---

## 🎯 Project Objectives

### General Objective

To develop and implement an integrated management and GIS-based plot reservation system that enhances operational efficiency, improves client services, and supports accurate spatial management of burial plots at Queen Mary Haven of Peace Memorial Garden.

### Specific Objectives

The project aims to:

* Develop a centralized system for managing client information, plot records, and reservation transactions.
* Implement a GIS-based interface for visualizing burial plots and their locations.
* Provide accurate plot identification using block and plot numbers.
* Support the management of plot reservations and client records.
* Track payment information and remaining balances.
* Support the management and tracking of grave records.
* Provide role-based access for administrators and staff.
* Generate reports related to plots, reservations, payments, and records.
* Improve the organization and accessibility of memorial garden records.

---

## 👥 User Roles

### Administrator

The Administrator is responsible for the overall management of the system.

Main functions include:

* Manage staff accounts
* Manage client accounts
* Manage burial plots
* Manage GIS plot information
* Review reservation requests
* Approve or reject reservations
* Manage payment records
* Manage grave records
* Generate reports
* Restore deleted records
* Manage system settings
* Access administrative records

### Staff

Staff assists with the daily operations of the memorial garden.

Main functions include:

* Create client accounts upon request
* Record client information
* Assist walk-in clients
* Process reservation requests
* Submit reservations for administrator approval
* Record payments
* Manage permitted grave information
* View plot information
* Assist clients with plot selection
* Access applicable reports

### Client

Clients have limited access to the system.

Client functions may include:

* Access their verified account
* View available plot information
* View their reservation information
* Submit plot reservation requests
* View payment status
* View remaining balance
* View relevant plot information
* Access frequently asked questions and client services

---

## 🗺️ GIS Plot Management

QMMemoria incorporates GIS functionality to visually represent the memorial garden's burial plots.

The GIS component is intended to provide:

* Block identification
* Plot identification
* Plot coordinates
* Plot boundaries
* Plot availability
* Plot reservation status
* Plot occupancy status
* Visual plot location
* Grave location tracking

The system is designed to use the actual coordinates and spatial boundaries of the memorial garden plots.

### Plot Structure

Example:

```text
Block 36
├── Plot 1
├── Plot 2
├── Plot 3
├── Plot 4
└── Plot 5
```

Sensitive client and deceased-person information should not be publicly displayed directly on the GIS map.

---

## 🔐 Authentication and Security

The system includes authentication and role-based access control.

Planned security features include:

* Staff-controlled client account creation
* Email verification
* Account authentication
* Password protection
* Role-based access
* Reservation authentication
* Terms and agreement confirmation
* Controlled access to sensitive client information
* Administrative approval for selected transactions

Clients must have a verified email before proceeding with applicable reservation transactions.

---

## 💰 Payment Management

The system supports the recording and monitoring of payment information.

Payment methods may include:

* Cash
* Installment

For installment arrangements, the system may record:

* Total amount
* Amount paid
* Remaining balance
* Payment dates
* Payment schedule
* Expected completion/end date
* Payment status

Example:

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

---

## 🪦 Grave and Burial Record Management

The system supports the management of grave and burial information associated with designated plots.

Possible information includes:

* Plot number
* Block number
* Deceased person's information
* Burial information
* Client/account information
* Burial date
* Plot status

Access to sensitive information is restricted according to user roles.

---

## 📊 Reports

QMMemoria provides reporting functionality for system records.

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

Instead of immediately permanently deleting records, the system may use a **Trash/Archive** mechanism.

Example workflow:

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

The system includes an FAQ/Client Services section intended to provide answers to common questions.

Possible topics include:

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

The project follows a web-based system architecture consisting of the user interface, application logic, database, and GIS components.

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

The project uses web development technologies and database technologies appropriate for the system implementation.

### Development

* PHP
* Laravel
* Blade
* HTML
* CSS
* JavaScript

### Database

* MySQL

### GIS / Mapping

* GIS-based plot mapping
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

```text
QMMemoria/
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
git clone https://github.com/YOUR-USERNAME/qmmemoria.git
```

### 2. Open the Project

```bash
cd qmmemoria
```

### 3. Install PHP Dependencies

```bash
composer install
```

### 4. Install Frontend Dependencies

```bash
npm install
```

### 5. Create Environment File

```bash
cp .env.example .env
```

For Windows:

```bash
copy .env.example .env
```

### 6. Generate Application Key

```bash
php artisan key:generate
```

### 7. Configure Database

Create a MySQL database and configure the `.env` file.

Example:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=qmmemoria
DB_USERNAME=root
DB_PASSWORD=
```

### 8. Run Database Migrations

```bash
php artisan migrate
```

If demo seed data is available:

```bash
php artisan db:seed
```

### 9. Run the Development Server

```bash
php artisan serve
```

The system can then be accessed through:

```text
http://127.0.0.1:8000
```

---

## 🔒 Security Notice

Do **not** upload the following to GitHub:

* `.env`
* Database passwords
* API keys
* Email credentials
* Authentication secrets
* Real client information
* Real deceased-person information
* Private payment information
* Other confidential records

Use `.env.example` for configuration examples.

For demonstrations and development, use **sample or anonymized data**.

---

## 📚 Capstone Documentation

The repository may contain project documentation such as:

```text
documentation/
├── Chapter I/
├── Chapter II/
├── Chapter III/
├── Chapter IV/
├── Chapter V/
└── Chapter VI/
```

Supporting documentation may include:

* Project proposal
* System requirements
* Use Case Diagram
* User Stories
* Data Flow Diagram
* Entity Relationship Diagram
* System Architecture
* GIS documentation
* Test results
* User guide
* Sample reports
* Screenshots
* Relevant source code

---

## 🎓 Academic Project

This project is developed as a **Capstone Project** in partial fulfillment of the requirements for the degree of:

**Bachelor of Science in Information Technology**

**Palawan State University – Quezon Campus**

### Project

**QMMemoria: An Integrated Management and GIS-Based Plot Reservation System for Queen Mary Haven of Peace Memorial Garden**

---

## 👨‍💻 Developers

**BS Information Technology Capstone Project**

Palawan State University
Quezon Campus
Palawan, Philippines

---

## 📌 Project Status

**Currently in Development**

The system is undergoing major revisions based on adviser/panel feedback. Future updates will include improvements to authentication, client account management, GIS plot mapping, reservation workflows, payment tracking, grave tracking, reporting, and role-based system access.

---

## 📄 License

This project is developed for academic purposes.

Unauthorized commercial use, redistribution, or reproduction of the project and its associated confidential data is not permitted without permission from the project owners and the concerned institution.
