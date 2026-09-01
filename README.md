# Keylogger

Educational keylogger for security research demonstrating input capture, window tracking, and C2 delivery techniques.

## Overview

This project provides an educational keylogger implementation designed for security research and learning purposes. It demonstrates fundamental concepts in input monitoring, system tracking, and secure coding practices. The tool is intentionally limited to synthetic environments and operates on the local machine only.

**Critical Safety Notice:** This keylogger is provided **strictly for educational and authorized security research purposes only**.

- **Never deploy** this keylogger on any system you do not own or have explicit written permission to monitor
- **All operations are strictly local** to the machine running the tool
- **No network transmission** occurs without explicit configuration
- **This tool must only be used** in controlled lab environments or with proper authorization
- **Unauthorized use** of keylogging software may violate federal and state laws (CFAA, state privacy laws, workplace monitoring laws)
- **Always obtain explicit written permission** before deploying any input monitoring software

## Features

### Keyboard Event Capture

- **Microsecond-precision timestamps** for accurate timing analysis
- **Global keyboard event monitoring** across active sessions
- **Key press/release tracking** with character identification
- **Modifier key tracking** (Shift, Ctrl, Alt, Caps Lock)

### Active Window Tracking

- **Cross-platform support**: Windows, macOS, and Linux
- **Window title tracking** with timestamps
- **Active process identification**
- **Window focus change detection**

### Configurable Log Management

- **Size-limited log rotation** (default 5MB) to prevent excessive log growth
- **Thread-safe log operations** with proper resource locking
- **Automatic timestamping** of all captured events
- **Structured log format** for easy analysis

### Runtime Control

- **F9 hotkey** to pause and resume capture at any time
- **Ctrl+C** for clean exit and graceful shutdown
- **Configuration via environment variables** for customization

## Installation

### Requirements

- **Python 3.10 or higher**
- **Operating system**: Windows, macOS, or Linux
- **Standard library modules only** (no external dependencies beyond those listed in requirements.txt)

### Setup

```bash
# Clone the repository
git clone https://github.com/OpKnock/keylogger.git
cd keylogger

# Install dependencies
uv sync

# Verify installation
python keylogger.py --help
```

### Run the Keylogger

```bash
python keylogger.py
```

- Press **F9** to toggle capture on/off
- Press **Ctrl+C** to stop the program and exit cleanly

The keylogger will begin capturing keyboard events immediately upon launch. Captured data is stored in local log files with automatic rotation when the size limit is reached.

## Legal and Ethical Notes

### Authorized Research Only

This tool is designed exclusively for authorized security research. Key principles:

- **Only deploy on systems you own or administer**
- **Obtain explicit written permission** from all stakeholders before deployment
- **Never deploy on production systems** without proper authorization
- **Report any discovered security findings** to the appropriate system owners

### Legal Compliance

- Unauthorized installation of keylogging software is illegal in most jurisdictions
- Federal laws (CFAA, ECPA) and state privacy laws regulate monitoring software
- Workplace monitoring requires employee consent and compliance with local regulations
- **Always consult legal counsel** before deploying any input monitoring tools

### Educational Value

Understanding keylogger architecture helps security teams:

- Design defenses against keylogging malware
- Implement proper input monitoring controls
- Educate users about monitoring detection
- Build awareness of surveillance risks

### Responsible Disclosure

- Report any security concerns to the project maintainers
- Follow responsible disclosure practices for any discovered vulnerabilities
- Ensure all testing is conducted in authorized environments only

## License

AGPL 3.0 - This project is free software: you can redistribute it and/or modify it under the terms of the GNU Affero General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

You should have received a copy of the AGPLv3 license along with this program. If not, see <https://www.gnu.org/licenses/>.