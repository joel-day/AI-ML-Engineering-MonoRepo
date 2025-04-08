# AI/ML Engineering MonoRepo

All Projects within the AI/ML space that utilize transformers are located here.

## Installation

```bash
# Clone the repository
git clone https://github.com/joel-day/AI-ML-Engineering-MonoRepo.git

# Move to repository directory
cd AI-ML-Engineering-MonoRepo

# Create the virtual environment
uv venv .venv

# Activate the virtual environment
source .venv\bin\activate # Mac/Linux
.venv\Scripts\activate   # Windows

# Sync environment based on dependencies in top-level pyproject.toml file
uv sync

# (OPTIONAL) Sync environment based on dependencies across all packages' pyproject.toml files
uv sync --all-packages
```

## Included Tools & Packages

- **UV**: Used for package management and virtual environment creation. Configured to manage environments in a monorepo setup, ensuring consistency across the project.

- **GitHub Actions**: Ensures that the code works across multiple operating systems (Linux, Mac, and Windows) and supports Python versions 3.10, 3.11, and 3.12. It's a part the CI pipeline and is configured to run on pull requests to main.

- **Pytest**: Configured to run tests and verify the correctness of code execution. It ensures that the codebase remains functional and that new changes don’t introduce unexpected behavior.
```bash
pytest
```
- **Flake8**: Used for checking code compliance with PEP8 standards. It helps maintain a clean and consistent code style across the project by enforcing formatting and style guidelines.
```bash
flake8 .
```

## Projects will be added soon
```bash
flake8 .
```

