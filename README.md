# Pi-Hole Setup Script (NanoPi Zero2 / Ubuntu 24.04 Noble)

This script bootstraps a **set-and-forget Pi-Hole appliance** on a **NanoPi Zero2** running **Ubuntu 24.04 Noble**.

It is designed for a **fresh system install** and prepares the SBC for unattended operation, installs Pi-Hole, configures blocklists, and applies basic system hardening.

---

## Hardware Summary

- FriendlyElec NanoPi Zero2
- ARM Quad-Core Cortex-A53
- 2 GB RAM
- SanDisk High Endurance 64 GB microSD card

---

## Starting point (required)

Before running this script:

1. Download an **Ubuntu 24.04 Noble** image for NanoPi Zero2 from:
https://download.friendlyelec.com/NanoPiZero2

2. Flash the image to a **microSD** card using a tool such as Rufus.

3. Boot the NanoPi Zero2 using the flashed card.

4. Ensure you can **SSH into the system** and have access to the "pi" user account which has sudo privileges.

As documented by FriendlyElec, the default credentials are:
- **Username:** `pi`
- **Password:** `pi`

---

## What this script does

- Updates and upgrades the OS
- Installs required dependencies
- Installs and configures the firewall (ufw)
- Installs Pi-Hole
- Adds blocklists to Pi-Hole and updates Gravity
- Enables unattended OS updates

---

## Security assumptions

After running this script you should
- Change the default pi user password
- Configure SSH key-based authentication
- Disable password and root SSH login

---

## Usage
```bash
sudo bash install.sh
```