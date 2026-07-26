# Brute It — Strengthening My Password Cracking & Linux Privilege Escalation Skills

**Platform:** TryHackMe  
**Room:** Brute It  
**Category:** Password Brute Forcing, Hash Cracking, Linux Privilege Escalation  
**Date:** 24 July 2026

After completing several Linux-focused rooms, I wanted to improve my understanding of password attacks and privilege escalation. Brute It felt like the perfect next step because it combined web enumeration, credential brute forcing, SSH access, password hash cracking, and Linux privilege escalation into a single challenge.

I started by scanning the target to identify the available services. The scan revealed an SSH service and a web server, so I explored the web application before moving on to further enumeration. Using directory enumeration, I discovered a hidden administrative panel that wasn't visible through normal browsing.

After spending some time gathering information, I used a dictionary attack to recover valid credentials for the admin panel. While exploring the application, I discovered an SSH private key that was protected with a passphrase. Instead of using it directly, I learned how to convert the key into a format compatible with John the Ripper and successfully recovered the passphrase, allowing me to gain SSH access to the target.

Once I had access, I explored the Linux filesystem, searched for privilege escalation opportunities, and became more comfortable analyzing user permissions. Along the way, I also learned how tools like Hydra, ssh2john, John the Ripper, and Hashcat can be used together during password recovery and credential attacks. Reading the shadow file through misconfigured sudo permissions and recovering the root password was one of the biggest takeaways from this room.

Compared to previous Linux rooms, Brute It focused more on password security and credential recovery rather than exploiting application vulnerabilities. Every stage depended on careful enumeration, effective password attacks, and understanding how weak credentials can ultimately lead to complete system compromise.

## Tools I Used

- Nmap
- Gobuster
- Hydra
- SSH
- ssh2john
- John the Ripper
- Hashcat
- Linux Terminal

## What I Learned

- Enumeration should always come before exploitation.
- Hidden web directories can expose administrative functionality.
- Dictionary attacks become highly effective when weak passwords are used.
- SSH private keys protected by weak passphrases can be cracked using ssh2joh and John the Ripper.
- Hashcat can be used to recover password hashes obtained during post-exploitation.
- Misconfigured sudo permissions can expose highly sensitive system files.
- Strong passwords and the principle of least privilege are essential for securing Linux systems.
- Patience and careful observation are just as important as technical knowledge.

## Final Thoughts

This room strengthened many of the concepts I learned in previous Linux challenges while introducing me to SSH key cracking, password hash recovery, and privilege escalation through misconfigured sudo permissions. More than anything, it reminded me that successful penetration testing isn't about finding one big vulnerability—it's about understanding the target, connecting small pieces of information, and approaching every stage methodically.

Looking forward to building on these skills with more CTF challenges.
