# Privilege Escalation Cheat Sheet

Checklists and commands for elevating privileges.

## Linux
- **Check OS and Kernel**: `uname -a`, `cat /etc/os-release`.
- **Sudo Permissions**: `sudo -l`.
- **SUID Binaries**: `find / -perm -u=s -type f 2>/dev/null`.
- **Automated Tools**:
  - `linpeas.sh`
  - `linux-exploit-suggester.sh`

## Windows
- **System Information**: `systeminfo`, `wmic qfe get Caption,Description,HotFixID,InstalledOn`.
- **User Privileges**: `whoami /priv`.
- **Scheduled Tasks**: `schtasks /query /fo LIST /v`.
- **Automated Tools**:
  - `winPEAS.exe`
  - `PowerUp.ps1`

## Common Paths
- Check config files for hardcoded passwords.
- Look for sensitive files in `/root`, `/home`, `C:\Users\Administrator`.
