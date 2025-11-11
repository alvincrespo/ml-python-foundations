# ML Python Foundations

## Prerequisites

- [pyenv](https://github.com/pyenv/pyenv) - Python version management
- [Poetry](https://python-poetry.org/) - Python dependency management

## Setup

### 1. Install pyenv

Follow the [pyenv installation guide](https://github.com/pyenv/pyenv#installation) for your operating system.

For Ubuntu/Debian:
```bash
curl https://pyenv.run | bash
```

Add to your shell configuration (`~/.bashrc`, `~/.zshrc`, etc.):
```bash
export PYENV_ROOT="$HOME/.pyenv"
export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init -)"
```

### 2. Set Python Version

Install and set the Python version for this project:

```bash
pyenv install $(cat .python-version)
pyenv local $(cat .python-version)
```

### 3. Install Poetry

```bash
pip install poetry
```

Verify installation:
```bash
poetry --version
```

### 4. Install Dependencies

Install JupyterLab and other project dependencies:
```bash
poetry install
poetry add jupyterlab # If you're doing it manually
```

## Running JupyterLab

Launch JupyterLab using Poetry:
```bash
poetry run jupyter lab
```

This will start JupyterLab in your default browser.

## Development

### Add Dependencies

```bash
poetry add <package-name>
```

### Add Development Dependencies

```bash
poetry add --group dev <package-name>
```

### Update Dependencies

```bash
poetry update
```

## Project Structure

```
ml-python-foundations/
├── .python-version       # Python version for pyenv
├── pyproject.toml        # Poetry configuration and dependencies
├── poetry.lock           # Locked dependency versions
└── README.md             # This file
```

## References

[Project Jupyter](https://jupyter.org)

[Poetry](https://python-poetry.org/)

[Machine Learning with Python: Foundations](https://www.linkedin.com/learning/machine-learning-with-python-foundations/what-you-should-know)

[StackOverflow - Jupyter kernel doesn't use Poetry environment](https://stackoverflow.com/a/78097001)

[Jupyter Notebooks in VS Code ](https://code.visualstudio.com/docs/datascience/jupyter-notebooks)

[Reddit - Is there a smarter way to build requirements.txt files? ](https://www.reddit.com/r/learnpython/comments/1djw6y9/is_there_a_smarter_way_to_build_requirementstxt/)
