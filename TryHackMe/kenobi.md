# Kenobi — SMB Enumeration, ProFTPD Exploitation & Linux Privilege Escalation

**Platform:** TryHackMe  
**Room:** Kenobi  
**Category:** SMB Enumeration, FTP Exploitation, Linux Privilege Escalation  
**Date:** 25 July 2026

Kenobi introduced me to a complete Linux penetration testing workflow that combined service enumeration, SMB share discovery, exploitation of a vulnerable ProFTPD service, and Linux privilege escalation. The room demonstrated how multiple services can work together to expose a complete attack path instead of relying on a single vulnerability.

---

## Tools Used

- Nmap
- SMBClient
- Searchsploit
- Netcat
- SSH
- Mount
- Strings
- Linux Terminal

---

## What I Learned

- Enumerated SMB shares to discover sensitive information.
- Explored NFS exports to access remote directories.
- Identified a vulnerable version of ProFTPD using version enumeration.
- Used public exploit research to understand the **mod_copy** vulnerability.
- Recovered an SSH private key and gained initial access to the target.
- Performed Linux post-exploitation enumeration.
- Identified a vulnerable SUID binary.
- Learned how PATH variable manipulation can lead to privilege escalation.

---

## Key Takeaways

- Enumeration should always come before exploitation.
- SMB and NFS services can unintentionally expose sensitive information.
- Public exploit databases are valuable during vulnerability research.
- Linux privilege escalation often begins with careful system enumeration.
- Misconfigured SUID binaries can lead to complete system compromise.

---

## Summary

Kenobi combined SMB enumeration, ProFTPD exploitation, SSH access, and Linux privilege escalation into a realistic penetration testing workflow. More importantly, it reinforced that successful exploitation depends on understanding the target, connecting information from multiple services, and approaching each stage methodically.
