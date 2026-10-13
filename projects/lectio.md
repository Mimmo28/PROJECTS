# 🚀 Lectio — AI-Powered PDF Study Engine
> **Architecture:** Modular Pipeline & Semantic Chunking | **Tech Stack:** Python, PyMuPDF, Gemini API, Chromium Headless, Markdown/CSS | **Status:** Active

## 📋 Project Overview
**Lectio** (formerly *Augment PDF*) is an automated educational pipeline designed to transform university lecture slides (PDFs) into structured, comprehensive study guides and handouts. It enriches the original material by interleaving detailed slide-by-slide explanations, conceptual summaries, glossaries, and practice quizzes directly into a newly compiled, bookmarked PDF document without altering the original slide visuals.

---

## 🏗️ Architectural Decisions

### 1. Two-Stage Semantic Segmentation Pipeline
Rather than processing slides in rigid arbitrary batches, Lectio features a dual-layer planning architecture:
- **Semantic Chunking:** Analyzes slide density, headers, and conceptual continuity using local heuristics or LLM planners (`Gemini`) to group related slides into logical teaching units.
- **Single-Shot Enrichment Execution:** Consolidates explanations, synthesis, and self-assessment quizzes into a single prompt per thematic block, drastically cutting API latency, token overhead, and model drift.

### 2. Lossless Document Recomposition & Headless Rendering
- Utilizes **PyMuPDF (`fitz`)** for high-precision extraction, layout analysis, bookmark/TOC generation, and PDF page merging.
- Leverages a **Headless Chromium** rendering engine with custom CSS styling to generate publication-grade typographical pages for explanatory notes and quizzes.
- Preserves 100% of the original slide layouts while interleaving augmented study chapters seamlessly.

### 3. Resilient Multimodal Vision & Fallback Engine
- **Vision Fallback:** For visual-heavy slides with sparse extractable text (e.g., hardware diagrams, network topographies), the pipeline automatically converts target slides to images for multimodal vision reasoning.
- **Fail-Safe Model Routing:** Implements tier-based model fallbacks (Primary $\rightarrow$ Secondary) with structural output validation (`warn` / `strict`) to prevent truncated or malformed responses.

---

## 🛡️ Security & Reliability by Design

*   **Zero Leakage & Secure Environment:** API keys (`GEMINI_API_KEY`) and secret configurations are managed strictly via environment variables (`.env`) with zero-commit policies.
*   **Deterministic Multi-Level Cache (v2):** Prevents unnecessary API calls through strict hashing of prompts, model versions, and chunking parameters, providing offline execution resilience and reproducible outputs.
*   **Structural Integrity Verification:** Built-in validators inspect completeness, slide coverage, and formatting rules before committing artifacts to disk.

---

## 🛠️ Engineering Highlights & Features

*   **Contextual Short-Term Memory:** Propagates running glossaries and key conceptual summaries across consecutive chunks to eliminate redundant definitions and avoid repetitive explanations.
*   **Configurable Subject Profiles:** Tailors tone, scientific depth, and teaching pedagogy via modular YAML profile definitions (`subjects/`).
*   **Extensible CLI Toolchain:** Rich command-line interface supporting `--dry-run`, `--segment-only`, `--heuristic-chunks`, and custom plan import/export.

---

## 📈 Performance & Impact
*   **Token Efficiency:** Reduced API overhead by ~40% via unified single-pass chunk prompting.
*   **Study Time Optimization:** Cuts manual lecture note compilation time down from hours to minutes.
*   **100% Layout Fidelity:** Perfectly preserves original slides alongside high-fidelity vector notes and interactive PDF bookmarks.

---

> **Developer:** Domenico Filippo Innamorato  
> **Source Repository:** *Private IP / Confidential Repository*
