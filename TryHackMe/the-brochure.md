# The Brochure — Learning Image-Based OSINT & Social Media Investigation

**Platform:** TryHackMe  
**Room:** The Brochure  
**Category:** OSINT, Image Analysis, Social Media Investigation  
**Date:** 3 August 2026

After completing several introductory OSINT rooms, I wanted to try a challenge that focused more on observation and investigation than technical exploitation. The Brochure felt like the perfect next step because it demonstrated how seemingly ordinary information shared online can reveal much more than intended when examined carefully.

I started by downloading the provided brochure image and inspecting it for hidden metadata using ExifTool. Since no useful metadata was present, I shifted my attention to the visual clues embedded within the image itself. Rather than relying on automated tools, I carefully examined the brochure and identified references that pointed toward the hotel's social media presence and an AI concierge named Vera.

Following those clues led me to the hotel's Instagram profile, where I explored its public information, posts, and account connections. Instead of stopping after finding the initial account, I continued investigating related profiles, which ultimately became the key to progressing further. While examining the available content, I noticed that important information had been intentionally distributed across multiple posts rather than presented in a single location.

Recognizing that the collected text was Base64-encoded allowed me to reconstruct and decode the final message successfully. This room reinforced how valuable patience and careful observation are during an OSINT investigation, where every small clue can contribute to uncovering the complete picture.

Compared to previous rooms, The Brochure required less technical exploitation and much more investigative thinking. Every stage depended on carefully following publicly available information, verifying assumptions, and connecting multiple sources before reaching the final result.

## Tools I Used

- ExifTool
- Web Browser
- Instagram
- Base64 Decoder

## What I Learned

- Metadata is not always the most valuable source of information during an investigation.
- Visual inspection can often reveal clues that automated tools cannot.
- Social media profiles and their relationships are valuable sources of OSINT.
- Publicly available information should always be examined carefully before drawing conclusions.
- Base64 is an encoding method that frequently appears in CTF challenges.
- Patience and attention to detail are essential skills during OSINT investigations.
- Small clues collected throughout an investigation often combine to reveal the complete solution.

## Final Thoughts

This room gave me a better understanding of how image analysis, social media investigation, and basic data decoding work together during an OSINT assessment. More than anything, it reminded me that successful investigations are built on observation, logical thinking, and carefully following every available lead instead of relying solely on specialized tools.

Looking forward to building on these skills with more CTF challenges.
