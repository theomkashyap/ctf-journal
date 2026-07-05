# RootMe — My First Web Exploitation & Privilege Escalation CTF

**Platform:** TryHackMe  
**Room:** RootMe  
**Category:** Web Exploitation, Enumeration, Privilege Escalation  
**Date:** 5 July 2026

After completing OhSINT, I wanted to try something more hands-on. RootMe felt like the perfect next step because it covered the complete process of attacking a target machine instead of gathering information through OSINT.

I started by scanning the target to identify the available services. Since a web server was running, I explored the website and then moved on to directory enumeration to discover hidden content that wasn't visible from the homepage.

After spending some time understanding the application, I found a way to gain an initial shell on the machine. Getting my first reverse shell was definitely the most satisfying part of the room because it was the first time I had successfully interacted with a target machine in that way.

Once I had access, I spent time exploring the Linux filesystem, searching for important files, checking permissions, and looking for privilege escalation opportunities. Along the way, I learned about SUID binaries and discovered GTFOBins, which introduced me to the idea that common Linux binaries can sometimes be used for privilege escalation. Learning how Python could be used in that context was completely new to me and one of the biggest takeaways from this room.

Compared to my first CTF, this room required much more patience. Every stage depended on proper enumeration, and it became clear that rushing ahead without understanding the target would only make things harder later.

## Tools I Used

- Nmap
- Gobuster
- Browser Developer Tools
- Linux Terminal
- GTFOBins

## What I Learned

- Enumeration should always come before exploitation.
- A reverse shell is only the beginning of an assessment.
- SUID binaries are an important area to investigate during Linux privilege escalation.
- GTFOBins is an excellent resource for understanding Linux privilege escalation techniques.
- Small clues discovered during enumeration often lead to the biggest breakthroughs.
- Patience and careful observation are just as important as technical knowledge.

## Final Thoughts

This room gave me my first complete experience of moving from reconnaissance to privilege escalation. More than anything, it taught me that successful exploitation starts with good enumeration, and understanding the target is often more important than immediately looking for an exploit.

Looking forward to building on these skills with more CTF challenges.
