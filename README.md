# Keylogger

Educational keylogger for security research demonstrating input capture, window tracking, and C2 delivery techniques.

## Overview

This project provides an educational keylogger implementation designed for security research and learning purposes. It demonstrates fundamental concepts in input monitoring, system tracking, and secure coding practices. The tool is intentionally limited to synthetic environments and operates on the local machine only.

## Features

- **Keyboard event capture** with microsecond-precision timestamps for accurate timing analysis
- **Active window tracking** across Windows, macOS, and Linux platforms
- **Configurable log rotation** with size limits (default 5MB) to prevent excessive log growth
- **Runtime control** via F9 hotkey to pause and resume capture at any time
- **Secure log handling** with thread-safe operations and proper resource locking
- **Clean exit handling** with Ctrl+C support for graceful shutdown

## Installation

```bash
# Clone the repository
git clone https://github.com/OpKnock/keylogger.git
cd keylogger

# Install dependencies
uv sync

# Run the keylogger
python keylogger.py
```

## Usage

- Press **F9** to toggle capture on/off
- Press **Ctrl+C** to stop the program and exit cleanly

The keylogger will begin capturing keyboard events immediately upon launch. Captured data is stored in local log files with automatic rotation when the size limit is reached.

## Safety and Ethics

**Important:** This project is designed exclusively for authorized security research and educational purposes. 

- Never deploy keyloggers on systems you do not own or have explicit permission to monitor
- All operations are local to the machine running the tool
- No network transmission occurs without explicit configuration
- This tool should only be used in controlled lab environments or with proper authorization

## Requirements

- Python 3.10 or higher
- Operating system: Windows, macOS, or Linux
- Standard library modules only (no external dependencies beyond those listed in requirements.txt)

## Learning Resources

This project includes comprehensive learning materials:

| Module | Topic |
|--------|-------|
| [00 - Overview](learn/00-OVERVIEW.md) | Prerequisites, setup, and quick start guide |
| [01 - Concepts](learn/01-CONCEPTS.md) | Keyboard event architecture, input monitoring techniques, and security implications |
| [02 - Architecture](learn/02-ARCHITECTURE.md) | System design, module layout, and data flow diagrams |
| [03 - Implementation](learn/03-IMPLEMENTATION.md) | Complete code walkthrough with explanations for every component |
| [04 - Challenges](learn/04-CHALLENGES.md) | Extension ideas and exercises for deepening understanding |

## License

AGPL 3.0 - This project is free software: you can redistribute it and/or modify it under the terms of the GNU Affero General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

You should have received a copy of the AGPLv3 license along with this program. If not, see <https://www.gnu.org/licenses/>.