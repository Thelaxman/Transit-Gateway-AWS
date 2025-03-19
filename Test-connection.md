
# Ubuntu Script to Switch to Root, Update Packages, and Ping Server

This script automates the process of switching to the root user, updating the system packages, and pinging a server located in a different AWS region.

## Script
```bash
#!/bin/bash

# Switch to root user
if [ "$EUID" -ne 0 ]; then
  echo "Switching to root user..."
  sudo su
fi

# Update package list and upgrade packages
echo "Updating package list and upgrading packages..."
apt update && apt upgrade -y

# Ping a server in a different region (replace with actual IP or domain)
SERVER_IP="198.51.100.42"
echo "Pinging server at $SERVER_IP..."
ping -c 4 $SERVER_IP

echo "Script completed."
