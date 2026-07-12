# Bypass Disable Functions — Understanding PHP Security & Restricted Execution

**Platform:** TryHackMe  
**Room:** Bypass Disable Functions  
**Category:** Web Exploitation, PHP Security, Remote Code Execution  
**Date:** 11 July 2026

After completing previous web exploitation rooms, I wanted to learn how PHP applications behave when dangerous execution functions are disabled. Bypass Disable Functions felt like an interesting challenge because it focused on understanding server configuration, restricted PHP environments, and how remote code execution can still be achieved under certain conditions.

I started by scanning the target to identify the available services before exploring the web application. As I moved through the room, I spent time enumerating directories and gathering information about the server. One of the most valuable discoveries was an exposed phpinfo() page, which revealed important details about the PHP environment and helped me understand how the application was configured.

After understanding the server configuration, I learned how reverse shells can still be achieved even when common PHP execution functions are disabled. This room introduced me to Chankro, a tool designed to bypass PHP disable_functions restrictions in vulnerable environments. It was interesting to see how proper reconnaissance and understanding the server configuration played a much bigger role than simply looking for an exploit.

Once I established a shell, I explored the Linux environment, navigated the filesystem, and continued practicing basic post-exploitation techniques. More than anything, this room reinforced how important information gathering is before attempting exploitation.

Compared to the previous rooms, Bypass Disable Functions focused more on PHP internals and server configuration than traditional web exploitation. It reminded me that understanding how an application is configured can often be just as valuable as understanding the vulnerability itself.

## Tools I Used

- Nmap
- Gobuster
- phpinfo()
- Chankro
- Netcat
- Linux Terminal

## What I Learned

- Enumeration should always come before exploitation.
- Information disclosed through **phpinfo()** can provide valuable insight into a server's configuration.
- Disabling dangerous PHP functions alone does not always eliminate the risk of remote code execution.
- Reverse shells remain an important part of understanding post-exploitation workflows.
- Understanding server configuration is just as important as understanding vulnerabilities.
- Careful observation and systematic reconnaissance often make exploitation much easier.

## Final Thoughts

Bypass Disable Functions introduced me to a different side of web exploitation by focusing on PHP security and restricted execution environments. More than anything, it reminded me that successful penetration testing isn't just about finding vulnerabilities—it's about understanding how the target is configured, gathering the right information, and using that knowledge effectively.

Looking forward to building on these skills with more CTF challenges.
