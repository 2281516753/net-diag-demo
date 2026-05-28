# Network Diagnostics Dashboard 📊

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-✓-000000?logo=flask)](https://flask.palletsprojects.com/)
[![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-✓-06B6D4?logo=tailwindcss)](https://tailwindcss.com/)
[![Chart.js](https://img.shields.io/badge/Chart.js-✓-FF6384?logo=chartdotjs)](https://www.chartjs.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> [📖 中文版 / Chinese Version](README_CN.md)

Full-stack network diagnostics web app — Flask backend + responsive frontend, monitoring WSL system health and network connectivity. Built with AI assistance (Hermes Agent + DeepSeek V4).

## Features

| Feature | Description |
|---------|-------------|
| 📊 **System Status** | WSL host metrics (uptime, CPU, memory, disk) |
| 🌐 **Connectivity** | Ping & HTTP reachability to common sites |
| 🔌 **Port Scanner** | Check if a remote TCP port is open |
| 🕵️ **DNS Lookup** | Resolve domain names to IPs |
| 📡 **Traceroute** | Simulated traceroute with hop display |
| 🛡️ **Proxy Status** | Check if mihomo proxy is running |

## Tech Stack

| Component | Technology |
|-----------|-----------|
| Backend | Python Flask |
| Frontend | HTML + Tailwind CSS + Chart.js |
| Dev Tools | Hermes Agent, DeepSeek V4 |
| Platform | WSL2 (Ubuntu 26.04) |

## Quick Start

```bash
pip install -r requirements.txt
python app.py
# Open http://localhost:5001
```

## API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/system` | GET | System metrics |
| `/api/connectivity` | GET | Site reachability |
| `/api/port-check` | POST | TCP port check `{host, port}` |
| `/api/dns-lookup` | POST | DNS resolution `{domain}` |
| `/api/proxy-status` | GET | Proxy status |

## Use Cases

- **Daily check**: System resources + network status at a glance
- **Troubleshooting**: Port scan + DNS lookup — diagnose in one page
- **WSL diagnostics**: Host metrics + proxy status for quick issue resolution
- **AI dev showcase**: Full-stack project built entirely through AI conversation

## Built With AI

This project was generated and refined through conversation with **Hermes Agent** running on **DeepSeek V4**.

> Submitted as part of Xiaomi MiMo 100T Token Grant for Builders application.

## Author

Wang Jiong (王炯) — Network Engineering student.

## License

MIT