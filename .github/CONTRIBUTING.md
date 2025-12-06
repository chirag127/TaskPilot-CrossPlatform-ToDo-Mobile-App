# 🤝 Contributing to TaskFlow-Mobile-Todo-App

As the Apex Technical Authority, we mandate that all contributions adhere to the highest standards of code quality, architectural integrity, and future-proofing. This repository follows a strict contribution workflow to ensure **Zero-Defect, High-Velocity** development.

## 1. Core Principles

Before contributing, internalize the following architectural mandates:

*   **SOLID Compliance:** All new components, modules, or logic must demonstrably adhere to SOLID principles.
*   **DRY Enforcement:** Duplication is an immediate refactoring trigger.
*   **YAGNI Adherence:** Implement only what is currently required. Avoid premature abstraction unless clearly necessitated by future projections (e.g., explicit platform branching).
*   **TypeScript Strictness (If applicable):** If modifying the TypeScript/JavaScript core, enforce maximum type safety.

## 2. Development Environment Setup

Ensure your local environment mirrors the CI/CD pipeline for maximum fidelity.

1.  **Fork the Repository:** Create your own fork of `chirag127/TaskFlow-Mobile-Todo-App`.
2.  **Clone Your Fork:**
    bash
    git clone https://github.com/YOUR_USERNAME/TaskFlow-Mobile-Todo-App.git
    cd TaskFlow-Mobile-Todo-App
    
3.  **Install Dependencies (Expo/React Native Standard):**
    bash
    # Using npm/yarn based on project preference, assume npm for standardization
    npm install
    # Ensure Expo CLI is globally available or use npx
    npx expo doctor -c
    
4.  **Create a Feature Branch:** Name it descriptively, prefixing with `feat/`, `fix/`, or `refactor/`.
    bash
    git checkout -b feat/new-notification-service
    

## 3. Contribution Workflow

All contributions must follow this mandatory sequence:

### A. Local Verification

Ensure all local checks pass before committing.

1.  **Linting & Formatting:** Use Biome (if adopted) or standard ESLint/Prettier to ensure style parity.
    bash
    npm run lint
    npm run format
    
2.  **Unit Testing:** Run relevant unit tests using Vitest.
    bash
    npm run test:unit
    
3.  **Build Check:** Ensure the application compiles without warnings/errors on the target platform (iOS/Android).
    bash
    npm run build:dev
    

### B. Commit Guidelines

Use the **Conventional Commits** specification for all commits. This fuels automated changelog generation.

**Format:** `<type>(<scope>): <subject>`

*   **Examples:**
    *   `feat(storage): Implement async/await wrapper for AsyncStorage persistence`
    *   `fix(ui): Correct alignment issue on TaskItem component for Android devices`
    *   `refactor(state): Migrate component state to global Context API using Signals approach`

### C. Pull Request Submission

1.  **Push to Fork:** Push your feature branch to your fork.
    bash
    git push origin feat/your-feature-name
    
2.  **Open PR:** Open a Pull Request targeting `chirag127:main`.
3.  **Use Template:** Fill out the mandatory **Pull Request Template** (`.github/PULL_REQUEST_TEMPLATE.md`). Do not skip any sections.
4.  **Verification:** Allow the GitHub Actions CI pipeline (`.github/workflows/ci.yml`) to run successfully. PRs failing CI will be automatically rejected by reviewers.

## 4. Reporting Issues

If you discover a bug or wish to propose a feature, utilize the provided issue templates in the `.github/ISSUE_TEMPLATE/` directory. Be specific, provide reproduction steps, and adhere to the principles outlined in `.github/SECURITY.md` when reporting vulnerabilities.

--- 

*By contributing to this repository, you agree to license your contributions under the terms specified in the `LICENSE` file (CC BY-NC 4.0).* 

For deeper guidance on architectural enforcement and automated tooling verification, consult the **AGENTS.md** file.