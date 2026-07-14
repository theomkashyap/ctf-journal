# Dreaming — Exploring Multi-Stage Linux Privilege Escalation

**Platform:** TryHackMe  
**Room:** Dreaming  
**Category:** Web Exploitation, Command Injection, Linux Privilege Escalation  
**Date:** 14 July 2026

After completing several Linux-focused rooms, I wanted to try something that required more than just finding a single privilege escalation vector. Dreaming felt like the perfect next step because it combined web enumeration, command injection, database interaction, process monitoring, and Python-based privilege escalation into one complete attack path.

I started by scanning the target to identify the available services before moving on to web enumeration. After exploring the application and its directories, I gained initial access to the machine and continued my investigation through the Linux terminal. Rather than immediately searching for privilege escalation techniques, I focused on understanding the system first.

While enumerating the machine, I explored user files, configuration files, and command history. One of the most useful findings came from the user's `.bash_history`, which revealed database credentials and provided a better understanding of how the application was configured. Using those credentials, I connected to MySQL and gathered additional information that helped me progress further through the room.

As I continued analyzing the application, I identified a Command Injection vulnerability caused by user-controlled input being passed directly into a shell command. Exploiting this vulnerability reinforced how dangerous improper input validation can be and how a small coding mistake can lead to full system compromise.

After gaining a stable shell, I shifted my attention to Linux privilege escalation. I monitored background processes using pspy64 and eventually discovered a Python script running periodically with elevated privileges. After inspecting how the script worked, I abused Python Module Hijacking by replacing an imported module with my own malicious code. When the scheduled task executed again, my code ran automatically with elevated privileges, leading to successful privilege escalation.

Compared to the previous rooms, Dreaming relied much more on careful enumeration and connecting multiple findings together. Every stage built upon the previous one, making it an excellent exercise in thinking through an entire attack chain instead of relying on a single exploit.

## Tools I Used

- Nmap
- Gobuster
- SSH
- MySQL
- pspy64
- Linux Terminal

## What I Learned

- Enumeration should always come before exploitation.
- .bash_history can reveal sensitive credentials and useful administrative commands.
- Database credentials can provide valuable insight during post-exploitation.
- Command Injection vulnerabilities often result from insecure input handling.
- pspy64 is an effective tool for discovering scheduled tasks and privileged background processes.
- Python Module Hijacking can be used to execute arbitrary code through insecure module imports.
- Multi-stage privilege escalation often depends on connecting several small findings rather than relying on one critical vulnerability.

## Final Thoughts

Dreaming brought together many of the concepts I had learned in previous rooms while introducing me to command injection, process monitoring, and Python module hijacking. More than anything, it reinforced that successful penetration testing is driven by thorough enumeration, understanding how different components interact, and patiently connecting small pieces of information to achieve the final objective.

Looking forward to building on these skills with more CTF challenges.
