# Web Server

Bash scripts for managing web servers.

## 0. Transfer a file to your server

`0-transfer_file` transfers a file from a local machine to a remote server using SCP.

```bash
./0-transfer_file PATH_TO_FILE IP USERNAME PATH_TO_SSH_KEY
```

The script accepts the file path, server IP address, SSH username and private key path. It copies the file to the remote user's home directory and disables strict host key checking.

## 1. Install nginx web server

`1-install_nginx_web_server` configures a new Ubuntu machine from scratch:

1. waits for the apt lock a freshly booted machine is still holding, then installs nginx (and curl, used for the final check),
2. writes a page containing `Holberton School` to the web root,
3. makes sure a default site listens on port 80 and points at that root,
4. validates the configuration, then restarts nginx with `service` (no `systemctl`),
5. fetches `http://127.0.0.1/`, retries for a few seconds, and exits non-zero unless the page comes back.

If a step cannot be completed the script stops with the reason (`nginx is not installed`, `The nginx configuration test failed`, `Port 80 is not serving the page`) instead of failing silently.

```bash
# on the server, as root
./1-install_nginx_web_server

# verify, from the server or from your machine
curl http://127.0.0.1/
curl -sI http://127.0.0.1/    # expect HTTP/1.1 200 OK and a Server: nginx header
```

It can be run twice without harm. Nginx logs are in `/var/log/nginx/`.

## Line endings

Every file is stored with LF endings (see `.gitattributes`). A script saved with CRLF fails on Ubuntu with `bad interpreter: /usr/bin/env bash^M`.
