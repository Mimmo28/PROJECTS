# 🚀 Personal Portfolio & Engineering Showcase
> **Architecture:** Hybrid SSR | **Tech Stack:** TypeScript, Tailwind CSS, Preact, Nano Stores | **Status:** Production / E-commerce

## 📋 Project Overview
This project is a high-performance showcase of the **Rocca Ciniè** digital ecosystem, representing a biological farm in the heart of Sicily. Transformed into a fully functional **E-commerce**, it utilizes a **Hybrid SSR architecture** with Astro to handle dynamic shopping cart logic and secure checkout flows. The platform supports native trilingual support (IT/EN/ES) and features a premium UI/UX, serving as a primary example of building scalable, secure, and SEO-optimized e-commerce applications.

---

## 🏗️ Architectural Decisions

### 1. Hybrid SSR Evolution
I transitioned the architecture from static to **Hybrid SSR** to support dynamic e-commerce features. While keeping the majority of the site static for extreme performance, critical routes like the **Shopping Cart** and **Checkout** are handled via server-side rendering, enabling real-time logic and future integration with payment gateways like Stripe.

### 2. State Management with Nano Stores
To provide a seamless user experience, I implemented a **persistent shopping cart** using **Nano Stores** and **Preact**. This allows for a reactive UI (Cart Flyout, Icon Badges) that maintains state across page transitions and browser sessions without the overhead of heavy frameworks, keeping the bundle size minimal.

### 3. Native Trilingual Routing (IT/EN/ES)
The multilingual system was expanded to include **Spanish**, maintaining robust routing consistency. The architecture handles separate localized paths (`/`, `/en/`, `/es/`) while sharing an optimized component codebase, ensuring SEO excellence across global markets.

---

## 🛡️ Security-by-Design Implementation
The project follows modern security standards to ensure data protection and resilience:

*   **Secure Environment Management:** Sensitive configurations (Stripe keys, Shipping APIs) are managed via **Environment Variables (.env)**, protected from source control and strictly server-side.
*   **Authentication & Anti-Spam:** The integrated contact form utilizes a secure validation system with **Honeypot techniques** to prevent automated bot abuse.
*   **Network & Perimeter Defense:**
    *   **Security Headers:** Implementation of **Content Security Policy (CSP)** and **HSTS** to prevent XSS and Man-in-the-Middle attacks.
    *   **Origin Protection:** Deployment on Node.js-ready environments with CDN-level filtering for DDoS mitigation.

---

## 🛠️ Engineering Challenges & Solutions

*   **Challenge:** Integrating a reactive e-commerce state in a primarily static Astro environment.
    *   **Solution:** Leveraged **Nano Stores** for lightweight, framework-agnostic state management, allowing Preact components to synchronize state across the entire site with zero performance penalty.
*   **Challenge:** Maintaining a 100/100 Lighthouse score while transitioning to SSR.
    *   **Solution:** Careful use of `client:load` directives and server-side logic optimization, ensuring that only necessary JavaScript is delivered to the client.

---

## 📈 Performance Results
*   **Lighthouse Performance:** 98-100/100 ✅
*   **First Contentful Paint:** < 0.6s ⚡
*   **State Persistence:** Persistent Cart via LocalStorage 🛒

---

> **Developer:** Domenico Filippo Innamorato  
> **Art Name:** The Dev Heart  
> **Live Site:** [https://www.roccacinie.it](https://www.roccacinie.it)
