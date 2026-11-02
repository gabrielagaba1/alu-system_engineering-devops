# ALU System Engineering - DevOps

Bash scripts and configuration files for the ALU systems engineering projects.

## 0x0B. SSH

Covers SSH configuration and secure connections to remote servers using private keys.

### 0. Use a private key

`ssh/0-use_a_private_key` connects to a server with SSH, using the private key at `~/.ssh/school` and the `ubuntu` user.

```bash
./0-use_a_private_key
```

## Web server

### 0. Transfer a file to your server

`web_server/0-transfer_file` copies a file to a remote server over SCP.

```bash
./0-transfer_file PATH_TO_FILE IP USERNAME PATH_TO_SSH_KEY
```

### 1. Install nginx web server

`web_server/1-install_nginx_web_server` configures a new Ubuntu machine so that:

* nginx is installed,
* it listens on port 80,
* `GET /` returns a page containing `Holberton School`.

```bash
# on the server, as root
./1-install_nginx_web_server

# from anywhere
curl http://<server-ip>/
```

The script uses `service` to start and restart nginx, never `systemctl`. It is safe to run more than once, and it ends by fetching its own page with `curl` so a failure is loud instead of silent.

## Requirements

- Scripts run on Ubuntu.
- Bash scripts begin with `#!/usr/bin/env bash`.
- The second line of every Bash script explains its purpose.
- All Bash scripts are executable.
- All files use LF line endings and end with a newline (enforced by `.gitattributes`).
