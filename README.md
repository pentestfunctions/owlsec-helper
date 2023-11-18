
# 🦉 OwlSec Toolkit

![Python](https://img.shields.io/badge/language-Python-blue.svg) ![Penetration Testing](https://img.shields.io/badge/category-Penetration%20Testing-brightgreen.svg)

## 📖 Project Description

OwlSec Toolkit is a Python package designed to streamline and automate various penetration testing tasks. It offers a comprehensive, modular approach for cybersecurity professionals and enthusiasts, focusing on passive techniques with future expansions planned.

## ✨ Features

- 🌐 **Subdomain Enumeration**: Retrieve and display subdomains and interesting URLs from archives.
- 🌍 **Port Scanning**: Identify open TCP and UDP ports.
- 💻 **Web Server Identification**: Check for alternative web servers on identified ports.
- 📁 **Common Files & Directories Discovery**: Check for common files and directories on each identified web server.
- 🔐 **Login Forms Discovery**: Identify possible login forms and display their parameters.
- 🛡️ **SSL Certificate Checker**: Analyze and display SSL certificate details for a domain.

## 🚀 Installation

```bash
# You may need to manually download HTTPx
# https://github.com/projectdiscovery/httpx/releases/download/v1.3.5/httpx_1.3.5_linux_386.zip
# Follow these steps if not using pip as root:
wget https://github.com/projectdiscovery/httpx/releases/download/v1.3.5/httpx_1.3.5_linux_386.zip
unzip httpx_1.3.5_linux_386.zip
chmod +x httpx
mv httpx /home/kali/.local/lib/python3.11/site-packages/owlsec/scripts/pentesting/
pip install owlsec
```

## 📚 Usage

### As a Standalone Script

```bash
python3 main.py
# Follow the on-screen prompts
```

### As a Library

```python
from owlsec import (
    get_subdomains_and_urls, 
    run_httpx_for_domain, 
    get_file_details,
    get_burp_responses,
    port_scan,
    SSLChecker
)
# Use these functions in your scripts
```

## 📃 Functions and Descriptions

- `print_interesting_urls_and_subdomains(domain)`: Prints interesting URLs and subdomains.
- `print_port_scan_results(domain)`: Prints port scan results.
- `print_httpx_results(domain)`: Prints HTTPx results.
- `print_file_details(domain)`: Prints file and directory details.
- `print_login_forms(domain)`: Prints potential login forms.
- `check_and_print_ssl_status(domain)`: Checks and prints SSL status.

## ⚠️ Disclaimer

This tool is intended for educational and legal penetration testing purposes only. The developers assume no responsibility for any misuse of this toolkit.
