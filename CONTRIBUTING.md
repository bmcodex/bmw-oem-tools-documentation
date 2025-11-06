# Contributing to BMW OEM Tools Documentation

We welcome contributions from the community to keep this documentation accurate, comprehensive, and up-to-date.

## 1. How to Contribute

1.  **Fork** the repository.
2.  **Clone** your fork locally.
3.  Create a new **branch** for your changes (`git checkout -b feature/your-feature-name`).
4.  Make your changes, ensuring they adhere to the **Style Guide** below.
5.  **Commit** your changes with descriptive commit messages (see **Commit Guidelines**).
6.  **Push** your branch to your fork.
7.  Open a **Pull Request (PR)** against the `main` branch of this repository.

## 2. Style Guide

*   **Language:** All documentation must be provided in both **English (EN)** and **Polish (PL)**. If you contribute a new section, please provide both translations.
*   **Format:** Use GitHub-flavored Markdown.
*   **Terminology:** Use professional, industry-standard terminology. All technical acronyms (e.g., **DTC**, **ECU**, **ENET**) must be explained upon first use and included in the `glossary.md`.
*   **Citations:** All factual claims, especially those related to official BMW procedures or specifications, **MUST** be cited using inline numeric citations (e.g., `[1]`) and listed in `docs/references.md`.
*   **Tables & Diagrams:** Use tables for comparisons and structured data. Diagrams should be provided in both **SVG** (source) and **PNG** (rendered) formats, placed in `docs/diagrams/`.

## 3. Commit Guidelines

We follow the Conventional Commits specification. Please use the following prefixes:

| Prefix | Description | Example |
| :--- | :--- | :--- |
| `feat` | A new feature or functionality. | `feat: Add detailed section for ISTA/P` |
| `fix` | A bug fix or correction to existing content. | `fix: Corrected ENET IP configuration in docs/tools/e-sys.md` |
| `docs` | Documentation changes only (e.g., typos, formatting). | `docs: Updated glossary with new terms` |
| `style` | Changes that do not affect the meaning of the code (e.g., formatting). | `style: Standardized table formatting in all tool files` |
| `refactor` | A code change that neither fixes a bug nor adds a feature. | `refactor: Restructured docs folder for better navigation` |

## 4. Prohibited Content

**DO NOT** submit any content that includes:

*   Links to pirated software, firmware, or unauthorized sources.
*   Binary files, firmware images, or executable files.
*   Sensitive or proprietary information from BMW AG (unless publicly released and cited).
*   Instructions that promote illegal activities or circumvent security measures.

## 5. Code of Conduct

This project adheres to the Contributor Covenant Code of Conduct. By participating, you are expected to uphold this code. Please report unacceptable behavior to the repository maintainers.
