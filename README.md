# Python CI/CD Pipeline Demo

This project demonstrates a simple CI/CD pipeline for a Python application using GitHub Actions. The pipeline is designed to lint the code, run tests, and ensure high code quality in an automated workflow.

---

## Project Structure

```plaintext
.
├── .github
│   └── workflows
│       └── python-ci-cd.yaml  # GitHub Actions workflow file
├── src
│   ├── __init__.py           # Module initialization
│   └── calculator.py         # Simple calculator module
├── tests
│   ├── __init__.py           # Test module initialization
│   └── test_calculator.py    # Unit tests for the calculator module
├── requirements.txt          # Python dependencies
└── README.md                 # Project documentation
```

---

## CI/CD Pipeline Overview

The GitHub Actions workflow (`.github/workflows/cicd.yaml`) is triggered on:
- Push events to the `main` branch.
- Pull requests targeting the `main` branch.

### Jobs

1. **Setup Environment**:
   - Checkout the repository code.
   - Set up Python (version 3.10).

2. **Lint Code**:
   - Install and run `flake8` to check for code quality issues.

3. **Run Tests**:
   - Install dependencies from `requirements.txt`.
   - Execute tests using `pytest`.

---

## How to Use This Project

### Prerequisites
- Python 3.10 or higher
- `pip` (Python package manager)
- `pytest` and `flake8` (installed via `requirements.txt`)

### Running Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/your-repo.git
   cd your-repo
   ```

2. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Run linting:
   ```bash
   flake8 .
   ```

5. Run tests:
   ```bash
   pytest
   ```
