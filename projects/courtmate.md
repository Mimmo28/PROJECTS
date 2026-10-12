# 🚀 CourtMate — Sports Centre Management System
> **Architecture:** Three-Tier Desktop Architecture | **Tech Stack:** Java, JavaFX, MySQL, JDBC, UML | **Status:** Completed (Academic / University of Palermo)

## 📋 Project Overview
**CourtMate** is an enterprise-grade desktop management application designed for sports centres, clubs, and athletic facilities. It automates user administration, real-time court bookings, membership tracking, and tournament scheduling. The project followed rigorous software engineering standards, including formal requirements engineering (RAD), system architecture design (SDD), and object design (ODD).

---

## 🏗️ Architectural Decisions

### 1. Three-Tier Modular Architecture
The application strictly enforces separation of concerns:
- **Presentation Tier (JavaFX):** Responsive graphical user interface built with modular FXML layouts, custom CSS stylesheets, and reactive event handlers.
- **Application Logic Tier (Java):** Enforces business rules, reservation conflict resolution, tournament bracket generation, and access control validation.
- **Data Tier (MySQL via JDBC):** Relational database storing customer profiles, court availability slots, transaction logs, and tournament fixtures.

### 2. Design Patterns & Engineering Principles
- **Data Access Object (DAO) Pattern:** Decouples persistence operations from domain entities, enabling clean testability and seamless database maintenance.
- **Model-View-Controller (MVC):** Decouples UI states from business logic, preventing concurrency anomalies during booking state transitions.
- **Singleton Pattern:** Used for secure database connection pooling and configuration management.

---

## 🛡️ Security & Reliability Implementation

*   **SQL Injection Prevention:** 100% of database queries are executed using parameterized `PreparedStatement` interfaces.
*   **Role-Based Access Control (RBAC):** Distinct permission levels separating system administrators, facility staff, and club members.
*   **Transaction Integrity & Concurrency:** Employs ACID database transactions and isolation levels to avoid double-booking races across simultaneous user sessions.
*   **Input Validation & Data Sanitization:** Client-side and domain-level boundary checks on all user inputs (dates, time-slots, member IDs).

---

## 🛠️ Software Engineering Documentation
Developed with formal software life-cycle artifacts:
- **Requirements Analysis Document (RAD):** Use cases, actor definitions, functional/non-functional requirements.
- **System Design Document (SDD):** Subsystem decomposition, hardware/software mapping, architectural topology.
- **Object Design Document (ODD):** Detailed UML class diagrams, sequence diagrams, and database schema normalizations (3NF).

---

> **Developer:** Domenico Filippo Innamorato  
> **Team Project:** University of Palermo
