# AI Forensics — AI-Assisted Digital Forensics

**Platform:** TryHackMe  
**Room:** AI Forensics  
**Category:** AI, Digital Forensics, Incident Response  
**Date:** 8 August 2026

After completing several traditional DFIR and cybersecurity rooms, I wanted to understand how AI can be used during digital forensic investigations. The AI Forensics room focused on using AI to identify anomalies, suspicious files, and patterns that could help investigators during an incident.

## What I Learned

The first part of the room covered some important AI concepts used in DFIR.

- **Anomaly Detection** — helps identify unusual patterns in large datasets.
- **Precision** — measures how many positively flagged results are actually correct.
- **Non-determinism** — the same input can sometimes produce different outputs from an AI system.
- **CNNs** — commonly used in image and video forensics to identify spatial patterns.
- **Sentiment Analysis** — can be used to analyze the emotional tone of messages.
- **Dynamic Analysis** — examines how a program behaves to determine whether it may be malicious.
- **Federated Learning** — allows machine learning while keeping sensitive data on local systems.

The room also introduced the **Daubert Test**, **Black Box AI**, and concerns around bias in technologies such as facial recognition.

## Practical Investigation

The practical section involved investigating a compromised DFIR environment using AI-assisted scripts.

I started by analyzing authentication logs:

```bash
source /opt/dfir-env/bin/activate
python3 /opt/dfir-lab/classify_logs.py /var/log/auth.log
