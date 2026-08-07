# The Concierge Knows Too Much — Exploring Prompt Injection in AI Systems

**Platform:** TryHackMe  
**Room:** The Concierge Knows Too Much  
**Category:** AI Security, Prompt Injection, LLM Security  
**Date:** 05 August 2026

As artificial intelligence continues to become a part of modern applications, I wanted to explore how Large Language Models (LLMs) can be manipulated through prompt injection attacks. The Concierge Knows Too Much introduced this concept in a simple but practical way by simulating an AI-powered hotel assistant that had access to confidential information.

The objective was not to exploit a traditional web application or operating system but to understand how carefully crafted prompts can influence an AI model's behavior. The assistant initially refused to reveal sensitive information, making it clear that it had been instructed to protect an internal escalation code.

Rather than attacking the underlying application, I focused on interacting with the AI itself. By observing its responses and understanding the context it trusted, I learned how prompt engineering and social engineering principles can be combined to influence an LLM into revealing information that it was intended to keep private.

This room demonstrated that prompt injection is fundamentally different from traditional software vulnerabilities. Instead of exploiting programming flaws, the attack targets the model's instructions, context, and decision-making process. It also highlighted why developers should never rely solely on prompts to protect sensitive information inside AI-powered applications.

Although this challenge was much shorter than a traditional penetration testing room, it provided an excellent introduction to one of the fastest-growing areas of cybersecurity. As AI assistants become increasingly common in real-world applications, understanding prompt injection techniques and AI security principles will become an important skill for security professionals.

## Tools I Used

- TryHackMe AI Playground
- Browser
- Prompt Engineering Techniques

## What I Learned

- Prompt injection targets an AI model's instructions rather than the application itself.
- Large Language Models can sometimes reveal confidential information when given carefully crafted prompts.
- AI assistants should never rely solely on prompts to protect sensitive data.
- Prompt engineering plays a significant role in both attacking and defending LLM-based applications.
- Understanding an AI assistant's context and behavior is often more important than repeatedly asking the same question.
- AI security introduces a completely different attack surface compared to traditional web exploitation.

## Final Thoughts

This room served as a great introduction to AI security and prompt injection attacks. While it was considerably shorter than traditional CTF rooms, it demonstrated that securing AI systems requires a different mindset from conventional penetration testing. Instead of focusing on software vulnerabilities, the challenge emphasized understanding how language models interpret instructions and why robust guardrails are essential for protecting sensitive information.

As AI continues to be integrated into modern applications, learning about prompt injection and LLM security will become an increasingly valuable skill for cybersecurity professionals. I look forward to exploring more AI-focused security challenges and gaining a deeper understanding of how these systems can be tested and secured.
