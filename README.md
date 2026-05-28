# Network Diagnostics Dashboard 📊

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-✓-000000?logo=flask)](https://flask.palletsprojects.com/)
[![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-✓-06B6D4?logo=tailwindcss)](https://tailwindcss.com/)
[![Chart.js](https://img.shields.io/badge/Chart.js-✓-FF6384?logo=chartdotjs)](https://www.chartjs.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> 全栈网络诊断 Web 应用 — Flask 后端 + 响应式前端，监控 WSL 系统健康与网络连通性。
> Full-stack network diagnostics web app built with Flask + AI-assisted development (Hermes Agent + DeepSeek V4).

## 功能 / What It Does

| 功能 Feature | 说明 Description |
|-------------|-----------------|
| 📊 **系统状态** | WSL 宿主机指标（uptime, CPU, 内存, 磁盘）/ System metrics |
| 🌐 **连通性检测** | 常用站点 Ping & HTTP 可达性 / Connectivity check |
| 🔌 **端口扫描** | 检测远程 TCP 端口是否开放 / Port scanner |
| 🕵️ **DNS 查询** | 域名解析到 IP 地址 / DNS lookup |
| 📡 **路由追踪** | 模拟 Traceroute 显示跳点 / Simulated traceroute |
| 🛡️ **代理状态** | 检查本地 mihomo 代理是否运行 / Proxy status |

## 技术栈 / Tech Stack

| 组件 Component | 技术 Technology |
|---------------|----------------|
| 后端 Backend | Python Flask |
| 前端 Frontend | HTML + Tailwind CSS + Chart.js |
| 开发工具 Dev Tools | Hermes Agent, DeepSeek V4 |
| 平台 Platform | WSL2 (Ubuntu 26.04) |

## 项目结构 / Project Structure

```
net-diag-demo/
├── app.py              # Flask 应用入口 / Application entry point
├── requirements.txt    # Python 依赖 / Dependencies
├── static/             # 静态资源 / Static assets
├── templates/
│   └── index.html      # 主 Dashboard 界面 / Main dashboard UI
└── README.md
```

## 快速开始 / Quick Start

```bash
pip install -r requirements.txt
python app.py
# 浏览器打开 / Open: http://localhost:5001
```

## API 接口 / API Endpoints

| 接口 Endpoint | 方法 Method | 说明 Description |
|--------------|------------|-----------------|
| `/api/system` | GET | 系统指标 / System metrics |
| `/api/connectivity` | GET | 站点可达性 / Site reachability |
| `/api/port-check` | POST | TCP 端口检测 `{host, port}` / Port check |
| `/api/dns-lookup` | POST | DNS 解析 `{domain}` / DNS resolution |
| `/api/proxy-status` | GET | 代理运行状态 / Proxy status |

## 使用场景 / Use Cases

### 1. 日常网络健康检查

打开 Dashboard 一眼看到系统资源和网络连通性。适合每天开工前快速确认开发环境正常。

### 2. 远程服务故障排查

API 或数据库连不上时，用端口扫描检查远程端口、DNS 查询确认解析——一个页面判断问题出在本地网络、DNS 还是远端服务。

### 3. WSL 开发环境诊断

WSL 网络容易出问题（DNS 丢失、代理断开）。Dashboard 直接展示宿主机指标 + 代理状态，快速定位问题侧。

### 4. AI 辅助开发案例展示

作为 AI 辅助开发的完整示例，展示从零用对话生成全栈项目的过程。适合技术分享或面试演示。

---

### Quick Use Cases (EN)

- **Daily health check**: System resources + network status at a glance
- **Remote troubleshooting**: Port scan + DNS lookup — diagnose in one page
- **WSL diagnostics**: Host metrics + proxy status for quick WSL issue resolution
- **AI dev showcase**: Full-stack project built entirely through AI conversation

## 🤖 AI 驱动开发 / Built With AI

本项目完全通过 **Hermes Agent + DeepSeek V4** 对话生成与迭代优化：
- 生成 Flask 后端骨架
- 设计交互式 Dashboard 界面
- 添加网络诊断功能
- 调试和测试每个功能
- 编写项目文档

> Submitted as part of Xiaomi MiMo 100T Token Grant for Builders application.

## Author

Wang Jiong (王炯) — Network Engineering student, cloud computing enthusiast.

## License

MIT
