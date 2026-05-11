# 🏗️ Vulskan Architecture & Design

## 🖥️ System Design
Vulskan is designed as a **Polyglot Hybrid Scanner** maximizing the strengths of Python, C, and Java.

### 1. The Orchestrator Core (Python)
- Manages the overall state and the GUI (`customtkinter`).
- Coordinates the scanning phases and generates the final HTML reports using `Jinja2`.
- Handles high-level logic like JWT validation and GraphQL introspection.

### 2. The Network Accelerator (C)
- Compiled as a native extension (`.pyd` / `.so`).
- Bypasses traditional Python socket overhead to achieve CPU-speed request rates.
- Ideal for Rate-Limit testing and concurrent endpoint brute-forcing.

### 3. The Data Analyzer (Java)
- Runs as a detached JVM process communicating via standard I/O (IPC).
- Parses massive HTTP responses without freezing the Python UI.
- Executes complex Regex matching to identify data leaks (PII/Tokens) at blazing speeds.
