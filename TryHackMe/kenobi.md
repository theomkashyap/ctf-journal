# Kenobi — Strengthening My Service Enumeration & Linux Privilege Escalation Skills

**Platform:** TryHackMe  
**Room:** Kenobi  
**Category:** SMB Enumeration, FTP Exploitation, Linux Privilege Escalation  
**Date:** 25 July 2026

After completing Vulnversity, I wanted to continue improving my Linux penetration testing skills by exploring network services beyond traditional web applications. Kenobi felt like the perfect next step because it combined SMB enumeration, NFS enumeration, exploitation of a vulnerable FTP service, SSH access, and Linux privilege escalation into a single challenge.

I started by scanning the target to identify the available services. The scan revealed several open ports, including SMB, FTP, SSH, and NFS. Instead of immediately attempting exploitation, I spent time enumerating each service to understand how they were connected. While exploring the anonymous SMB share, I discovered useful information that revealed details about the FTP service and the target user's SSH key.

After spending some time gathering information, I identified a vulnerable version of ProFTPD and researched publicly available exploits. Using the vulnerable mod_copy module, I copied the target user's private SSH key to an accessible location. By mounting the exposed NFS share, I recovered the private key and successfully gained SSH access to the system.

Once I had access, I explored the Linux filesystem, searched for privilege escalation opportunities, and became more comfortable identifying insecure SUID binaries. Along the way, I also learned how tools like SMBClient, Searchsploit, and NFS can work together during a penetration test. Discovering a custom SUID binary and abusing the PATH environment variable to execute commands with root privileges was one of the biggest takeaways from this room.

Compared to Vulnversity, this room focused less on web exploitation and more on understanding how multiple network services can expose different pieces of information that eventually lead to complete system compromise. Every stage depended on careful enumeration, and it reinforced the idea that connecting small discoveries is often more valuable than relying on a single exploit.

## Tools I Used

- Nmap
- SMBClient
- Searchsploit
- Netcat
- NFS
- SSH
- Strings
- Linux Terminal

## What I Learned

- Enumeration should always come before exploitation.
- SMB shares can expose valuable information during reconnaissance.
- NFS exports may unintentionally reveal sensitive files.
- Public exploit databases like Searchsploit are useful for identifying known vulnerabilities.
- ProFTPD's mod_copy vulnerability can lead to unauthorized file access.
- PATH variable manipulation is an effective privilege escalation technique when privileged binaries execute commands insecurely.
- Linux privilege escalation should always begin with systematic enumeration.
- Patience and careful observation are just as important as technical knowledge.

## Final Thoughts

This room strengthened many of the concepts I learned in Vulnversity while introducing me to SMB enumeration, NFS shares, and PATH variable manipulation for privilege escalation. More than anything, it reminded me that successful penetration testing isn't about finding one big vulnerability—it's about understanding the target, connecting small pieces of information, and approaching every stage methodically.

Looking forward to building on these skills with more CTF challenges.
