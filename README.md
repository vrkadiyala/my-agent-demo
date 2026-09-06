# My Agent Demo

A demonstration project showcasing a multi‑agent system built with Python. This repository provides example implementations of agents that can communicate, collaborate, and solve tasks together.

---

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

---

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/my-agent-demo.git
   cd my-agent-demo
   ```
2. **Create a virtual environment** (optional but recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows use `venv\\Scripts\\activate`
   ```
3. **Install the required dependencies**
   ```bash
   pip install -r requirements.txt
   ```
4. **(Optional) Install the package in editable mode**
   ```bash
   pip install -e .
   ```

---

## Usage

The entry point for the demo is `main.py`. Run it with:

```bash
python main.py
```

You can also explore the individual agents located in the `agents/` package. Each agent implements a simple `run()` method that can be invoked directly:

```python
from agents.chat_agent import ChatAgent

agent = ChatAgent()
agent.run()
```

---

## Examples

Below are a few quick examples to get you started.

### 1. Simple chat between two agents
```python
from agents.chat_agent import ChatAgent
from agents.task_agent import TaskAgent

chat = ChatAgent(name="Alice")
task = TaskAgent(name="Bob")

chat.send_message("Hello, Bob! Can you help me plan a trip?")
response = task.process_message(chat.last_message)
print(response)
```

### 2. Running the full multi‑agent pipeline
```bash
python scripts/run_pipeline.py --config configs/pipeline.yaml
```

Check the `scripts/` directory for more ready‑to‑run examples.

---

## Contributing

Contributions are welcome! Please follow these steps:

1. **Fork the repository**
2. **Create a new branch** for your feature or bug‑fix:
   ```bash
   git checkout -b my-feature-branch
   ```
3. **Make your changes** and ensure the code passes linting and tests:
   ```bash
   flake8 .
   pytest
   ```
4. **Commit your changes** with a clear commit message.
5. **Push to your fork** and open a Pull Request against the `main` branch.

Please adhere to the existing code style and include appropriate unit tests for new functionality.

---

## License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---

*Happy coding!*
