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

## 使用场景

### 1. 日常网络健康检查

打开 Dashboard，一眼看到系统资源（CPU、内存、磁盘）和网络连通性状态。适合每天上班后快速确认开发环境正常，避免工作中才发现网络不通。

### 2. 远程服务故障排查

某个 API 或数据库突然连不上时，用端口扫描检查远程端口是否开放，用 DNS 查询确认域名解析是否正常。一个页面就能判断问题是出在本地网络、DNS 还是远端服务。

### 3. WSL 开发环境诊断

WSL 环境下网络配置容易出问题（DNS 丢失、代理断开等）。Dashboard 直接展示 WSL 宿主机的系统指标，结合代理状态检查，快速定位是 Windows 侧还是 WSL 侧的问题。

### 4. 演示与教学

作为 AI 辅助开发的完整示例，展示从零到一用对话生成全栈项目的过程。适合在技术分享、面试或团队内推广 AI 工具时进行现场演示。

## Built With AI

This entire project was generated and refined through conversation with **Hermes Agent** running on **DeepSeek V4**. The agent:
- Generated the Flask backend skeleton
- Designed the interactive dashboard UI
- Added network diagnostic functions
- Debugged and tested each feature
- Created the project documentation

> Submitted as part of Xiaomi MiMo 100T Token Grant for Builders application.
