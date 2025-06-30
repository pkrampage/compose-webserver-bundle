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

2. Create .env file:

   ```bash
   NPM_DB_USER = db_username
   NPM_DB_PASSWORD = db_password
   NPM_DB_NAME = db_name

4. Echo uid and gid to .env file:
   ```bash
   echo "UID=$(id -u)" >> .env
   echo "GID=$(id -g)" >> .env

5. Create required volumes and start the containers:
   ```bash
   docker-compose up -d

6. An 'admin' password is automatically generated. To find it, use this method:
   ```bash
   docker logs filebrowser-container-name
   ```
   
   ```bash
   2025/06/30 03:01:18 Warning: filebrowser.db can't be found. Initialing in /config/
   2025/06/30 03:01:18 Using database: /config/filebrowser.db
   2025/06/30 03:01:19 No config file used
   2025/06/30 03:01:19 Randomly generated password for user 'admin': generated-password

7. Access services:
- Nginx Proxy Manager: http://localhost:81
- Portainer: http://localhost:9000
- Filebrowser: http://localhost:8080

## Requirements
- Docker
- Docker Compose
