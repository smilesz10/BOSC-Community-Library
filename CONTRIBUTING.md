# Contributing to BOSC Community Library

Thank you for your interest in improving our public-sector resource! Please follow these guidelines to ensure a smooth contribution process.

## How to Report Bugs
* Before creating an issue, search the existing tracker to see if the bug has been reported.
* [cite_start]Use the **Issue Template** provided in the repository to report a bug[cite: 19].
* Provide a clear description, steps to reproduce, and the expected vs. actual behavior.

## Branching Strategy
[cite_start]To maintain a clean repository history, we use a feature-branch workflow[cite: 37]:
1. **Main Branch:** Reserved for stable, production-ready code.
2. **Feature Branches:** All work must be done in a branch named `feature/description` or `fix/description` (e.g., `feature/swahili-support`).
3. [cite_start]**Pull Requests:** Work must be merged into `main` via a Pull Request (PR) after a peer review[cite: 37].

## Coding Standards
* **Documentation:** All new features must include updates to the relevant Markdown files.
* **Linting:** Ensure code is formatted and free of syntax errors before submission.
* **Commit Messages:** Use descriptive messages (e.g., "Add Swahili localization to resource index") instead of vague terms like "update file."