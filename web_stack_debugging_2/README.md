# Web stack debugging #2

## Project Overview
This project covers running software with restricted permissions (running as an unprivileged user instead of root) to minimize attack surfaces. It includes executing commands as another user and reconfiguring Nginx to run under the `nginx` user context on unprivileged port 8080.

## Requirements
- Interpreted on Ubuntu 14.04 LTS
- All files end with a newline
- A `README.md` file at the root of the project folder is mandatory
- All Bash scripts must be executable
- Scripts must pass Shellcheck without errors
- First line: `#!/usr/bin/env bash`
- Second line: comment explaining what the script does

## Tasks

### 0. Run software as another user
- File: `0-iamsomeoneelse`
- Executes `whoami` under the user passed as an argument.

### 1. Run Nginx as Nginx
- File: `1-run_nginx_as_nginx`
- Configures Nginx to run under the `nginx` user listening on port 8080.
