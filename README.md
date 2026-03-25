<!-- BlackRoad SEO Enhanced -->

# roadc playground

> Part of **[BlackRoad OS](https://blackroad.io)** — Sovereign Computing for Everyone

[![BlackRoad OS](https://img.shields.io/badge/BlackRoad-OS-ff1d6c?style=for-the-badge)](https://blackroad.io)
[![BlackRoad-Sandbox](https://img.shields.io/badge/Org-BlackRoad-Sandbox-2979ff?style=for-the-badge)](https://github.com/BlackRoad-Sandbox)

**roadc playground** is part of the **BlackRoad OS** ecosystem — a sovereign, distributed operating system built on edge computing, local AI, and mesh networking by **BlackRoad OS, Inc.**

### BlackRoad Ecosystem
| Org | Focus |
|---|---|
| [BlackRoad OS](https://github.com/BlackRoad-OS) | Core platform |
| [BlackRoad OS, Inc.](https://github.com/BlackRoad-OS-Inc) | Corporate |
| [BlackRoad AI](https://github.com/BlackRoad-AI) | AI/ML |
| [BlackRoad Hardware](https://github.com/BlackRoad-Hardware) | Edge hardware |
| [BlackRoad Security](https://github.com/BlackRoad-Security) | Cybersecurity |
| [BlackRoad Quantum](https://github.com/BlackRoad-Quantum) | Quantum computing |
| [BlackRoad Agents](https://github.com/BlackRoad-Agents) | AI agents |
| [BlackRoad Network](https://github.com/BlackRoad-Network) | Mesh networking |

**Website**: [blackroad.io](https://blackroad.io) | **Chat**: [chat.blackroad.io](https://chat.blackroad.io) | **Search**: [search.blackroad.io](https://search.blackroad.io)

---


[![CI](https://github.com/blackboxprogramming/roadc-playground/actions/workflows/ci.yml/badge.svg)](https://github.com/blackboxprogramming/roadc-playground/actions/workflows/ci.yml)
[![Python 3.10+](https://img.shields.io/badge/python-3.10%2B-3776AB.svg)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-009688.svg)](https://fastapi.tiangolo.com)
[![Web IDE](https://img.shields.io/badge/web-IDE-FF6B2B.svg)](https://blackroad.io)



Interactive browser-based REPL for the [RoadC programming language](https://github.com/blackboxprogramming/roadc). Write, run, and experiment with RoadC code directly in your browser.

## Features

- Split-pane code editor with output panel
- 7 built-in examples (Hello World, Fibonacci, Factorial, FizzBuzz, Lists, Closures, Functions)
- Ctrl+Enter to run, Tab for indentation
- Execution timing
- BlackRoad-branded UI

## RoadC Language

```
fun fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n - 1) + fibonacci(n - 2)

let i = 0
while i <= 12:
    print(fibonacci(i))
    i = i + 1
```

## API

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/` | GET | Code editor UI |
| `/health` | GET | Service status |
| `/examples` | GET | Built-in code examples |
| `/run` | POST | Execute RoadC code (`{"code": "..."}`) |

## Run

```bash
pip install -r requirements.txt
python server.py  # http://localhost:8400
```

## Test

```bash
pip install pytest httpx
pytest tests/
```

## Related Projects

| Project | Description |
|---------|-------------|
| [RoadC](https://github.com/blackboxprogramming/roadc) | The RoadC programming language |
| [Universal Computer](https://github.com/blackboxprogramming/universal-computer) | Turing machine simulator |
