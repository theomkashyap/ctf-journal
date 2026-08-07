# Vulnversity — Learning Web Exploitation and Linux Privilege Escalation

**Platform:** TryHackMe  
**Room:** Vulnversity  
**Category:** Web Enumeration, File Upload Exploitation, Linux Privilege Escalation  
**Date:** 07 August 2026

After completing several introductory rooms, I wanted to practice a complete penetration testing workflow that covered reconnaissance, directory enumeration, web exploitation, and privilege escalation. Vulnversity provided a realistic environment where every stage depended on the information gathered during the previous one.

I began by performing network reconnaissance to identify the services running on the target machine. Using Nmap, I discovered multiple open ports, identified the operating system as Ubuntu, and found that the web application was hosted on a non-standard port. This reinforced the importance of performing thorough service enumeration instead of assuming applications always run on common ports.

With the web server identified, I continued by enumerating hidden directories. Instead of using Gobuster as suggested in the room, I chose to use Dirsearch to discover additional paths. This revealed an internal upload page that became the primary attack surface for the remainder of the challenge.

While testing the upload functionality, I noticed that standard PHP files were blocked. Rather than stopping there, I used Burp Suite Intruder to fuzz different PHP extensions and discovered that the server accepted .phtml files. This demonstrated how file upload restrictions often rely on simple extension filtering, which can sometimes be bypassed using alternative file extensions.

After successfully uploading a modified PHP reverse shell, I established a reverse connection to the target machine and gained an interactive shell. From there, I explored the Linux filesystem, identified the user managing the web server, and collected the user flag while continuing to enumerate the system for privilege escalation opportunities.

For privilege escalation, I searched for SUID binaries and discovered that systemctl had the SUID bit set, which immediately stood out as unusual. Using GTFOBins as a reference, I created a malicious systemd service that executed a reverse shell with elevated privileges. After enabling and starting the service, I obtained a root shell and successfully captured the final flag.

This room demonstrated how a complete attack chain is built by combining careful reconnaissance, web application testing, post-exploitation enumeration, and Linux privilege escalation. Every stage relied on information gathered during earlier phases, making enumeration the most important part of the assessment.

## Tools I Used

- Nmap
- Dirsearch
- Burp Suite
- Netcat
- PHP Reverse Shell (PentestMonkey)
- Python HTTP Server
- Linux Terminal
- GTFOBins

## What I Learned

- Thorough reconnaissance is essential before attempting exploitation.
- Services running on uncommon ports should never be overlooked.
- Directory enumeration often reveals hidden attack surfaces.
- File upload protections can sometimes be bypassed using alternative PHP extensions such as .phtml.
- Burp Suite Intruder is useful for testing multiple payload variations efficiently.
- Reverse shells provide initial access but require further enumeration for privilege escalation.
- Enumerating SUID binaries is an important step during Linux privilege escalation.
- Misconfigured systemctl binaries can lead to full root compromise when executed with elevated permissions.
- Successful penetration testing depends on connecting information gathered across every stage of an assessment.

## Final Thoughts

Vulnversity was an excellent room for reinforcing the complete penetration testing methodology, from reconnaissance to full system compromise. It strengthened my understanding of web application enumeration, file upload vulnerabilities, reverse shells, and Linux privilege escalation while emphasizing that successful exploitation begins with careful observation rather than immediately searching for vulnerabilities.

This room gave me more confidence in performing end-to-end assessments and highlighted how each phase of penetration testing builds upon the one before it. It was another valuable step toward developing practical web exploitation and privilege escalation skills through hands-on learning.
