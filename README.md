# LLM Firewall


All code changes are subjected to an automated validation pipeline prior to acceptance.

    Black ensures consistent code formatting.

    Ruff performs linting to identify errors and style issues.

    isort enforces consistent ordering of import statements.

    mypy performs strict type checking to prevent type‑related defects.

    Bandit conducts static security analysis to detect potential vulnerabilities.

All unit and integration tests, including asynchronous tests, are executed with pytest, with coverage measurement to ensure a high proportion of the codebase is tested. Only changes that pass these checks are packaged into a deployable Docker image. The pipeline executes both locally via pre‑commit hooks and remotely via GitHub Actions on every push and pull request.