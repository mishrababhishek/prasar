# 🌟 Prasar Event Handling Framework 🌟

<div align="center">

<img src="https://raw.githubusercontent.com/mishrababhishek/prasar/master/logo.png" alt="Prasar Logo" width="200" height="200">


[![PyPI version](https://badge.fury.io/py/prasar.svg)](https://badge.fury.io/py/prasar)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python Versions](https://img.shields.io/pypi/pyversions/prasar.svg)](https://pypi.org/project/prasar/)

</div>

<h3 align="center">🚀 Robust, Type-Safe, and Asynchronous Event Handling for Python 🐍</h3>

---

## ✨ Features

- 🔄 Support for both synchronous and asynchronous events
- 🛡️ Strong type checking for event arguments and return types
- 🌈 Custom logging with colored output
- 🎛️ Easy-to-use API for binding and emitting events
- 🧪 Comprehensive error handling and validation

## 🛠️ Installation

To install Prasar, simply use pip:

```bash
pip install prasar
```
## 📚 Dependencies

* Python 3.7+
* colorama
* typing

## 🚀 Quick Start

```python
from prasar import Prasar

# Create a Prasar instance
prasar = Prasar()

# Define and bind a synchronous event
def greet(name: str) -> str:
    return f"Hello, {name}!"

prasar.bind_event("greet", greet, str, return_type=str)

# Emit the event
result = prasar.emit("greet", "Alice")
print(result)  # Output: Hello, Alice!

# Define and bind an asynchronous event
async def fetch_data(url: str) -> dict:
    # Simulating async operation
    return {"data": "Some data from " + url}

prasar.bind_async_event("fetch", fetch_data, str, return_type=dict)

# Emit the async event
import asyncio
result = asyncio.run(prasar.async_emit("fetch", "https://example.com"))
print(result)  # Output: {'data': 'Some data from https://example.com'}
```

## 🌈 Logging

Prasar includes a custom logging module with colorful output:

```python
from prasar_logger import Logger

logger = Logger("MyLogger").get_logger()
logger.info("✅ This is an info message")
logger.error("❌ This is an error message")
```

## 📘 API Reference

### Prasar Class


| Method | Description |
|----------|----------|
| bind_event() | Binds a synchronous event |
| bind_async_event() | Binds an asynchronous event |
| emit() | Emits a synchronous event |
| async_emit() | Emits an asynchronous event |


### Logger Class

| Method | Description |
|----------|----------|
| __init__() | Initializes a new Logger instance |
| get_logger() |Returns the configured logger object |

For detailed API documentation, please visit our API Reference.

## 🤝 Contributing

We welcome contributions! Please see our Contribution Guidelines for more details.

## 📄 License

This project is licensed under the [MIT License](LICENSE). See the LICENSE file for details.

## 🙏 Acknowledgements
* Thanks to all our contributors and users!
* Inspired by various event handling systems in the Python ecosystem.

<div align="center">
Made with ❤️ by Abhishek Mishra

⭐ Star us on GitHub | 🐦 Follow us on [Instagram](https://www.instagram.com/mishrabroshan)
</div>