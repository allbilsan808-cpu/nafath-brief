Version: NAFATH-V3 Track: Mobile

## Overview
This document covers the research for building a trustworthy AI assistant for public service mobile applications under the NAFATH-V3 program.

## Software
### Question: When does the major, minor, or patch version number change according to Semantic Versioning (SemVer)?
- **MAJOR version (`X.0.0`):** Incremented when breaking changes or incompatible API updates are introduced that require client updates.
- **MINOR version (`0.X.0`):** Incremented when new functionality or features are added in a backward-compatible manner.
- **PATCH version (`0.0.X`):** Incremented when backward-compatible bug fixes or security patches are applied.

## AI
### Question: What is Retrieval-Augmented Generation (RAG) and how does it help reduce hallucinations?
- **Retrieval-Augmented Generation (RAG):** A technique that connects Large Language Models (LLMs) to external authoritative databases or document stores to retrieve relevant context before generating a response.
- **Reducing Hallucinations:** By grounding the AI's responses in retrieved, verified facts rather than relying solely on pre-trained weights, RAG ensures accurate and trustworthy outputs for public services.

## Mobile
### Question: What is the function of iOS App Transport Security (ATS)?
- **App Transport Security (ATS):** A privacy and security feature enforced by iOS that requires apps to establish secure network connections over HTTPS using TLS v1.2 or higher.
- **Function:** It protects sensitive user data in transit by blocking unencrypted HTTP connections by default.

## Networking
### Question: What is the difference between IPv4 and IPv6?
- **IPv4:** Uses a 32-bit address space (providing ~4.3 billion unique addresses), represented in decimal format (e.g., `192.168.1.1`).
- **IPv6:** Uses a 128-bit address space (providing an virtually unlimited number of addresses), represented in hexadecimal format (e.g., `2001:db8::1`), offering built-in security (IPsec) and better routing efficiency. 
## Cybersecurity
### Question: What is Prompt Injection and how can its risks be mitigated?
- **Prompt Injection:** A vulnerability where malicious input overwrites or manipulates the original instructions given to an LLM, causing it to perform unintended actions or bypass guardrails.
- **Mitigation:** Implemented through input sanitization, strict system prompt separation, strict role-based authorization, output validation, and continuous monitoring.
## Data
### Question: What is the difference between Data Anonymization and Pseudonymization?
- **Data Anonymization:** Irreversibly alters personal data so that the data subject can no longer be identified directly or indirectly by anyone.
- **Pseudonymization:** Replaces identifiable data fields with artificial identifiers (pseudonyms) in a way that allows re-identification only with a separately stored secret key.
## Misconception in My Track
- **Misconception:** Assuming that App Transport Security (ATS) guarantees complete end-to-end security for all data handled within a mobile app.
- **Reality:** ATS only secures data in transit over the network. Developers must still implement robust local encryption for stored data (e.g., EncryptedSharedPreferences/Keychain) and maintain server-side protection.
## Open Question
- How can mobile applications efficiently cache RAG-retrieved data locally while ensuring real-time compliance with updated public service policies without causing excessive data usage?
