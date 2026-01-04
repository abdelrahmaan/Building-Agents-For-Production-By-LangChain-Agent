# 🔗 Introduction to LangChain - Python

## Introduction

Salam,
My name is Abdulrahman Kamar and happy for you to join me in this course.

---

## 🚀 Setup

### Prerequisites

- The Chrome browser is recommended
- Ensure you're using Python >=3.12, <3.14 [More info](#python-virtual-environments)
- A package/project manager: [uv](https://docs.astral.sh/uv/) (recommended) or [pip](https://pypi.org/project/pip/)
    - note: `uv` is also required in Module 2, Lesson 1 to run the MCP server with `uvx`


### Installation

Download the course repository
```bash
# Clone the repo
git clone https://github.com/abdelrahmaan/Building-Agents-For-Production-By-LangChain-Agent.git
cd Building-Agents-For-Production-By-LangChain-Agent
```

Make a copy of example.env
```bash
# Create .env file
cp example.env .env
```

Edit the .env file to include the keys below. [More info](#model-providers)
```bash
# Required for model usage
OPENAI_API_KEY='your_openai_api_key_here'
TAVILY_API_KEY='your_tavily_api_key_here'

# optional, only used in Lesson 1 once
ANTHROPIC_API_KEY='your_anthropic_api_key_here'

# Optional for evaluation and tracing
LANGSMITH_API_KEY='your_langsmith_api_key_here'
LANGSMITH_TRACING=true
LANGSMITH_PROJECT=Building-Agents-For-Production-By-LangChain-Agent
```

Make a virtual environment and install dependencies. [More info](#python-virtual-environments)

<details open>
<summary>Using uv (recommended)</summary>

```bash
uv sync
```

</details>

<details>
<summary>Using pip</summary>

```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

</details>

### Quick Start Verification

After completing the Setup section, you can run this command to verify your environment:

<details open>
<summary>Using uv</summary>

```bash
uv run python env_utils.py
```

</details>

<details>
<summary>Using pip</summary>

```bash
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
python env_utils.py
```

</details>

### Run Notebooks [More Info](#development-environment)

<details open>
<summary>Using uv (recommended)</summary>

```bash
uv run jupyter lab
```

</details>

<details>
<summary>Using pip</summary>

```bash
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
jupyter lab
```

</details>


## 📚 Lessons
This repository contains three Modules that serve as introductions to many of LangChain's most-used features.

---

### Lesson 1: LangChain Foundational 

- How to call llm?
- Chat models
- Invocation
    - invoke
    - stream
    - batch 

- Tool Calling


## 📖 Related Resources

### Python Virtual Environments 

Managing your Python version is often best done with virtual environments. This allows you to select a Python version for the course independent of the system Python version.

<details open>
<summary>Using uv (recommended)</summary>

`uv` will install a version of Python compatible with the versions specified in the `pyproject.toml` in the `.venv` directory when running the `uv sync` specified above. It will use this version when invoking with `uv run`. For additional information, please see [uv](https://docs.astral.sh/uv/).
</details>

<details>
<summary>Using pyenv + pip</summary>

If you are using pip instead of uv, you may prefer using pyenv to manage your Python versions. For additional information, please see [pyenv](https://github.com/pyenv/pyenv).

```bash
pyenv install 3.12
pyenv local 3.12
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

</details>

### Getting Started with LangSmith

- Create a [LangSmith](https://smith.langchain.com/) account
- Create a LangSmith API key

<img width="600" alt="LangSmith Dashboard" src="https://github.com/user-attachments/assets/e39b8364-c3e3-4c75-a287-d9d4685caad5" />

<img width="600" alt="LangSmith API Keys" src="https://github.com/user-attachments/assets/2e916b2d-e3b0-4c59-a178-c5818604b8fe" />

- Update your .env file you created with your new LangSmith API Key.

For more information on LangSmith, see our docs [here](https://docs.langchain.com/langsmith/home).

### Environment Variables

This course uses the [dotenv](https://pypi.org/project/python-dotenv) module to read key-value pairs from the .env file and set them in the environment in the Jupyter notebook. They do not need to be set globally in your system environment.

### Development Environment

The course uses [Jupyter](https://jupyter.org/) notebooks. Jupyter is installed and can be run as described above. Jupyter notebooks can also be edited and run in VSCode or other VSCode variants such as Windsurf or Cursor.  