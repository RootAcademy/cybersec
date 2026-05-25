# Root Red Team

**Multi-Distro Cybersecurity Tools Installer**  
*By Root Academy*

---

## Overview

Root Red Team is a powerful, interactive bash-based installer designed for cybersecurity professionals and penetration testers. It automates the installation, removal, and management of hundreds of security tools across multiple Linux distributions — all from a single, unified interface.

---

## Supported Distributions

| Distribution        | Package Manager | Status     |
|---------------------|-----------------|------------|
| Kali Linux          | apt             | Full       |
| Arch / BlackArch    | pacman          | Full       |
| Debian / Ubuntu     | apt             | Full       |
| Parrot OS           | apt             | Full       |
| Fedora / RHEL       | dnf / yum       | Full       |
| CentOS / Rocky      | dnf / yum       | Full       |
| openSUSE            | zypper          | Full       |

---

## Features

| Feature                        | Description                                                  |
|--------------------------------|--------------------------------------------------------------|
| Auto Distro Detection          | Automatically detects your Linux distribution and configures the correct package manager |
| Category-Based Installation    | Install only the tools you need by selecting specific categories |
| Full Install Mode              | Install all supported tools in one command                   |
| Tool Removal                   | Clean uninstall of any installed category or individual tool |
| Git Tool Management            | Clone, update, and remove tools installed from GitHub        |
| Auto Update (Git Tools)        | Update all git-based tools with a single option              |
| Backup & Restore               | Backup and restore all tool configurations                   |
| Docker Support                 | Pull pre-built pentest Docker images                         |
| BlackArch Repo Setup           | Automatically configures the BlackArch repository on Arch    |
| Alias Setup                    | Adds useful shell aliases for common security commands       |
| Dependency Checker             | Checks and installs Java, Node.js, Ruby, and Docker          |
| Disk Space Check               | Verifies available disk space before installation            |
| Logging                        | All actions are logged with timestamps                       |
| Interactive Animated UI        | Spinners, progress bars, and typing effects                  |

---

## Tool Categories

| # | Category                  | Example Tools                                      |
|---|---------------------------|----------------------------------------------------|
| 1 | Information Gathering     | nmap, masscan, theharvester, dnsrecon, sublist3r   |
| 2 | Vulnerability Analysis    | nikto, lynis, openvas, sqlmap, wapiti              |
| 3 | Web Application Testing   | burpsuite, gobuster, ffuf, wfuzz, dirsearch        |
| 4 | Exploitation Frameworks   | metasploit, routersploit, exploitdb, commix        |
| 5 | Password Cracking         | hashcat, john, hydra, medusa, crunch, SecLists     |
| 6 | Wireless / Bluetooth      | aircrack-ng, kismet, wifite, bully, reaver         |
| 7 | Sniffing & Spoofing       | wireshark, bettercap, responder, mitmproxy, scapy  |
| 8 | Post-Exploitation & C2    | evil-winrm, chisel, ligolo-ng, bloodhound, impacket|
| 9 | Reverse Engineering       | ghidra, radare2, gdb, peda, frida, binwalk         |
|10 | Digital Forensics         | autopsy, volatility3, sleuthkit, foremost, dc3dd   |
|11 | OSINT & Social Engineering| spiderfoot, sherlock, maltego, gophish, holehe     |
|12 | Database Assessment       | sqlmap, sqlninja, redis-tools, postgresql-client   |
|13 | Hardware / RFID / SDR     | gnuradio, hackrf, rtl-sdr, bladerf, ubertooth      |
|14 | Cloud Security            | pacu, ScoutSuite, awscli, cloudscraper             |
|15 | Mobile Security           | apktool, dex2jar, jadx, frida-tools, objection     |

---

## Requirements

- Linux-based OS (see supported distributions above)
- Root / sudo privileges
- Internet connection
- Minimum 5 GB free disk space (recommended)
- `git`, `curl`, `bash` installed

---

## Installation & Usage

### Quick Start

```bash
git clone https://github.com/RootAcademy/cybersec.git
cd cybersec
chmod +x cybersec.sh
sudo bash cybersec.sh
```

### One-Line Install

```bash
sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/RootAcademy/cybersec/main/cybersec.sh)"
```

---

## Menu Options

| Key | Action                          |
|-----|---------------------------------|
| I   | Install Tools (with sub-menu)   |
| R   | Remove Tools                    |
| U   | Update all Git-based tools      |
| F   | Fix common issues               |
| B   | Backup configurations           |
| C   | Restore configurations          |
| D   | Pull Docker pentest images      |
| T   | Install Top 10 essential tools  |
| V   | Check for updates               |
| Q   | Exit                            |

---

## Install Modes

| Mode                         | Description                                                    |
|------------------------------|----------------------------------------------------------------|
| Auto-detect and Install ALL  | Detects distro and installs all categories automatically       |
| Select Categories            | Choose specific categories by number (e.g. `1,3,5`)           |
| Manual Distro + Categories   | Manually select distro then choose categories                  |
| Install EVERYTHING           | Full install including distro-specific meta-packages           |

---

## Post-Install Notes

```bash
# Initialize Metasploit database (first time)
msfdb init

# Apply shell aliases
source /root/.bashrc

# Add user to Wireshark group
usermod -aG wireshark $USER
```

---

## Logs

All actions are automatically logged to:

```
/tmp/rrt-YYYYMMDD-HHMMSS.log
```

---

## Community

Join the Root Academy community on WhatsApp:

[https://chat.whatsapp.com/C5HoSBCoVge0ha9B5subjG](https://chat.whatsapp.com/C5HoSBCoVge0ha9B5subjG)

---

## License

```
Copyright (c) 2026 Root Academy — All Rights Reserved.
Unauthorized modification or redistribution is not permitted.
```

---

## Disclaimer

This tool is intended for use in authorized penetration testing, security research, and educational environments only. The authors are not responsible for any misuse or damage caused by this tool. Always obtain proper authorization before testing any system.
