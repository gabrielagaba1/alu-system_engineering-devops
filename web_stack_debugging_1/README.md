# Web stack debugging #1

## Project Overview
This project focuses on debugging an Nginx web server configuration in an Ubuntu container environment where Nginx is failing to listen on port 80. The objective is to identify the port misconfiguration and write a minimal non-interactive Bash script to automate the fix.

## Requirements
- Allowed editors: `vi`, `vim`, `emacs`
- Interpreted on Ubuntu 20.04 LTS
- All files end with a newline
- A `README.md` file at the root of the project folder is mandatory
- All Bash scripts must be executable
- Scripts must pass Shellcheck without errors
- First line of all scripts: `#!/usr/bin/env bash`
- Second line: comment explaining what the script does
- Not allowed to use `wget`

## Tasks

### 0. Nginx likes port 80
- File: `0-nginx_likes_port_80`
- Reconfigures `/etc/nginx/sites-available/default` so that Nginx listens on port `80` across all active IPv4 addresses, and restarts the Nginx service.
