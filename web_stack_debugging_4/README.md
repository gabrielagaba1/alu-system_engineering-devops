# Web stack debugging #4

## Project Overview
This project addresses benchmarking and high-concurrency issues with Nginx under stress testing using ApacheBench (`ab`). Under heavy load, requests fail due to low operating system file descriptor limits (`ULIMIT`). The fix is automated using Puppet.

## Requirements
- Interpreted on Ubuntu 14.04 LTS
- All files end with a newline
- A `README.md` file at the root of the project folder is mandatory
- Puppet manifests pass puppet-lint version 2.1.1 without errors
- Puppet manifests first line must be a comment explaining what the manifest does
- Files end with `.pp` extension
- Checked with Puppet v3.4

## Tasks

### 0. Sky is the limit, let's bring that limit higher
- File: `0-the_sky_is_the_limit_not.pp`
- Increases the Nginx ULIMIT limit in `/etc/default/nginx` and restarts the service.
