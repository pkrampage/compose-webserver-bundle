# compose-webserver-bundle
A Docker Compose configuration that sets up a lightweight and powerful webserver environment with:

- **Nginx Proxy Manager** – for managing reverse proxies with SSL support
- **Portainer** – for Docker container management via web UI
- **Filebrowser (hurlenko/image)** – for browsing and managing files in a simple interface

## Features

- Easy setup using `docker-compose`
- Centralized management for web server, containers, and files
- Built-in SSL support via Nginx Proxy Manager
- Clean and modular configuration

## Services

| Service              | Description                                      | Port         |
|----------------------|--------------------------------------------------|--------------|
| Nginx Proxy Manager  | Reverse proxy with SSL & UI                      | 81, 443, 80  |
| Portainer            | Docker management UI                             | 9000         |
| Filebrowser          | Web-based file manager using hurlenko/filebrowser| 8080         |

## Getting Started

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/compose-webserver-bundle.git
   cd compose-webserver-bundle

2. Create required volumes and start the containers:
   ```bash
     docker-compose up -d

3. Access services:
- Nginx Proxy Manager: http://localhost:81
- Portainer: http://localhost:9000
- Filebrowser: http://localhost:8080

## Requirements
- Docker
- Docker Compose
