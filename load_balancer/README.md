# Load Balancer

This project introduces web server redundancy and high availability by setting up HAProxy to distribute HTTP traffic across multiple backend web servers (web-01 and web-02) using a round-robin algorithm.

## Tasks

- **0-custom_http_response_header**: Configures Nginx on web-01 and web-02 to return the `X-Served-By` HTTP response header containing the server hostname.
- **1-install_load_balancer**: Automates the installation and configuration of HAProxy on lb-01.
