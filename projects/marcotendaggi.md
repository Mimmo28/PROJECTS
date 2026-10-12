# 🚀 Personal Portfolio & Engineering Showcase
> **Architecture:** Astro Islands | **Tech Stack:** TypeScript, Tailwind CSS v4, i18n | **Status:** Production

## 📋 Project Overview
This project is a high-performance web platform for custom craftsmanship and artisan manufacturing businesses. Developed with **Astro**, it focuses on extreme loading speed, accessible UI/UX, multi-language internationalization, and high-conversion local lead generation, serving as a primary production-grade showcase for modern static-first web applications.

---

## 🏗️ Architectural Decisions

### 1. Component-Based Islands & Zero-JS Baseline
Utilizes Astro's **Islands Architecture** to strictly isolate runtime client scripts. Interactive UI components (such as native Lightbox gallery, Cookie Banner, and contact floating action triggers) load minimal JavaScript on demand, keeping baseline pages at zero client-side JavaScript overhead for lightning-fast Time to Interactive (TTI).

### 2. Static Site Generation (SSG) & Edge CDN
Pre-rendered entirely at build time into pure static HTML/CSS. Eliminates server runtime dependencies and runtime database queries, shrinking the attack surface to zero while enabling instant cache delivery (TTFB < 100ms) on edge CDNs.

### 3. Native i18n Routing & Localization
Implemented clean URL prefix-less default localization (`it`) with seamless secondary language routing (`en`), hreflang alternates, and canonical management without bloated external libraries.

---

## 🛡️ Security-by-Design Implementation

*   **Zero Server Attack Surface:** Full SSG model eliminates vulnerabilities like SQL injection, server-side template injection (SSTI), or backend exploits.
*   **Asset & Dependency Integrity:** Automated CI/CD dependency audits (`npm audit --audit-level=high`) protect the build pipeline against vulnerabilities.
*   **Hardened Security & Headers:** Prepared for HSTS, anti-clickjacking policies, and strict Content Security Policies (CSP).

---

## 🛠️ Engineering Highlights & Solutions

*   **Tailwind CSS v4 & Vite Engine:** Built with Tailwind CSS v4 via `@tailwindcss/vite` plugin for ultra-fast builds and zero unused CSS bundle output.
*   **Automated Asset Pipeline:** Uses Astro Image optimization pipeline with responsive `srcset`, automated WebP conversion, and lazy-loading for heavy photographic galleries.
*   **Structured SEO & Microdata:** Comprehensive JSON-LD structured data (`LocalBusiness` / `HomeAndConstructionBusiness`), XML sitemap automation with `@astrojs/sitemap`, and OpenGraph protocols.

---

## 📈 Performance Results
*   **Lighthouse Performance:** 98-100/100 ✅
*   **First Contentful Paint (FCP):** < 0.6s ⚡
*   **Largest Contentful Paint (LCP):** < 1.2s ⚡
*   **Total Blocking Time (TBT):** 0ms 🚀
*   **Cumulative Layout Shift (CLS):** 0 📐

---

> **Developer:** Domenico Filippo Innamorato  
> **Art Name:** The Dev Heart  
> **Live Site:** [https://mimmo28.github.io/marcotendaggi/](https://mimmo28.github.io/marcotendaggi/)
