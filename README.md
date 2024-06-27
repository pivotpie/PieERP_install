# Unattended Install Script for PieERP
Unattended script for PieERP installation (Supports Versions 13, 14 and 15).

This is a no-interactive script for installing PieERP Versions 13, 14 and 15. You can set up either development or production with very minimal interaction.

# How To:
To use this script, follow these steps:

# Before Installation

Make sure you install the latest package versions by updating system packages if you are running this script on a fresh Ubuntu machine.

```
sudo apt update && sudo apt -y upgrade
```
and then reboot your machine 

# Installation:

1. Clone the Repo:
```
git clone https://github.com/pivotpie/PieERP_install.git
```
2. navigate to the folder:
```
cd PieERP_install
```
3. Make the script executable
```
chmod +x PieERP_install.sh
```
4. Run the script:
```
source PieERP_install.sh
```
# Compatibility

Ubuntu 24.04 LTS,
Ubuntu 23.04 LTS,
Ubuntu 22.04 LTS,
Ubuntu 20.04 LTS

Debian 10 (Buster),
Debian 11 (Bulls Eye)
Debian 12 (Bookworm)

# NOTE:

Version 15 Compatibility is set to Ubuntu 22.04 LTS and above and Debian 12 only. Lower versions are not supported for version 15 installation due to dependency issues

If you encounter spawn error on socketio when running bench restart, run the following commands:

```
bench setup socketio
bench setup supervisor
bench setup redis
sudo supervisorctl reload
```
This will fix the spawn error and all services will restart successfully.
