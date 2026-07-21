# Agent Sudo — Strengthening My Enumeration & Multi-Stage Exploitation Skills

**Platform:** TryHackMe  
**Room:** Agent Sudo  
**Category:** Web Enumeration, Password Cracking, Steganography, Linux Privilege Escalation  
**Date:** 21 July 2026

After completing several beginner-friendly Linux and web exploitation rooms, I wanted to challenge myself with something that combined multiple attack techniques into a single workflow. Agent Sudo felt like the perfect next step because it brought together web enumeration, password cracking, steganography, credential discovery, SSH access, and Linux privilege escalation.

I started by scanning the target to identify the available services. Since multiple services were running, I explored the web application first and quickly realized that it behaved differently depending on the HTTP User-Agent header. Discovering hidden functionality simply by changing the User-Agent reminded me that even small details during web enumeration can become valuable entry points.

After spending some time gathering information, I identified a valid username and eventually recovered FTP credentials through password cracking. While exploring the downloaded files, I discovered that the room involved much more than simple enumeration. Examining image metadata, extracting hidden files, recovering a password-protected ZIP archive, and analyzing encoded information gradually revealed the credentials needed to gain SSH access.

Once I had access to the machine, I explored the Linux filesystem, searched for privilege escalation opportunities, and became more comfortable investigating the system after initial compromise. Along the way, I also learned how tools like ExifTool, Foremost, zip2john, John the Ripper, and Steghide can work together during file analysis and credential recovery. Understanding how each clue led to the next was one of the biggest takeaways from this room.

Compared to Dreaming, this room focused less on custom exploitation techniques and more on combining different reconnaissance, file analysis, password recovery, and privilege escalation methods into one complete attack chain. Every stage depended on careful enumeration, and it reinforced the idea that patience and attention to detail often make the biggest difference.

## Tools I Used

- Nmap
- Burp Suite
- Hydra
- FTP
- ExifTool
- Foremost
- zip2john
- John the Ripper
- Steghide
- SSH
- Linux Terminal

## What I Learned

- Enumeration should always come before exploitation.
- HTTP headers like **User-Agent** can reveal hidden application functionality.
- Dictionary attacks become much more effective when valid usernames are available.
- Image metadata and embedded files can expose valuable information.
- zip2john and John the Ripper introduced me to cracking password-protected ZIP archives.
- Steganography can hide sensitive information inside seemingly ordinary image files.
- Careful Linux enumeration is essential for identifying privilege escalation opportunities.
- Patience and careful observation are just as important as technical knowledge.

## Final Thoughts

This room strengthened many of the concepts I learned in Dreaming while introducing me to steganography, file analysis, and multi-stage credential recovery. More than anything, it reminded me that successful penetration testing isn't about finding one big vulnerability—it's about understanding the target, connecting small pieces of information, and approaching every stage methodically.

Looking forward to building on these skills with more CTF challenges.
