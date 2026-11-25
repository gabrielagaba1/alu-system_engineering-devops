# Firewall

## Project Overview
This project covers network security and packet filtering using the Uncomplicated Firewall (UFW) in an Ubuntu Linux environment. The objective is to secure web servers by implementing a default-deny policy for incoming connections while explicitly whitelisting authorized communication ports.

## Requirements
- Allowed editors: `vi`, `vim`, `emacs`
- Interpreted on Ubuntu 20.04 / 22.04 / 24.04 LTS
- All bash scripts must be executable
- Scripts must pass `shellcheck` (version 0.7.0) without errors
- All scripts start with `#!/usr/bin/env bash`

## Tasks

### 0. Block all incoming traffic but
- File: `0-block_all_incoming_traffic_but`
- Configure `ufw` on `web-01` to:
  - Block all incoming traffic by default
  - Allow all outgoing traffic by default
  - Allow incoming TCP on port `22` (SSH)
  - Allow incoming TCP on port `80` (HTTP)
  - Allow incoming TCP on port `443` (HTTPS SSL)
