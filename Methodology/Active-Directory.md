# Active Directory (AD) Attack Methodology

Standard workflow for attacking Windows AD environments.

## 1. Enumeration
- **BloodHound**: Map out the network and relationships.
- **Enumerating Users/Groups**:
  ```bash
  netview.exe
  crackmapexec smb <IP> --users
  ```

## 2. Initial Access
- **Kerberoasting**: Requesting service tickets to crack offline.
- **AS-REP Roasting**: Attacking users with no pre-authentication required.
- **LLMNR/NBT-NS Poisoning**: Using `Responder`.

## 3. Lateral Movement
- **Pass-the-Hash (PtH)**: Using NTLM hashes instead of passwords.
- **Pass-the-Ticket (PtT)**: Using Kerberos tickets.
- **Remote Execution**: `psexec`, `wmiexec`, `smbexec`.

## 4. Privilege Escalation
- **Domain Admin Search**: Finding paths to become Domain Admin.
- **Exploiting Misconfigurations**: GPO abuse, ACL misconfigurations.
- **DCSync Attack**: Mimicking a Domain Controller to pull hashes.
