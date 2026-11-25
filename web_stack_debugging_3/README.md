# Web stack debugging #3

## Project Overview
This project focuses on debugging an Apache 500 Internal Server Error in a WordPress LAMP stack using `strace` to trace system calls and determine where the application crashes. The fix is automated using a Puppet manifest.

## Requirements
- Interpreted on Ubuntu 14.04 LTS
- All files end with a newline
- A `README.md` file at the root of the project folder is mandatory
- Puppet manifests pass puppet-lint version 2.1.1 without errors
- Puppet manifests first line must be a comment explaining what the manifest does
- Files end with `.pp` extension
- Checked with Puppet v3.4

## Tasks

### 0. Strace is your friend
- File: `0-strace_is_your_friend.pp`
- Fixes the typo in `/var/www/html/wp-settings.php` where `.phpp` was used instead of `.php`.
