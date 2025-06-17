# 🔐 Secure Log Analyzer

A lightweight and extensible **CLI-based tool** to analyze application and server logs for suspicious patterns, IP addresses, and potential security threats.

Built with security best practices, modern Python tooling, and an extensible architecture.

---

## 🚀 Features

- ✅ Detect suspicious access patterns (admin, login, git, .env, etc.)
- 🛑 Detect HTTP error codes like 401, 403, and 500
- 🐍 Curl or scripted login attempt detection
- 🌐 Show top N most frequent IPs
- 🔍 Log level filtering (e.g., ERROR, WARNING)
- 📄 Output results as plain text or JSON
- 🧪 Built-in test suite using `pytest`
- 📦 Clean project scaffolding via Cookiecutter
- 🔐 Static analysis and secret scanning via pre-commit hooks

---

---
## 📦 Installation & Usage

```bash
git clone https://github.com/yourname/secure-log-analyzer.git
cd secure-log-analyzer
python -m venv venv
source venv/bin/activate
pip install -e .[dev]

# Analyze a log file
python main.py --file sample_logs/app.log --top-ips 5

---

## ✅ Pre-commit Setup

```bash
pre-commit install
pre-commit run --all-files

---

## 🧱 Folder Structure

```bash
secure-log-analyzer/
├── analyzer/                  # Core logic and modules
│   ├── core.py
│   ├── detectors.py
│   ├── filters.py
│   ├── reporters.py
│   ├── utils.py
│   └── patterns.json          # Default detection rules
├── sample_logs/              # Example log files
│   └── app.log
├── tests/                    # Unit tests
├── main.py                   # CLI entrypoint
├── pyproject.toml            # Tooling and dependency config
├── .pre-commit-config.yaml   # Pre-commit hook config
├── .secrets.baseline         # Baseline for detect-secrets
└── README.md

---
