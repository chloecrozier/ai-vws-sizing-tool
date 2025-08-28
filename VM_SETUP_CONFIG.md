# VM Setup Configuration Guide

This document provides the prerequisite steps for setting up a VM with vGPU passthrough before deploying the AI vWS Sizing Advisor.

## Prerequisites

Before following the main [README.md](./README.md) deployment guide, ensure your VM is properly configured with the following setup steps.

## Network Configuration

Install network tools and configure network interface:

```bash
sudo apt install net-tools
ifconfig | grep inet
```

## SSH Server Setup

Install and configure SSH server for remote access:

```bash
sudo apt install openssh-server
sudo systemctl start ssh
sudo systemctl status ssh # Verify service is active and enabled
```

## Firewall Configuration

Disable UFW firewall (if not needed for your security requirements):

```bash
sudo systemctl disable ufw
sudo systemctl status ufw # Verify service is active but disabled
```

## SSH Key Generation

Generate SSH keys for secure authentication:

```bash
ssh-keygen -t ed25519 -C "chloecrozier@gmail.com" -f ~/.ssh/ccrozier-ai-vws
```

## SSH Configuration

Edit SSH configuration file:

```bash
sudo nano ~/.ssh/config
```

## Development Tools Installation

Install GitHub CLI and Git:

```bash
sudo apt install gh
sudo apt install git
```

## System Updates

Update the system packages:

```bash
sudo apt update
```

## Next Steps

After completing these VM setup steps, proceed to the main [README.md](./README.md) file to continue with the AI vWS Sizing Advisor deployment process.

## Important Notes

- Ensure your VM has vGPU passthrough properly configured before starting
- Verify all services are running as expected before proceeding to the main deployment
- These steps assume you have appropriate permissions and network access
- Adjust SSH key email and filename as needed for your environment