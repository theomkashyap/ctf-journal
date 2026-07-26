# Cache Me Outside — Strengthening My OSINT Investigation Skills

**Platform:** TryHackMe  
**Room:** Cache Me Outside  
**Category:** OSINT  
**Date:** 26 July 2026

After completing several penetration testing and Linux-focused rooms, I wanted to improve my Open Source Intelligence (OSINT) skills. Cache Me Outside felt like the perfect next step because it combined username enumeration, GitHub investigation, social media analysis, image intelligence, and geolocation into a single investigation.

I started by examining the provided chat screenshot and identifying the first clue. From there, I followed the target's public digital footprint across multiple online platforms instead of relying on a single source of information. As I progressed through the room, I realized that every profile and post revealed a small piece of information that became useful later in the investigation.

After spending some time gathering information, I discovered the target's GitHub profile and explored its repositories. While reviewing the commit history, I learned about the .patch technique, which exposed additional Git metadata that wasn't immediately visible through the standard GitHub interface. This was one of the most interesting techniques I learned from the room.

As the investigation continued, I correlated information gathered from GitHub, email, Instagram, Threads, and Google Maps to uncover the remaining clues. Unlike my previous OSINT room, this challenge emphasized following a continuous trail of publicly available information rather than analyzing a single image or file.

Compared to OhSINT, this room focused more on connecting information across multiple platforms and understanding how seemingly unrelated pieces of public data can build a complete digital footprint. Every stage depended on careful observation, and it reinforced the idea that patience and attention to detail are essential during OSINT investigations.

## Tools I Used

- Browser
- Google Search
- Komoot
- GitHub
- Git Commit History
- Git Patch (.patch)
- Instagram
- Threads
- Google Maps

## What I Learned

- OSINT investigations rely on correlating information from multiple public sources.
- Git commit metadata can unintentionally expose valuable information.
- Username reuse across platforms makes digital footprint analysis much easier.
- Images can reveal location information through background objects.
- Publicly available information can often be connected to build a detailed profile of a target.
- Patience and careful observation are just as important as technical knowledge.

## Final Thoughts

This room strengthened many of the concepts I learned in OhSINT while introducing me to Git metadata analysis, username pivoting, and image-based geolocation. More than anything, it reminded me that successful OSINT investigations aren't about finding one obvious clue—they're about following the digital trail, connecting small pieces of information, and approaching every stage methodically.

Looking forward to building on these skills with more OSINT challenges.
