# My Agent Demo

A multi‑agent demonstration project showcasing how to build, orchestrate, and document AI agents using the OpenAI API.

## Table of Contents
- [Project Overview](#project-overview)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)

---

## Project Overview

This repository contains a demo implementation of a **multi‑agent system**. It includes:
- Core agent framework
- Example agents (e.g., a planner, a researcher, and a summarizer)
- Utilities for prompting, logging, and error handling
- Sample scripts to run end‑to‑end workflows

The goal is to provide a clear, well‑documented starting point for developers interested in building their own AI‑driven agent architectures.

---

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/my-agent-demo.git
   cd my-agent-demo
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv .venv
   source .venv/bin/activate   # On Windows use `.venv\Scripts\activate`
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up OpenAI credentials**
   - Obtain an API key from the OpenAI platform.
   - Export it as an environment variable:
     ```bash
     export OPENAI_API_KEY="your-api-key"
     ```
   - Alternatively, create a `.env` file in the project root:
     ```
     OPENAI_API_KEY=your-api-key
     ```

---

## Usage

Run the main demo script to see the agents in action:
```bash
python demo.py
```

### Example Output
```
[Planner] Planning the task...
[Researcher] Gathering information about ...
[Summarizer] Summarizing the findings...
```

#### Custom Scripts
You can create your own scripts by importing the agent classes:
```python
from agents.planner import PlannerAgent
from agents.researcher import ResearcherAgent
from agents.summarizer import SummarizerAgent

planner = PlannerAgent()
researcher = ResearcherAgent()
summarizer = SummarizerAgent()

# Example workflow
plan = planner.create_plan('Explain quantum computing')
info = researcher.fetch_information(plan)
summary = summarizer.summarize(info)
print(summary)
```

---

## Configuration

Configuration options are stored in `config.yaml`. Common settings include:
- `model`: The OpenAI model to use (e.g., `gpt-4o-mini`).
- `temperature`: Sampling temperature.
- `max_tokens`: Token limit per request.

Edit `config.yaml` to suit your needs, or override settings via environment variables.

---

## Contributing

Contributions are welcome! Please follow these steps:
1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Make your changes** and ensure tests pass.
4. **Commit with a clear message**
5. **Push to your fork** and open a Pull Request.

### Code Style
- Use `black` for formatting.
- Run `flake8` for linting.
- Write docstrings for all public functions and classes.

### Testing
```bash
pytest
```

---

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.

---

*Happy hacking!*
