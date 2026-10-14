# Lab 5: Static Code Analysis — Reflection

### 1. What is static code analysis?

Static code analysis examines source code without running the program. It helps identify possible bugs, security vulnerabilities and coding-style violations early in development.

### 2. What are Pylint, Bandit and Flake8 used for?

Pylint checks code quality, naming, documentation and potential programming problems. Bandit identifies common security risks in Python code. Flake8 checks formatting and style rules. Together, they provide a more comprehensive code review.

### 3. What issues were identified and fixed?

The original program had a mutable default argument, inconsistent naming, missing docstrings, an unused sorting parameter and unsafe data-handling patterns. The code was updated with improved validation, JSON-based storage, safer subprocess usage and consistent naming.

### 4. How does static analysis improve software quality?

Static analysis helps identify problems before deployment, improves code readability and maintainability, and reduces security risks. Rerunning the tools after changes helps developers check whether the identified problems have been resolved.
