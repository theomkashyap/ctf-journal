# OhSINT — My First CTF

**Platform:** TryHackMe  
**Room:** OhSINT  
**Category:** OSINT  
**Date:** 4 July 2026

My first CTF ever. I went in solo, used no hints, and picked this room randomly just to get started.

The room starts with a single image—a Windows XP wallpaper. My first instinct was to inspect its metadata using exiftool because images often contain more information than they appear to. That gave me a GPS location and an author name, which became my starting point.

A quick Google search for the author led me to a GitHub profile, a Twitter account, and a personal WordPress website. From there, I followed each clue one by one until everything started coming together.

Along the way, I used Browser Developer Tools to inspect a webpage, looked up a wireless network using Wigle.net, and connected different pieces of publicly available information to move forward.

The wireless network lookup was the part that took me the longest. I spent too much time digging deeper into the author's online presence instead of focusing on the clue that actually mattered. Once I stopped overthinking and focused on the missing piece, everything started making sense.

## Tools I Used

- ExifTool
- Google Search
- Browser Developer Tools
- Wigle.net

## What I Learned

- Always inspect file metadata before making assumptions.
- OSINT is about connecting small pieces of public information.
- Not every lead is worth chasing.
- Staying focused is just as important as technical knowledge.

## Final Thoughts

This was a simple room, but it was a great introduction to OSINT. More than anything, it taught me that OSINT isn't about hacking systems—it's about asking the right questions, following the evidence, and knowing where to look next.

Looking forward to building on these skills with more CTF challenges.
