# Core Stack (Homelab Tools)

This repository contains a Docker Compose stack for essential homelab infrastructure tools. It currently includes:

- [Portainer](https://www.portainer.io/) – Docker management GUI  
- [Uptime Kuma](https://github.com/louislam/uptime-kuma) – Self-hosted monitoring/status page  
- [NGINX](https://hub.docker.com/_/nginx) – Lightweight reverse proxy for routing internal services

## 📦 Setup Instructions

📁 Volumes

Container	Host Path
Portainer	/opt/docker-config/portainer:/data
Uptime Kuma	/opt/docker-config/uptime-kuma:/app/data

Ensure these folders exist and are writable.

🔐 Security Notes
Portainer should not be exposed to the internet directly. Use reverse proxy + HTTPS if remote access is needed.

All services run with restart: unless-stopped for reliability.

You can bind ports to 127.0.0.1 if using a reverse proxy or LAN-only access.

