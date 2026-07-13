# Mr. Robot CTF — Bringing Multiple Skills Together

**Platform:** TryHackMe  
**Room:** Mr. Robot CTF  
**Category:** Web Enumeration, WordPress, Credential Discovery, Linux Privilege Escalation  
**Date:** 13 July 2026

After completing several beginner-friendly rooms, I wanted to challenge myself with something that combined multiple techniques into a single assessment. Mr. Robot CTF felt like the perfect next step because it brought together web enumeration, WordPress reconnaissance, credential discovery, password cracking, SSH access, and Linux privilege escalation.

I started by scanning the target to identify the available services. Once I understood the attack surface, I explored the web application and continued with directory enumeration. As I moved through the room, I discovered that even simple files like robots.txt could reveal valuable information that later became an important part of the assessment.

After spending time gathering information, I identified WordPress users, recovered credentials, and decoded Base64-encoded data that helped me move forward. Recovering a password from its hash using CrackStation reminded me how dangerous weak passwords can be, even when they are not stored in plain text.

Once I had valid credentials, I gained access to the machine over SSH and continued exploring the Linux environment. I spent time navigating the filesystem, examining MySQL, and searching for privilege escalation opportunities. Learning how SUID binaries can be abused with the help of GTFOBins was one of the biggest takeaways from this room.

Compared to the previous rooms, Mr. Robot required me to combine many of the skills I had already learned instead of relying on a single technique. Every stage depended on good enumeration, careful observation, and connecting small pieces of information together before moving forward.

## Tools I Used

- Nmap
- Gobuster
- Browser Developer Tools
- CrackStation
- SSH
- MySQL
- GTFOBins
- Linux Terminal

## What I Learned

- Enumeration should always come before exploitation.
- WordPress can expose valuable information when not configured securely.
- Files like robots.txt should never be ignored during reconnaissance.
- Base64 is an encoding method, not encryption.
- Weak passwords remain a major security risk even when stored as hashes.
- SSH provides a much more stable environment for post-exploitation activities.
- Understanding Linux permissions and SUID binaries is essential for privilege escalation.
- Small pieces of information gathered during enumeration often become the key to solving later stages of an assessment.

## Final Thoughts

This room brought together many of the concepts I had learned throughout previous challenges while giving me more confidence with web enumeration, credential discovery, Linux exploration, and privilege escalation. More than anything, it reminded me that successful penetration testing isn't about relying on a single exploit—it's about understanding the target, connecting small pieces of information, and approaching every stage methodically.

Looking forward to building on these skills with more CTF challenges.
