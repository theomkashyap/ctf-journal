# The Brochure — Learning Image-Based OSINT & Social Media Investigation

**Platform:** TryHackMe  
**Room:** The Brochure  
**Category:** OSINT, Image Analysis, Social Media Investigation  
**Date:** 03 August 2026

After completing several beginner-friendly OSINT challenges, I wanted to explore a room that focused more on investigation than exploitation. The Brochure introduced an image-based OSINT scenario where the objective was to gather information from publicly available sources by carefully following visual clues instead of relying solely on technical tools.

I began by examining the provided brochure image and checking it for hidden metadata using ExifTool. Although the image did not contain any useful metadata, this reinforced an important lesson that OSINT investigations should never depend on a single technique. When one source provides little information, it's important to continue investigating other available clues.

Instead of focusing on metadata, I carefully analyzed the contents of the brochure and identified references that pointed toward the hotel's online presence, including its social media accounts and an AI concierge named Vera. Following these clues led me through several publicly accessible profiles, where each account revealed additional information that helped progress the investigation.

As I continued examining the available content, I noticed that important information had been intentionally distributed across multiple posts rather than being available in one location. By collecting and connecting these small pieces of information, I was eventually able to reconstruct the complete message. Recognizing that the collected text was Base64-encoded allowed me to decode it successfully and complete the challenge.

Compared to previous rooms, The Brochure emphasized observation, patience, and logical thinking over technical exploitation. Every stage required careful analysis of publicly available information and demonstrated how seemingly insignificant details can become valuable intelligence during an OSINT investigation.

## Tools I Used

- ExifTool
- Web Browser
- Instagram
- Base64 Decoder

## What I Learned

- Metadata is not always the most valuable source of information during an investigation.
- Visual analysis can reveal important clues that automated tools may overlook.
- Social media platforms are valuable sources of publicly available intelligence.
- Information collected from multiple sources should be correlated before drawing conclusions.
- Base64 is an encoding method commonly encountered during CTF challenges.
- Observation, patience, and logical thinking are essential skills in OSINT investigations.
- Small pieces of publicly available information can often be combined to reveal the complete picture.

## Final Thoughts

The Brochure provided a practical introduction to image-based OSINT and demonstrated how valuable careful observation can be during an investigation. Rather than relying on complex exploitation techniques, the room highlighted the importance of following visual clues, analyzing public information, and connecting evidence from multiple sources. It reinforced that successful OSINT investigations are built on curiosity, attention to detail, and methodical analysis rather than sophisticated tools alone.

Looking forward to applying these investigative techniques in more OSINT and CTF challenges.
