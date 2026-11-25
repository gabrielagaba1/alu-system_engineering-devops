# Web stack debugging #0

## Project Overview
This project introduces Docker-based web stack debugging. The task involves inspecting a container with a non-responsive web server, diagnosing the root cause, and providing a non-interactive Bash script to bring the web service to an operational state.

## Requirements
- Allowed editors: `vi`, `vim`, `emacs`
- Interpreted on Ubuntu 14.04 LTS
- All files end with a newline
- A `README.md` file at the root of the project folder is mandatory
- All Bash scripts must be executable
- Scripts must pass Shellcheck without errors
- First line of all scripts: `#!/usr/bin/env bash`
- Second line: comment explaining what the script does

## Tasks

### 0. Give me a page!
- File: `0-give_me_a_page`
- Fixes Apache service inside the Docker container so that querying `curl 0:8080` returns the default page containing `Hello Holberton`.
