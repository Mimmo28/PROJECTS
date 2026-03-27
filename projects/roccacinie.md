# 🚀 Personal Portfolio & Engineering Showcase
> **Architecture:** Astro Islands | **Tech Stack:** TypeScript, Tailwind CSS, PHP | **Status:** Production

## 📋 Project Overview
This project is a high-performance showcase of the **Rocca Ciniè** digital ecosystem, representing a biological farm in the heart of Sicily. Developed using **Astro**, it focuses on extreme speed, native multilingual support (IT/EN), and a premium UI/UX, serving as a primary example of my ability to build production-ready, secure, and SEO-optimized web applications for the agricultural and e-commerce sectors.

---

## 🏗️ Architectural Decisions

### 1. Component-Based Islands
I utilized Astro's **Islands Architecture** to optimize the critical rendering path. By isolating interactive elements (like the navigation drawer, multi-language switcher, and dynamic FAB buttons), the site maintains a zero-JS baseline by default, significantly reducing the Time to Interactive (TTI) and improving overall performance for mobile users.

### 2. Native i18n Routing
To ensure global reach, I implemented a robust **multilingual routing system**. Using Astro’s file-based routing, the architecture handles separate localized paths (`/` for IT, `/en/` for EN) while sharing a single, optimized component codebase, ensuring SEO consistency across different languages.

---

## 🛡️ Security-by-Design Implementation
The project follows modern security standards to ensure data protection and resilience:

*   **Data Integrity:** All assets and dependencies are validated during the build process. Sensitive configurations (like the PHP mailer settings) are managed through secure environment variables, ensuring no information leakage occurs in the public build.
*   **Authentication & Anti-Spam:** The integrated contact form utilizes a **PHP-based backend** with secure validation and **Honeypot techniques** to prevent automated bot abuse, ensuring that only legitimate customer requests are processed.
*   **Network & Perimeter Defense:**
    *   **Security Headers:** Implementation of **Content Security Policy (CSP)** and **HSTS** to prevent XSS and Man-in-the-Middle attacks.
    *   **Origin Protection:** Deployment behind a global CDN that acts as a first-line firewall, filtering malicious traffic and mitigating DDoS risks before they reach the application logic.

---

## 🛠️ Engineering Challenges & Solutions

*   **Challenge:** Maintaining a 100/100 Lighthouse score while handling high-resolution agricultural and product imagery.
    *   **Solution:** Implemented a custom asset pipeline using Astro's `Image` component for automated **WebP/AVIF conversion** and adaptive lazy-loading strategies.
*   **Challenge:** Seamlessly bridging the gap between a static frontend and a functional PHP backend for lead generation.
    *   **Solution:** Developed a decoupled contact architecture where the Astro frontend communicates with a secure PHP endpoint, ensuring scalability and ease of hosting on traditional cPanel environments.

---

## 📈 Performance Results
*   **Lighthouse Performance:** 100/100 ✅
*   **First Contentful Paint:** < 0.5s ⚡
*   **Total Blocking Time:** 0ms 🚀

---

> **Developer:** Domenico Filippo Innamorato  
> **Art Name:** The Dev Heart  
> **Live Site:** [https://www.roccacinie.it](https://www.roccacinie.it)
