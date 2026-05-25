# Network Diagnostics Dashboard

A full-stack network diagnostics web application built with **Flask + AI-assisted development** (Hermes Agent + DeepSeek V4).

## What It Does

- 📊 **System Status** — WSL host metrics (uptime, CPU, memory, disk)
- 🌐 **Connectivity Check** — Ping & HTTP reachability to common sites
- 🔌 **Port Scanner** — Check if a remote port is open (TCP)
- 🕵️ **DNS Lookup** — Resolve domain names to IP addresses
- 📡 **Traceroute (simulated)** — Show routing hops to a target
- 🛡️ **Proxy Status** — Check if local proxy (mihomo) is running

## Tech Stack

| Component | Technology |
|-----------|-----------|
| Backend | Python Flask |
| Frontend | HTML + Tailwind CSS + Chart.js |
| Dev tools | Hermes Agent, DeepSeek V4 |
| Platform | WSL2 (Ubuntu 26.04) |

## Project Structure

```
net-diag-demo/
├── app.py              # Flask application entry point
├── requirements.txt    # Python dependencies
├── static/             # Static assets (future use)
├── templates/
│   └── index.html      # Main dashboard UI
└── README.md           # This file
```

## Quick Start

```bash
# Install dependencies
pip install -r requirements.txt

# Run the app
python app.py

# Open in browser
# http://localhost:5001
```

## API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/system` | GET | System metrics (uptime, CPU, memory, disk) |
| `/api/connectivity` | GET | Check reachability to well-known sites |
| `/api/port-check` | POST | Check if a TCP port is open (`{host, port}`) |
| `/api/dns-lookup` | POST | DNS resolution (`{domain}`) |
| `/api/proxy-status` | GET | Check if mihomo proxy is running |

## Built With AI

This entire project was generated and refined through conversation with **Hermes Agent** running on **DeepSeek V4**. The agent:
- Generated the Flask backend skeleton
- Designed the interactive dashboard UI
- Added network diagnostic functions
- Debugged and tested each feature
- Created the project documentation

> Submitted as part of Xiaomi MiMo 100T Token Grant for Builders application.
