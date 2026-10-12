# 🚀 Android Application for Railway Services
> **Architecture:** Client-Server Mobile Architecture | **Tech Stack:** Kotlin, XML, Android Studio, Python, Flask | **Status:** Completed (Academic / University of Palermo, Team Project)

## 📋 Project Overview
A native mobile application developed in **Kotlin** designed to support railway operations and commuter services. Built collaboratively as a university team project at the **University of Palermo**, the system features a dedicated lightweight backend developed in **Python / Flask** adhering to a RESTful client-server paradigm.

---

## 🏗️ Architectural Decisions

### 1. Client-Server Decoupling
- **Mobile Client (Android):** Built natively with Kotlin and XML layouts in Android Studio. Implements asynchronous networking and robust lifecycle management to ensure fluid UX during dynamic train schedule lookups.
- **Backend Service (Python & Flask):** Serves lightweight REST APIs delivering JSON payloads for route information, train statuses, delays, and schedule tracking.

### 2. Networking & Data Serialization
- REST API integration via HTTP client libraries handling serialization/deserialization between JSON and Kotlin data models.
- Graceful error handling for mobile network drops and asynchronous background task dispatching (coroutines / threading).

---

## 🛡️ Security & Reliability Implementation

*   **API Validation:** Server-side request sanitization in Flask to protect against malformed payloads.
*   **Secure Communication:** Enforces HTTPS/TLS communication between Android endpoints and the service backend.
*   **Resilient UX:** Client-side caching and offline state fallbacks when connectivity is intermittent.

---

> **Developer:** Domenico Filippo Innamorato  
> **Team Project:** University of Palermo (BSc Computer Engineering)
