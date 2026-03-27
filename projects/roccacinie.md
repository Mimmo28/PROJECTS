# 🚀 Personal Portfolio & Engineering Showcase
> **Architecture:** Astro Islands | **Tech Stack:** TypeScript, Tailwind CSS | **Status:** Production

## 📋 Project Overview
This project is a high-performance personal portfolio designed to showcase my engineering background and technical projects. Developed using **Astro**, it focuses on speed, accessibility, and a clean UI/UX, serving as the primary entry point for my professional online presence.

---

## 🏗️ Architectural Decisions

### 1. Component-Based Islands
I utilized Astro's **Islands Architecture** to optimize the critical rendering path. By isolating interactive elements, the site maintains a zero-JS baseline by default, significantly reducing the Time to Interactive (TTI).

### 2. Static Site Generation (SSG)
To ensure maximum availability and performance, the site is pre-rendered at build time. This approach eliminates server-side processing during requests, reducing the attack surface and improving loading speeds via CDN distribution.

---

## 📂 Project Portfolio

| Project Name | Tech Stack | Documentation | Live Demo |
| :--- | :--- | :--- | :--- |
| **Rocca Ciniè** | Astro 6, Tailwind CSS 4, PHP | [Technical Specs](./README.md) | [Visit Live](https://www.roccacinie.it) |
| **Mega Shop Arredi** | Astro, Tailwind, i18n | [Technical Specs](#) | [Visit Live](#) |

---

## 🛡️ Security-by-Design Implementation
L'architettura del sito segue i principi fondamentali della sicurezza informatica per garantire integrità e protezione:

*   **Data Integrity:** Tutti gli asset e le dipendenze sono validati durante la pipeline di CI/CD. Le configurazioni sensibili sono gestite tramite variabili d'ambiente criptate, evitando leak di informazioni nelle build pubbliche.
*   **Authentication & Logic:** I form di contatto e gli eventuali trigger di dashboard utilizzano validazione sicura basata su token e tecniche di honeypot per prevenire abusi automatizzati.
*   **Network & Perimeter Defense:**
    *   **Security Headers:** Implementazione di Content Security Policy (CSP) e HSTS per prevenire attacchi XSS e Man-in-the-Middle.
    *   **Origin Protection:** Il deployment è protetto da un CDN globale che agisce come firewall di prima linea, filtrando il traffico malevolo.

---

## 🛠️ Engineering Challenges & Solutions

*   **Challenge:** Mantenere un punteggio Lighthouse di 100/100 utilizzando asset visivi complessi.
    *   **Solution:** Ottimizzazione automatica delle immagini e strategie di lazy-loading tramite Astro.
*   **Challenge:** Documentare repository privati in modo sicuro.
    *   **Solution:** Creazione di questo repository dedicato (`PROGETTI`) per fungere da ponte tra la riservatezza del codice e la visibilità professionale.

---

## 📈 Performance Results
*   **Lighthouse Performance:** 100/100
*   **First Contentful Paint:** < 0.5s
*   **Total Blocking Time:** 0ms

---

> **Developer:** Domenico Filippo Innamorato  
> **Art Name:** dfinn.dev  
> **Live Site:** [www.roccacinie.it](https://www.roccacinie.it)
