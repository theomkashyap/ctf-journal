# Brooklyn Nine-Nine — Strengthening My Enumeration & Linux Privilege Escalation Skills

**Platform:** TryHackMe  
**Room:** Brooklyn Nine-Nine  
**Category:** Enumeration, Credential Attacks, Steganography, Linux Privilege Escalation  
**Date:** 15 July 2026

After completing Dreaming, I wanted to continue improving my Linux penetration testing skills. Brooklyn Nine-Nine felt like the perfect next step because it combined service enumeration, credential discovery, password cracking, steganography, SSH access, and Linux privilege escalation into a single room.

I started by scanning the target to identify the available services. The scan revealed an FTP server, an SSH service, and a web application, so I spent time exploring each one instead of focusing on a single attack path. During enumeration, I discovered that the FTP server allowed anonymous access, which exposed useful information that later helped me identify a valid user account.

After spending some time gathering information, I used password cracking to recover valid credentials and eventually gained access to the target over SSH. While exploring the web application, I also encountered a steganography challenge where hidden information inside an image revealed another set of credentials. Unlike my previous rooms, this challenge showed me that the same machine can often be compromised through multiple attack paths, reinforcing the importance of exploring every possible avenue during an assessment.

Once I had access, I explored the Linux filesystem, searched for privilege escalation opportunities, and became more comfortable identifying misconfigured sudo permissions. Along the way, I learned how anonymous FTP access, Hydra, and steganography can all contribute to credential discovery, while GTFOBins demonstrated how common Linux utilities like **less** and **nano** can be abused for privilege escalation when they are improperly configured.

Compared to Dreaming, this room focused less on complex exploitation and more on understanding different attack paths. Every stage depended on careful enumeration, and it reinforced the idea that small findings collected throughout an assessment often lead to the biggest breakthroughs.

## Tools I Used

- Nmap
- FTP
- Hydra
- Stegcracker
- SSH
- GTFOBins
- Linux Terminal

## What I Learned

- Enumeration should always come before exploitation.
- Anonymous FTP shares can expose valuable information.
- Hydra is an effective tool for credential attacks when supported by good reconnaissance.
- Steganography can hide sensitive information inside seemingly harmless files.
- Multiple attack paths may exist for the same target.
- Reviewing sudo permissions is an essential part of Linux privilege escalation.
- GTFOBins is an excellent resource for understanding Linux privilege escalation techniques.
- Patience and careful observation are just as important as technical knowledge.

## Final Thoughts

This room strengthened many of the concepts I learned in Dreaming while introducing me to steganography and multiple attack paths. More than anything, it reminded me that successful penetration testing isn't about finding one big vulnerability—it's about understanding the target, connecting small pieces of information, and approaching every stage methodically.

Looking forward to building on these skills with more CTF challenges.
