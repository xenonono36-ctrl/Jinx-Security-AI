# Jinx-Security-AI

AI-powered code security assistant that scans codebases for vulnerabilities (SQL injection, XSS, hardcoded secrets, insecure auth) and auto-generates fixes. Combines static analysis with LLM reasoning to catch issues faster than manual review, then suggests or applies secure patches directly in your workflow.

---

## ✨ Features

- 🔍 **Vulnerability Scanning** — Detects common security flaws including SQL injection, XSS, hardcoded API keys/secrets, insecure authentication, and misconfigurations.
- 🤖 **LLM-Driven Analysis** — Uses large language models alongside static analysis to understand code context and reduce false positives.
- 🛠️ **Automated Fixes** — Generates secure code patches automatically, with the option to review before applying.
- ⚡ **Fast Feedback Loop** — Designed to catch issues earlier and faster than manual code review.
- 🔗 **Workflow Integration** — Fits into existing developer workflows (CI/CD pipelines, pre-commit hooks, or IDE plugins).

---

## 🏗️ How It Works

1. **Scan** — The tool analyzes your codebase using static analysis rules to flag potential vulnerabilities.
2. **Reason** — An LLM reviews flagged code in context to confirm real issues and filter out noise.
3. **Fix** — The assistant generates a secure patch for each confirmed vulnerability.
4. **Apply** — You review and approve fixes, or configure auto-apply for trusted fix types.

---

## 📦 Installation

```bash
# Clone the repository
git clone https://github.com/xenonono36-ctrl/Jinx-Security-AI.git
cd Jinx-Security-AI

# Install dependencies
npm install
# or
pip install -r requirements.txt
```

> ⚠️ Keep whichever install line matches your stack (Node or Python) and remove the other, and add any required environment variables (e.g., API keys for the LLM provider).

---

## 🚀 Usage

```bash
# Run a scan on your project
scan-tool scan ./path/to/project

# Run a scan and automatically apply fixes
scan-tool scan ./path/to/project --fix
```

Example output:
