# RoadC Playground

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
