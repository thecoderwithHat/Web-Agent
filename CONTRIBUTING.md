# Contributing to Web-Agent

Thank you for your interest in contributing to Web Agent! This document provides guidelines and instructions for contributing to this project.

## Table of Contents

- [Getting Started](#getting-started)
  - [Development Environment](#development-environment)
  - [Installation](#installation-from-source)
  
- [Development Workflow](#development-workflow)
  - [Branching Strategy](#branching-strategy)
  - [Commit Messages](#commit-messages)
  - [Code Style](#code-style)
  - [Pre-commit Hooks](#pre-commit-hooks)

- [Testing](#testing)
  - [Running Tests](#running-tests)
  - [Adding Tests](#adding-tests)

- [Pull Requests](#pull-requests)
  - [Creating a Pull Request](#creating-a-pull-request)
  - [Pull Request Template](#pull-request-template)
  
- [Documentation](#documentation)
- [Getting Help](#getting-help)

## Getting Started

### Development Environment

WebAgent requires:
- Python 3.11 or later

### Installation

1. Fork the repository on GitHub.
2. Clone your fork locally:

```bash
git clone https://github.com/CursorTouch/Web-Agent.git
cd web-agent
```

3. Install the package in development mode:

```bash
pip install -e ".[dev,search]"
```

4. Set up pre-commit hooks:

```bash
pip install pre-commit
pre-commit install
```

## Development Workflow

### Branching Strategy

- `main` branch contains the latest stable code
- Create feature branches from `main` named according to the feature you're implementing: `feature/your-feature-name`
- For bug fixes, use: `fix/bug-description`

### Commit Messages

For now no commit style is enforced, try to keep your commit messages informational.

### Code Style

Key style guidelines:

- Line length: 100 characters
- Use double quotes for strings
- Follow PEP 8 naming conventions
- Add type hints to function signatures

### Pre-commit Hooks

We use pre-commit hooks to ensure code quality before committing. The configuration is in `.pre-commit-config.yaml`.

The hooks will:

- Run linting checks
- Check for trailing whitespace and fix it
- Ensure files end with a newline
- Validate YAML files
- Check for large files
- Remove debug statements

## Testing

### Running Tests

Run the test suite with pytest:

```bash
pytest
```

To run specific test categories:

```bash
pytest tests/
```

### Adding Tests

- Add unit tests for new functionality in `tests/unit/`
- For slow or network-dependent tests, mark them with `@pytest.mark.slow` or `@pytest.mark.integration`
- Aim for high test coverage of new code

## Pull Requests

### Creating a Pull Request

1. Ensure your code passes all tests and pre-commit hooks
2. Push your changes to your fork
3. Submit a pull request to the main repository
4. Follow the pull request template

## Documentation

- Update docstrings for new or modified functions, classes, and methods
- Use Google-style docstrings:

```python
def function_name(param1: type, param2: type) -> return_type:
    """Short description.
      Longer description if needed.

     Args:
        param1: Description of param1
        param2: Description of param2

    Returns:
        Description of return value

    Raises:
        ExceptionType: When and why this exception is raised
    """
```


## Getting Help

If you need help with your contribution:

- Open an issue for discussion
- Reach out to any of the our maintainers

We look forward to your contributions!