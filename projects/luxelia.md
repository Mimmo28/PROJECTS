# 🚀 Personal Portfolio & Engineering Showcase
> **Architecture:** WordPress / WooCommerce Custom Ecosystem | **Tech Stack:** PHP, REST API, Python, AI Agents | **Status:** Production

## 📋 Project Overview
This project represents the development, SEO engineering, and automation ecosystem built for **Luxelia**, a production e-commerce platform managing over 3,500 products. The architecture integrates custom WordPress plugins, automated SEO pipelines, REST API integrations, and AI-driven automation workflows to scale catalog optimization, technical SEO compliance, and conversion rate optimization.

---

## 🏗️ Architectural Decisions

### 1. Custom Plugin Ecosystem (`luxelia-seo-api` & Loyalty Engine)
Rather than relying solely on off-the-shelf plugins, I engineered custom PHP solutions:
*   **`luxelia-seo-api`**: Built a specialized REST API controller for granular, automated management of Rank Math SEO metadata, sitemaps, and programmatic indexing.
*   **Loyalty & Promotion Engine**: Developed a tailored WooCommerce coupon and retention plugin enforcing business rules (first-order incentives, minimum thresholds, single-use validations, and anti-abuse checks).

### 2. High-Performance Automation Pipeline
To manage massive catalog updates across thousands of products, I developed an external automation suite in Python:
*   **Batch Processing & Rate Limiting**: Managed large-scale API operations with exponential backoff and error recovery.
*   **AI Agent Workflows**: Leveraged LLMs and vision workflows for structured catalog enrichment, alt-text generation, and contextual content publishing.

---

## 🛡️ Security-by-Design Implementation
The project implements stringent security practices across data handling and WordPress APIs:

*   **API Authentication & Least Privilege:** Secure authentication via application passwords and WooCommerce REST credentials, keeping administrative keys isolated in environment variables (`.env`).
*   **Input Sanitization & Validation:** All custom endpoints sanitize incoming payloads (`sanitize_text_field`, nonce verification, schema validation) preventing SQL injection and arbitrary code execution.
*   **Data Integrity & Rollback Controls:** Automated audit scripts generate validation reports before and after bulk operations to prevent data corruption.

---

## 🛠️ Engineering Challenges & Solutions

*   **Challenge:** Programmatically optimizing SEO attributes across 3,500+ product images and 70 categories without performance degradation.
    *   **Solution:** Built asynchronous Python pipelines interfacing with WordPress REST API and Rank Math endpoints, updating metadata in controlled batches with real-time audit logging.
*   **Challenge:** Enforcing strict coupon rules in WooCommerce without slowing down checkout.
    *   **Solution:** Hooked into native WooCommerce validation filters with lightweight server-side checks, caching customer order history lookups.

---

## 📈 Documented Results
*   **Optimized Categories:** 70 product categories optimized with metadata and editorial content ✅
*   **Catalog Alt-Text Coverage:** 3,530+ primary product images updated with contextual accessibility data ⚡
*   **Internal Linking:** Automated insertion of 64 contextual internal links across commercial silos 🔗
*   **Technical SEO Audit:** 100% compliance on sitemaps, canonical tags, and 301 redirects 🎯

---

> **Developer:** Domenico Filippo Innamorato  
> **Art Name:** The Dev Heart  
> **Live Site:** [https://www.luxelia.it](https://www.luxelia.it)
