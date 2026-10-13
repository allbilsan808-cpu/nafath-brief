Version: NAFATH-V3
Track: Mobile

## Overview
Building a public service AI chat assistant requires integrating six key IT fields into a cohesive system. Software standardizes releases, AI delivers grounded responses through retrieval, and Mobile enforces strict transport security. Networking ensures scalable device connectivity, Cybersecurity protects against prompt exploitation, and Data manages privacy for chat logs. Together, these fields form a secure, efficient, and compliant solution for citizen services, with a primary focus on Mobile app integration.

## Software
Under Semantic Versioning (SemVer 2.0.0), the assistant's public API increments the MAJOR version when breaking changes or incompatible API updates are introduced that require client updates. It increments the MINOR version when new backward-compatible functionality is added, and the PATCH version when backward-compatible bug fixes are applied.

Resource: Semantic Versioning 2.0.0 - https://semver.org/

## AI
Retrieval-Augmented Generation (RAG) is a technique that connects Large Language Models (LLMs) to external, authoritative databases or document stores to retrieve relevant context before generating a response. It reduces incorrect answers and hallucinations by grounding outputs directly in verified public service data rather than relying solely on pre-trained model weights.

Resource: What is RAG? - AWS - https://aws.amazon.com/what-is/retrieval-augmented-generation/

## Mobile
iOS App Transport Security (ATS) enforces secure network connections by requiring apps to use HTTPS with TLS v1.2 or higher. If the app attempts to call a plain HTTP (non-HTTPS) endpoint, iOS blocks the network request by default, triggering a connection failure unless specific, temporary domain exceptions are configured in Info.plist.

Resource: Apple Developer Documentation: App Transport Security - https://developer.apple.com/documentation/security/app_transport_security

## Networking
IPv6 uses a 128-bit address space providing virtually unlimited unique IP addresses, whereas IPv4 uses a 32-bit address space limited to ~4.3 billion addresses. As the number of connected mobile devices grows, IPv6 is critical to prevent IP exhaustion, eliminate Network Address Translation (NAT) overhead, and improve end-to-end routing efficiency.

Resource: RFC 8200 - Internet Protocol, Version 6 (IPv6) Specification - https://datatracker.ietf.org/doc/html/rfc8200

## Cybersecurity
Prompt injection is an attack where malicious input manipulates an LLM into performing unintended actions. Direct prompt injection occurs when a user directly feeds malicious instructions in the chat input. Indirect prompt injection occurs when the LLM processes external untrusted content containing hidden malicious instructions. Risks are reduced by separating system instructions from user inputs and sanitizing inputs.

Resource: OWASP Top 10 for LLM Applications: Prompt Injection - https://llmtop10.owasp.org/LLM01_Prompt_Injection/

## Data
Data anonymization irreversibly alters personal data so the subject cannot be identified directly or indirectly, whereas pseudonymization replaces identifiers with artificial keys that can be re-identified using separately stored data. Data anonymization takes chat logs outside the scope of data protection laws because the data is no longer considered personal data.

Resource: Regulation (EU) 2016/679 (GDPR) Recital 26 - https://gdpr-info.eu/recitals/no-26/

## Misconception in My Track
A common misconception regarding iOS App Transport Security (ATS) is that it secures all app data end-to-end. In reality, ATS only protects data in transit over HTTPS networks; it does not encrypt data stored locally on the device or secure backend server storage.

Resource: Apple Developer Documentation: App Transport Security - https://developer.apple.com/documentation/security/app_transport_security

## Open Question
How can mobile applications efficiently cache RAG-retrieved public service data locally while maintaining real-time compliance with policy updates without causing high data usage?
