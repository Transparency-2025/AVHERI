


--- START OF FILE Paste April 30, 2026 - 3:00PM ---

# AVHERI Project Plan V4.0
## Acoustic Violence, Harassment & Exploitation Research Initiative

**Version:** 4.0 | **Date:** 2026-04-30 | **Status:** Hardware Architecture & Deployment Release

---

## Executive Summary

AVHERI V4.0 transitions the initiative from a strategic framework into an execution-ready operational entity. This version integrates robust hardware architecture (the AVHERI Sentinel Node), solves critical compute and interface bottlenecks, mitigates the "Trauma-Cryptography paradox" via Shamir's Secret Sharing, and introduces spatial acoustic tracking (Direction of Arrival) to legally pinpoint perpetrators. Furthermore, it embeds ISO/IEC 27037 digital forensic standards to ensure absolute legal admissibility across EU jurisdictions.

---

## 1. Project Overview & Mission

**Project Name:** AVHERI — Acoustic Violence, Harassment & Exploitation Research Initiative

**Mission:** To systematically research, document, and combat acoustic violence and tech-facilitated acoustic abuse through an empirically rigorous, privacy-preserving, and forensic-grade knowledge base that empowers survivors, informs policy, and equips legal frameworks.

**Core Philosophy:** *Survivor-Centered, Forensically Sound, Academically Anchored, Privacy-Preserving, Legally Compliant.*

---

## 2. Core Goals & Focus Areas

| # | Goal | Description | Priority | Status |
|---|------|-------------|----------|--------|
| 1 | **Legal & Governance** | Register CLG; establish Ethics Review Subcommittee; appoint Data Protection Officer (DPO). | **Critical** | In Progress |
| 2 | **Academic Anchoring (IRB)** | Secure a core university partnership (TCD, DCU) for IRB host and lab validation. | **Critical** | Not Started |
| 3 | **Privacy & Cryptography** | Deploy Edge VAD speech-scrubbing, spectrogram-first logging, and Shamir’s Secret Sharing for trauma-informed key recovery. | **Critical** | Scoping |
| 4 | **Hardware Deployment** | Build the "AVHERI Sentinel Node" (RPi5-based) with spatial tracking (DOA), offline buffering, and multi-spectrum sensors. | **Critical** | Scoping |
| 5 | **Survivor-Centered Design** | Establish Lived Experience Advisory Panel; co-design granular consent flows. | High | Not Started |
| 6 | **Forensic Standardization** | Achieve ISO/IEC 27037 compliance for digital evidence collection. | High | Not Started |
| 7 | **Policy & Funding** | Execute targeted 2026/2027 grant roadmap (IHREC, EPA, IRC, Horizon Europe). | Medium | Active |

---

## 3. Legal & Governance Infrastructure

### 3.1 Legal Entity & Governance

AVHERI will be registered as a **Company Limited by Guarantee (CLG)** in Ireland, governed by a Board of Directors including a Legal Chair, Project Lead, Academic Director, and Survivor Advocate.

### 3.2 Data Protection & Evidence Integrity (ISO/IEC 27037)

Under GDPR Article 37, a **Data Protection Officer (DPO)** is mandatory. To guarantee evidence admissibility in court, all data handling will be aligned with **ISO/IEC 27037:2012** (Guidelines for identification, collection, acquisition, and preservation of digital evidence).

**Key Protocols:**
- **Tamper-Evident Hardware:** Sensors log gyroscopic movement and power loss to prove devices were not moved or manipulated by the survivor.
- **Counter-Forensic Buffering:** Devices feature massive local SQLite SD buffers to defeat perpetrator Wi-Fi jamming, syncing only when connections are secure.

---

## 4. Survivor-Centered Design & Data Control

### 4.1 Granular Consent Model (A/B/C)
Survivors choose their participation level (A: Anonymous Research, B: Identifiable Legal Support, C: Full Research Participation) with a guaranteed **72-hour Safe Exit Deletion Protocol**.

### 4.2 Mitigating the Trauma-Cryptography Paradox
Trauma deeply impacts memory. If a survivor loses an encryption password, zero-knowledge encryption results in permanent evidence loss.

**Solution: Shamir’s Secret Sharing (SSS) / Social Recovery**
The master decryption key is cryptographically split into three shards:
1. **Shard 1:** Held by the Survivor.
2. **Shard 2:** Held by AVHERI Secure Storage.
3. **Shard 3:** Held by a Trusted NGO (e.g., SAFE Ireland, FLAC).
*Requirement:* Any **2 of the 3** shards can reconstruct the evidence. AVHERI cannot access the data alone, but if the survivor forgets their password, AVHERI + the NGO can collaboratively recover the evidence for them.

---

## 5. Workstreams & Deliverables

### Workstream A: Research & Evidence Base

| Phase | Activity | Deliverable | Timeline |
|-------|----------|-------------|----------|
| A1 | **Academic Anchor & IRB Approval** | Formal MOU with university (TCD/DCU); Ethical Review | Months 1–2 |
| A2 | **Counter-Forensics Analysis** | Research acoustic masking separation (e.g., pulling infrasound spikes from underneath loud music) | Months 2–4 |
| A3 | **Forensic Standards Update** | Implementation of ISO/IEC 27037 chain-of-custody protocols | Months 3–6 |
| A4 | **Field Study & Deployment** | Deployment of 10 Sentinel Nodes for health impact correlations | Months 4–12 |

### Workstream B: Public Awareness & Institutional Education
*(Governed by the "Credibility Ladder" — strictly no law enforcement engagement until Phase 4 / peer review).*

| Phase | Activity | Deliverable | Timeline |
|-------|----------|-------------|----------|
| B1 | **Phase 1: Silent Research** | Closed alpha testing; IRB applications; university MOU | Months 1–3 |
| B2 | **Phase 2: Academic Validation** | First peer-reviewed paper submitted; NGO MOUs signed | Months 4–6 |
| B3 | **Phase 3: Controlled Visibility** | Co-branded university whitepaper; media embargo lift | Months 7–9 |
| B4 | **Phase 4: Policy Entry** | EPA submission; Gardaí ASB training module rollout | Months 10–12 |

### Workstream C: Tool Development (The Hardware & Tech Stack)

#### C.1 The "AVHERI Sentinel" Compute Node
To solve the compute bottleneck of running real-time AI and processing multi-band audio, AVHERI replaces standard PCs with a standardized hardware appliance deployed to survivor homes.

*   **Core Logic Board:** Raspberry Pi 5 (8GB) or NVIDIA Jetson Nano.
*   **Sensor Array:**
    *   *Audible:* ReSpeaker Mic Array v2.0 (Calculates **Direction of Arrival [DOA]** to legally prove *where* the sound originates—e.g., the ceiling vs. the adjoining wall).
    *   *Infrasound (<20Hz):* Infiltec MIC-1 (via custom Analog-to-Digital [ADC] USB Hat).
    *   *Ultrasound (>20kHz):* Knowles SPU0410LR5H-QB.
*   **Security:** Tamper-evident enclosure (IMU gyro logs physical movement).

#### C.2 SCADMS v4.0 Architecture Update

| Layer | Technology | Rationale / Upgrade |
|-------|------------|---------------------|
| **Compute Node** | RPi 5 (8GB) + Custom Hat | Solves thermal throttling; unifies analog/digital interfaces. |
| **Spatial Tracking** | ReSpeaker DOA algorithms | Calculates acoustic heatmaps to identify perpetrator location. |
| **Speech Scrubbing** | Silero VAD + Whisper Tiny | Dual-layer verification; false negatives caught by Whisper. |
| **Threat Mitigation** | Local SD Buffering | Defeats perpetrator Wi-Fi jamming attempts. |
| **Storage & Keys** | MinIO + Shamir's Secret Sharing | ISO 27037 compliant; prevents trauma-induced data loss. |

**SCADMS v4.0 Pseudocode Enhancements:**
```python
def process(self, multi_channel_buffer: AudioBuffer) -> EvidencePackage:
    # 1. Privacy Scrubbing (Dual Layer)
    if self.vad(multi_channel_buffer) > 0.5 or self.whisper.detect(multi_channel_buffer):
        return PrivacyEvent("SPEECH_MUTED")

    # 2. Counter-Forensic Separation
    clean_infrasound = separate_masking_noise(multi_channel_buffer)
    
    # 3. Spatial Acoustics (Where is it coming from?)
    doa_angle = calculate_direction_of_arrival(multi_channel_buffer)
    spatial_heatmap = generate_doa_heatmap(doa_angle)

    # 4. Anti-Jamming & Cryptography
    evidence = self.hasher.seal({
        'spectrogram': clean_infrasound,
        'doa_heatmap': spatial_heatmap,
        'tamper_log': self.imu.get_movement_log()
    })
    
    if network.is_jammed():
        self.local_buffer.save(evidence) # Wait for safe sync
    else:
        self.storage.write(evidence, keys=self.shamir.get_public_shards())
```

---

## 6. Funding Strategy: 2026 Active Pipeline

| Tier | Source | Amount | Focus | Deadline | Status |
|------|--------|--------|-------|----------|--------|
| **Bootstrap** | Internal | €5,000 | CLG Setup, DPO, Sentinel Node Prototype | Immediate | Secured |
| **Rights/Seed** | IHREC Grant (Strand 3) | €22,000 | Digital rights advocacy, survivor triage | 19 May 2026 | Drafting |
| **Environmental**| EPA Research Call 2026 | €330k–€660k | Noise enforcement / Academic Partnership | 28 May 2026 | Pitching |
| **Research** | IRC Enterprise Partnership | €120,000 | Forensics PhD funding | Sept 2026 | Scoping |
| **Scale** | EU Horizon Cluster 3 | €3M+ | Multi-state law enforcement tool | May 2027 | Planned |

---

## 7. Upgraded Risk Register V4.0

| Risk | Likelihood | Impact | Mitigation Strategy | Owner |
|------|------------|--------|---------------------|-------|
| **Hardware/Compute Bottleneck** | High | Critical | Standardize on RPi 5 Sentinel Node; custom ADC Hat for analog multi-sensors. | Tech Lead |
| **Trauma-Cryptography Paradox** | High | High | Implement Shamir’s Secret Sharing (Survivor + AVHERI + NGO) for social key recovery. | DPO / Triage |
| **Hostile Counter-Forensics** | Medium | High | Local offline buffering against Wi-Fi jammers; frequency isolation algorithms against acoustic masking. | Security |
| **Inadmissibility in Court** | Medium | Critical | Implement ISO/IEC 27037 standards; cryptographic timestamping; tamper-evident IMU hardware. | Legal Advisor |
| **"Credibility Trap"** | High | Critical | Enforce "Credibility Ladder" phased rollout; no state engagement without peer review. | Project Lead |

---

## 8. Success Metrics V4.0 (Year 1)

| Domain | Metric | Target | Verification Method |
|--------|--------|--------|---------------------|
| **Governance** | CLG & DPO Appointed | 100% | CRO Certificate / PIA Document |
| **Funding** | 2026 Grants Submitted | 2 | IHREC (May 19) & EPA (May 28) receipts |
| **Research** | Academic Partnership / IRB | 1 | Signed MOU (TCD or DCU) |
| **Hardware** | Sentinel Nodes Deployed | 10 | Device heartbeat logs in MinIO |
| **Hardware** | Spatial Accuracy (DOA) | < 15° error | Lab calibration certificates |
| **Survivor** | Lived Experience Panel | 5 members | Signed agreements |
| **Survivor** | Evidence Packages Generated | 150 | Database query |

---

## 9. Immediate Action Plan: Next 14 Days

| Day | Action | Output | Owner |
|-----|--------|--------|-------|
| 1–3 | **Hardware BOM Draft** | Finalize Bill of Materials for the AVHERI Sentinel Node (RPi5 + ADCs) | Tech Lead |
| 2–4 | **EPA / Academic Pitch** | Deliver 2-page executive summary to TCD/DCU targeting May 28 EPA grant | Research Dir |
| 4–7 | **IHREC Narrative** | Complete draft of €22k grant narrative focusing on privacy & digital rights | Grant Dir |
| 7–10 | **Triage Form v1.1** | Finalize A/B/C Granular Consent logic and Social Recovery protocols | Triage Lead |
| 10–14| **CLG Formation** | Submit Form A1 & Constitution to CRO; setup bank account | Project Lead |

---

## 10. Expanded GitHub Architecture V4.0

```text
📂 AVHERI (GitHub Organization)
│
├── 📂 core-documentation
│   ├── irb-and-ethics/
│   ├── legal-and-standards/
│   │   └── iso-27037-compliance-matrix.md
│   └── measurement-protocols/
│
├── 📂 AVHERI-Sentinel-OS  <-- (NEW: Hardware Repo)
│   ├── hardware-designs/
│   │   └── multi-adc-hat-schematic.kicad
│   ├── firmware/
│   │   └── imu-tamper-monitor.py
│   └── bom-sentinel-node.csv
│
├── 📂 SCADMS-Core
│   ├── src/
│   │   ├── spatial_audio/      # DOA algorithms (ReSpeaker)
│   │   ├── crypto/             # Shamir's Secret Sharing logic
│   │   └── anti_jamming/       # Local SQLite buffer sync
│   └── README.md
│
└── 📂 Survivor-Portal
    ├── frontend/               # Triage v1.1
    └── backend/                # Granular consent handling
```

---

## 11. Appendices

### Appendix A: Sentinel Node Bill of Materials (Estimated)
| Component | Function | Approx. Cost (€) |
|-----------|----------|------------------|
| Raspberry Pi 5 (8GB) | Core Compute / Local AI | €95 |
| ReSpeaker Mic Array v2.0 | Audible & Spatial DOA Tracking | €45 |
| Infiltec INFRASONIC MIC-1 | <20Hz Detection | €450 |
| Knowles SPU0410LR5H-QB | >20kHz Detection | €15 |
| Custom ADC Hat/Interface | Analog to Digital routing | €40 |
| Tamper Enclosure w/ IMU | Anti-tamper & physical security | €30 |
| **Total per Sentinel Node** | | **~€675** |

*(Document Control: V4.0 Strategic Hardware Update completed 2026-04-30)*
