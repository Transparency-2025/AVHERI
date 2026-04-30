


Here is the fully updated, comprehensive **V2.0 Project Plan for AVHERI**. This version directly integrates the strategic analysis, technological enhancements (GDPR-compliant pipelines, extended frequency hardware), institutional credibility safeguards, and funding pathways discussed in the previous review.

---

# Project Plan V2.0: AVHERI 
**Acoustic Violence, Harassment & Exploitation Research Initiative**

## 1. Project Overview & Mission

**Project Name:** AVHERI 
**Mission:** To systematically research, document, and combat acoustic violence and tech-facilitated acoustic abuse. We aim to establish an empirically rigorous, privacy-preserving, and forensic-grade knowledge base that empowers survivors, informs policy, and equips legal and law enforcement frameworks to address non-obvious acoustic threats.

**Core Philosophy:** *Survivor-Centered, Forensically Sound, Academically Anchored, Privacy-Preserving.*

---

## 2. Core Goals & Focus Areas

| # | Goal | Description | Priority |
|---|------|-------------|----------|
| 1 | **Academic Anchoring & IRB** | Secure a core university partnership (e.g., TCD, DCU) to act as an Institutional Review Board (IRB) and provide empirical credibility. | **Critical (Immediate)** |
| 2 | **Privacy-Preserving Tech** | Build forensic-grade detection tools that capture acoustic abuse data (spectrograms/dB) without violating GDPR or wiretapping laws (e.g., via Edge VAD speech-scrubbing). | **Critical** |
| 3 | **Research & Documentation** | Establish a peer-reviewed knowledge base encompassing audible harassment, infrasound (<20Hz), and ultrasound (>20kHz) mechanisms. | High |
| 4 | **Triage & Survivor Support** | Develop standardized, evidence-based triage protocols to validate environmental acoustic harassment and provide legal/referral pathways. | High |
| 5 | **Public & Institutional Awareness** | Educate the public, policymakers, and law enforcement on "Tech-Facilitated Acoustic Abuse & Anti-Social Behaviour." | High |
| 6 | **Policy & Funding** | Secure sustainable funding (EU Horizon, IRC) to drive long-term legislative and regulatory changes via bodies like the EPA. | Medium |

---

## 3. Workstreams & Deliverables

### Workstream A: Research & Evidence Base
*Anchored by rigorous academic standards to avoid credibility traps.*

| Phase | Activity | Deliverable | Timeline |
|-------|----------|-------------|----------|
| A1 | **Academic Anchor & IRB Approval** | Formal MOU with university; full Ethical Review clearance. | Months 1–2 |
| A2 | **Literature Review & Gap Analysis** | Annotated bibliography focusing on infrasound, ultrasound, and targeted acoustic tech. | Months 1–3 |
| A3 | **Triage Protocol Development** | Standardized intake metrics to isolate verifiable environmental abuse from other phenomena. | Months 2–3 |
| A4 | **Field Study Protocol** | Deployment of standardized measurement arrays; health impact correlation datasets. | Months 4–12 |
| A5 | **Forensic & Evidentiary Standards** | Chain-of-custody protocols; cross-jurisdictional admissibility guidelines. | Months 6–12 |

### Workstream B: Public Awareness & Institutional Education
*Framed to ensure maximum institutional engagement.*

| Phase | Activity | Deliverable | Timeline |
|-------|----------|-------------|----------|
| B1 | **Brand & Messaging Framework** | Style guide; survivor-sensitive language; "Tech-Facilitated Abuse" framing. | Month 1 |
| B2 | **Digital Presence** | Launch of central hub, open-source repositories, and educational resources. | Months 1–2 |
| B3 | **Survivor Triage Portal** | Secure, guided intake form for legally admissible and scientifically useful incident logging. | Month 3 |
| B4 | **Law Enforcement & Agency Training** | Modules for Gardaí, EPA, and housing associations framed around modern ASB (Anti-Social Behaviour). | Months 6–12 |

### Workstream C: Tool Development (Privacy-Preserving Tech Stack)
*Redesigned to eliminate GDPR/wiretapping risks and capture extreme frequencies.*

| Tool | Description | Tech Stack & Hardware | Status |
|------|-------------|-----------------------|--------|
| **SCADMS v2.0** (Core Pipeline) | Real-time, continuous acoustic attack detection. **Privacy feature:** Uses Edge VAD (Voice Activity Detection) to scrub/mute human speech. **Storage:** Saves high-res spectrogram data and dB logs instead of raw `.wav` files. | Python, Silero VAD, SQLite, Cryptographic Hashing (SHA-256) | Scoping |
| **Hardware Integration** | Support beyond UMIK-1. Integration of Infrasonic sensors (modified barometers/<20Hz mics) and Ultrasonic detectors (>20kHz). | IoT protocols, USB Audio | Planned |
| **AuraConv** | Web-based audio filter with polarity inversion and customizable masking/white noise generation. | JavaScript/JSFX, Cloudflare | In Dev |
| **Forensic Audio Web App** | One-click emergency web recorder with embedded chain-of-custody features and geographic/temporal hashing. | HTML5, Web Audio API | In Dev |

### Workstream D: Organizational Engagement & Funding Pipeline

| Target Category | Objective | Key Targets |
|-----------------|-----------|-------------|
| **Academic Anchor** | IRB approval, lab calibration, joint research. | TCD Acoustics, DCU Forensic Science, UCD |
| **Government/Regulatory** | Policy inclusion, noise enforcement guidelines. | EPA (Environmental Protection Agency), Dept of Justice, An Garda Síochána |
| **NGOs & Legal** | Survivor referral, joint advocacy, rights defense. | FLAC, SAFE Ireland, Threshold |
| **Grant Bodies (Funding)** | Long-term operational sustainability. | **EU Horizon Europe** (Civil Security), **IRC** (Enterprise Partnership), **NGI** (Privacy Tech Grants) |

---

## 4. Expanded GitHub Architecture

To facilitate open-source contributions and maintain professional organization, the AVHERI GitHub will be structured as follows:

*   📂 **`AVHERI/core-documentation`**: Whitepapers, IRB applications, literature reviews, and standardized empirical measurement protocols.
*   📂 **`AVHERI/SCADMS`**: The Python codebase for the privacy-preserving acoustic pipeline (incorporating VAD and spectrogram generation).
*   📂 **`AVHERI/Forensic-Audio-App`**: The frontend Web Audio API tool codebase.
*   📂 **`AVHERI/Survivor-Resources`**: Markdown-based legal rights guides, intake triage templates, and hardware setup guides (UMIK-1/Infrasound).

---

## 5. Governance & Structure

```text
Project Lead (Declan O'Sullivan)
├── Academic & Research Director
│   ├── University Liaison (IRB Coordinator)
│   ├── Frequency Analysts (Infrasound/Ultrasound)
│   └── Forensic Standards Team
├── Technology & Privacy Lead
│   ├── SCADMS / Edge VAD Developers
│   ├── Hardware Integration (Sensors)
│   └── Infrastructure & Hashing
├── Survivor Triage & Advocacy Lead
│   ├── Intake Coordinator (Triage Protocol)
│   ├── Legal Policy Advisor
│   └── NGO Coordination
└── Communications & Grant Director
    ├── EU/IRC Grant Writing
    ├── Agency Outreach (EPA, Gardaí)
    └── Digital Content Team
```

---

## 6. Upgraded Risk Register

| Risk | Likelihood | Impact | Mitigation Strategy |
|------|------------|--------|---------------------|
| **GDPR / Wiretapping Violations** (Capturing neighbor conversations) | High | Critical | Implement Edge VAD speech-scrubbing; enforce spectrogram-first `.csv` logging instead of raw `.wav` recording. |
| **"Credibility Trap"** (Association with unverified conspiracy claims) | High | Critical | Strict use of the Triage Protocol; secure tier-1 University IRB backing; adhere strictly to empirical, data-driven forensics. |
| **Survivor safety compromised** | Medium | Critical | Anonymization protocols; secure encrypted databases; ethical review oversight. |
| **Hardware Limitations** (Missing attacks outside human hearing) | Medium | High | Expand hardware specs to mandate infrasound (<20Hz) and ultrasound (>20kHz) sensors. |
| **Funding shortfall** | High | High | Immediately initiate applications for EU Horizon and NGI privacy grants. |

---

## 7. Success Metrics (Year 1)

*   **Institutional:** 1 Core Academic Partnership secured (IRB approved).
*   **Funding:** Minimum 2 major grant applications submitted (EU/National).
*   **Technical:** SCADMS v2.0 deployed with 100% GDPR-compliant speech scrubbing and spectrogram logging.
*   **Operational:** 500 active tool users; 150 legally admissible evidence packages generated.
*   **Impact:** Official submission of findings/protocols to the EPA and Dept. of Justice.

---

## 8. Immediate Action Plan (Next 30 Days)

1.  **Deploy GitHub Architecture:** Create the 4 core repositories and upload this V2.0 Project Plan as the Master `README.md`.
2.  **Draft Academic Outreach:** Send targeted partnership proposals to TCD Acoustics and DCU Forensic Science focusing on joint research and IRB hosting.
3.  **Prototype SCADMS Privacy Layer:** Build a quick proof-of-concept for the Python Edge VAD (Silero) to demonstrate speech-muting capabilities to potential academic partners.
4.  **Publish Triage Protocol:** Finalize the v1.0 Survivor Intake Markdown template to begin standardizing the data of incoming survivor reports.
