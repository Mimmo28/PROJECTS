# 🚀 Personal Portfolio & Engineering Showcase
> **Architecture:** Static with Client-side E-commerce | **Tech Stack:** TypeScript, Vanilla CSS, Preact, Nano Stores | **Status:** Production / E-commerce Ready

## 📋 Project Overview
This project is a high-performance showcase of the **Rocca Ciniè** digital ecosystem, representing a biological farm in the heart of Sicily. Transformed into a modern **E-commerce platform**, it utilizes a **Static Site Generation (SSG)** architecture with Astro to ensure lightning-fast load times, while handling dynamic shopping cart logic via client-side state management. The platform supports native trilingual support (IT/EN/ES) and features a premium UI/UX, serving as a primary example of building scalable, secure, and SEO-optimized web applications.

---

## 🏗️ Architectural Decisions

### 1. Performance-First E-commerce
I chose an SSG architecture to support the e-commerce features while maintaining a 100/100 performance score. While the site is static, it integrates a sophisticated **persistent shopping cart** and dynamic product configurators that handle complex pricing and format selections without requiring a backend for the browsing experience.

### 2. State Management with Nano Stores
To provide a seamless user experience, I implemented a **persistent shopping cart** using **Nano Stores** and **Preact**. This allows for a reactive UI (Cart Flyout, Icon Badges) that maintains state across page transitions and browser sessions, keeping the bundle size minimal and the experience fluid.

### 3. Native Trilingual Routing (IT/EN/ES)
The multilingual system was expanded to include **Spanish**, with a smart header that handles contextual language switching. This means users can switch from a specific product in Italian directly to its Spanish equivalent without losing their place, maintaining robust routing consistency.

---

## 🛡️ Security-by-Design Implementation
The project follows modern security standards to ensure data protection and resilience:

*   **Secure Environment Management:** Sensitive configurations (Stripe keys, Shipping APIs) are managed via **Environment Variables (.env)**, protected from source control.
*   **Authentication & Anti-Spam:** The integrated contact form utilizes a secure validation system with **Honeypot techniques** to prevent automated bot abuse.
*   **Optimized Deployment:** Deployment is automated via **GitHub Actions**, syncing a flat, optimized build structure to cPanel/Netsons via FTP, ensuring zero-downtime updates.

---

## 🛠️ Engineering Challenges & Solutions

*   **Challenge:** Integrating a reactive e-commerce state in a static Astro environment.
    *   **Solution:** Leveraged **Nano Stores** for lightweight, framework-agnostic state management, allowing Preact components to synchronize state across the entire site with zero performance penalty.
*   **Challenge:** Enabling direct orders for seasonal products without a full database.
    *   **Solution:** Implemented context-aware "Order Now" CTAs that pre-fill contact forms or WhatsApp messages, bridging the gap between a catalog and a full transactional system.

---

## 📈 Performance Results
*   **Lighthouse Performance:** 100/100 ✅
*   **First Contentful Paint:** < 0.5s ⚡
*   **State Persistence:** Persistent Cart via LocalStorage 🛒

---

> **Developer:** Domenico Filippo Innamorato  
> **Art Name:** The Dev Heart  
> **Live Site:** [https://www.roccacinie.it](https://www.roccacinie.it)
