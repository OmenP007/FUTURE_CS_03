# 📜 Tech Manifest: Scripts & Modules

The scanning process is orchestrated by a unique polyglot architecture combining the flexibility of Python, the raw speed of C, and the data processing power of Java.

## 🐍 Python Modules (Orchestration)
- **`api_security_engine.py`**: The central orchestrator. Manages the scan lifecycle, API endpoint discovery, and coordination between modules.
- **`gui/dashboard.py`**: The interactive CustomTkinter interface for real-time monitoring and target management.
- **`scanners/`**: Contains specific protocol and vulnerability scanners (REST, GraphQL, tokens, rate limits).

## ⚡ C Modules (Network Acceleration)
- **`core/c_modules/api_scanner.c`**: Implements high-speed concurrent network probing, bypassing Python's GIL to test for Rate-Limiting missing controls.
- **`core/c_modules/token_analyzer.c`**: Handles fast cryptographic and algorithmic checks for JWT validation.

## ☕ Java Modules (Data Analysis)
- **`core/java/DataAnalyzer.java`**: Exploits the JVM via IPC (`stdin/stdout`) to process megabytes of HTTP responses with ultra-fast Regex, detecting leaked PII and exposed credentials.

## 📊 Reporting
- **`reports/report_generator.py`**: Utilizes `Jinja2` to generate high-fidelity, dynamic HTML reports with a modern "cyber" design.
