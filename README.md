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
[HIGH] SQL Injection detected in db/queries.py:42
→ Suggested fix: use parameterized queries
[MEDIUM] Hardcoded API key found in config.js:15
→ Suggested fix: move to environment variable


---

## 🔧 Configuration

You can customize scan behavior with a config file (e.g., `.scanconfig.yml`):

```yaml
rules:
  sql_injection: true
  xss: true
  hardcoded_secrets: true
  insecure_auth: true

auto_fix: false
severity_threshold: medium
```

---

## 🧩 Integrations

- **CI/CD** — Add as a step in GitHub Actions, GitLab CI, or Jenkins pipelines.
- **Pre-commit Hook** — Catch issues before code is even committed.
- **IDE Plugin** *(planned)* — Real-time scanning while you code.

---

## 🗺️ Roadmap

- [ ] Support for additional languages/frameworks
- [ ] IDE plugin (VS Code)
- [ ] Custom rule authoring
- [ ] Dashboard for tracking vulnerability trends over time

---

## 🤝 Contributing

Contributions are welcome! Please:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes
4. Open a pull request

See `CONTRIBUTING.md` for detailed guidelines.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 📬 Contact

For questions, issues, or feature requests, please open an [issue](https://github.com/xenonono36-ctrl/Jinx-Security-AI/issues).
