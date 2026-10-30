# Web Server

This directory contains Bash scripts for managing web servers.

## 0. Transfer a file to your server

The `0-transfer_file` script transfers a file from a local machine to a remote server using SCP.

Usage:

./0-transfer_file PATH_TO_FILE IP USERNAME PATH_TO_SSH_KEY

The script accepts the file path, server IP address, SSH username, and private key path. It transfers the file to the remote user's home directory and disables strict host key checking.
