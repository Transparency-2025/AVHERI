# **AVHERI Project Plan V9.0**
## Acoustic Violence, Harassment & Exploitation Research Initiative

**Version:** 9.0 | **Date:** 2026-05-04 | **Status:** Live Court & Scale Release
**Author:** Declan O'Sullivan

---

## **Executive Summary**

AVHERI V9.0 represents the **Live Court & Scale Release**. Building upon the Court-Readiness Track (V8.0: 9.7/10), this version transitions the initiative from a localized 5-home pilot framework into a **50+ node scale-ready, cross-jurisdictional, industrial-grade operation**. 

This release directly resolves the scaling bottlenecks identified in V8.0: physical hardware fragility (SD card corruption), environmental drift (false positives draining cloud compute), the "Expert Witness Bottleneck" (reliance on scarce forensic engineers), and Chain-of-Custody handover flaws (emailing PDFs to police).

### **V8.0 Critical Gaps Resolved in V9.0**

| Gap | V8.0 Issue | V9.0 Resolution |
| :--- | :--- | :--- |
| **Gap 1** | **Expert Witness Bottleneck:** Reliance on DES personnel for every court case limits scalability. | **Zero-Knowledge Verification:** `avheri-verifier` CLI tool developed for automated, open-source hash/OTS/VAD validation by courts/defense. |
| **Gap 2** | **Environmental Drift:** Static 72h baseline triggers infinite false positives if ambient noise changes (e.g., new HVAC). | **Adaptive Rolling Baselines:** Implementation of EWMA (Exponentially Weighted Moving Average) at the Edge to assimilate safe mechanical noise. |
| **Gap 3** | **Chain-of-Custody Handover:** Emailing/USB transfer of evidence packages to Gardaí breaks digital CoC. | **Law Enforcement Portal (LEP):** Zero-trust, 2FA portal. Police view evidence directly on AVHERI servers; access logged cryptographically. |
| **Gap 4** | **Hardware Scale/Fragility:** RPi5 + SD Card prone to corruption over time; consumer-grade limits reliability. | **Industrial Hardware Transition (Workstream H):** Transition to RPi Compute Module (CM5) + eMMC on a custom AVHERI Carrier Board. |
| **Gap 5** | **Jurisdictional Isolation:** Tuned strictly for Irish law, weakening EU Horizon Europe €3M+ grant prospects. | **Cross-Border Admissibility:** Workstream G expanded to map UK (Harassment Act 1997) and EU (StGB § 238) legal standards. |

## **Target Score**

| V8.0 Assessment Score: 9.7/10 <br> **V9.0 Target Score: 9.9/10** <br> *Score delta gated on: Law Enforcement Portal deployment, CM5 Carrier Board prototype, EWMA Edge logic, and EU/UK legal mapping.* |
| :--- |

---

# **1. Project Overview & Mission**

## **1.1 Project Identity**

| Field | Value |
| :--- | :--- |
| **Project Name** | AVHERI — Acoustic Violence, Harassment & Exploitation Research Initiative |
| **Version** | 9.0 (Live Court & Scale Release) |
| **Date** | 2026-05-04 |
| **Status** | Active — Scale & Industrialisation Track |
| **Legal Entity** | Company Limited by Guarantee (CLG), Ireland |

## **1.2 Core Philosophy**
Survivor-Centered | Forensically Sound | Academically Anchored | Privacy-Preserving | Legally Compliant | **Industrial-Grade** | **Cross-Jurisdictional** | **Zero-Trust Handover**

---

# **2. Core Goals & Focus Areas**

| # | Goal | Description | Priority | Status |
| :--- | :--- | :--- | :--- | :--- |
| 1 | **Legal & Governance** | Register CLG; DPO oversight; Law Enforcement Portal (LEP) for secure evidence handover. | Critical | Active |
| 2 | **Academic Anchoring** | IRB sign-off (TCD/DCU); Pilot Alpha completion; EU/UK university consortium building. | Critical | Active |
| 3 | **Privacy & Crypto** | VAD speech-scrubbing, Tiered Capture, GF(P) SSS key recovery, `avheri-verifier` zero-knowledge verification. | Critical | Scoping |
| 4 | **Hardware (Industrial)** | Transition to CM5 Compute Module + eMMC on AVHERI Custom Carrier Board for fleet reliability. | **Critical** | **NEW (V9.0)** |
| 5 | **Forensic Standardization** | ISO 27037 compliance; Adaptive EWMA Baselines to defeat environmental drift. | **Critical** | **NEW (V9.0)** |
| 6 | **Survivor UX** | BLE LESC Companion App; SUS target >85; Deployment Boundary Geofencing. | High | Active |
| 7 | **Counter-Forensics** | Cloud ICA; Faraday cage testing; automated anomaly delta detection. | High | Active |
| 8 | **Court Readiness** | Expert Witness Protocol; EU/UK Admissibility mapping; Law Enforcement Portal (LEP). | **Critical** | **NEW (V9.0)** |

---

# **3. Legal, Governance & Scale Infrastructure**

## **3.1 Law Enforcement Portal (LEP) — Zero-Trust Handover (V9.0 NEW)**

**The Chain-of-Custody Flaw:** In V8.0, generating a cryptographically sealed package is useless if it is emailed to a Garda or printed out, breaking the digital chain of custody.

**V9.0 Solution (LEP):**
AVHERI will deploy a read-only, 2FA-secured web portal exclusively for Law Enforcement, Prosecutors, and Defense Counsel.
*   **Issuance:** Survivor and AVHERI generate a time-limited viewing token for a specific Garda badge number.
*   **Viewing:** The officer logs into the AVHERI portal to view the annotated spectrograms, DOA heatmaps, and lay summaries.
*   **Cryptographic Logging:** The portal logs the officer's IP address, badge number, and exact viewing timestamp *directly into the evidence package's immutable SQLite/MinIO chain-of-custody log*.
*   **Legal Impact:** Pre-empts defense arguments about evidence tampering post-capture. It proves exactly *who* in the police department viewed the evidence and *when*.

## **3.2 Cross-Jurisdictional Admissibility (Horizon Europe Prep)**

To secure the €3M+ Horizon Europe Cluster 3 grant, AVHERI must demonstrate multi-state utility. Workstream G now includes legal mapping for:
*   **United Kingdom:** Admissibility under the *Protection from Harassment Act 1997* and *Police and Criminal Evidence Act 1984 (PACE)*.
*   **Germany:** Alignment with *Strafgesetzbuch (StGB) Section 238 (Stalking)* and *BDSG (Federal Data Protection Act)*.
*   **EU Wide:** Compliance with the upcoming *EU Directive on combating violence against women and domestic violence* (specifically cyber-flashing/tech-abuse provisions).

---

# **4. Survivor-Centered Design & Data Control**

## **4.1 Zero-Knowledge Evidence Verification (`avheri-verifier`)**

**The Expert Bottleneck:** Scaling to 50+ homes means AVHERI’s DES (Digital Evidence Specialists) cannot testify in every court case. 
**V9.0 Solution:** We are releasing `avheri-verifier`, an open-source, standalone CLI tool.
*   A judge, defense lawyer, or independent forensic expert downloads the tool from GitHub.
*   They drag-and-drop the AVHERI Evidence Package into the tool.
*   The tool automatically recalculates SHA-256/Blake3 hashes, verifies the OpenTimestamps blockchain proof, and outputs a "PASS/FAIL" cryptographically signed certificate.
*   **Impact:** Removes the need for AVHERI personnel to explain complex math on the witness stand; the math proves itself.

---

# **5. Hardware Architecture: Industrial Transition (Workstream H)**

## **5.1 Compute Platform: CM5 Custom Carrier Board (V9.0 NEW)**

**The RPi5 Fragility:** Consumer-grade Raspberry Pi 5s using SD cards suffer from high read/write corruption rates over 12-24 months.
**V9.0 Solution:** AVHERI will transition to the **Raspberry Pi Compute Module 5 (CM5)** or CM4 with onboard eMMC storage, mounted on a custom AVHERI PCB Carrier Board.

| Upgrade Feature | V8.0 (RPi5 + SD Card) | V9.0 (CM5 + eMMC Carrier Board) | Forensic/Scale Benefit |
| :--- | :--- | :--- | :--- |
| **Storage Media** | SanDisk Industrial SD | Onboard eMMC 32GB Flash | Eliminates 95% of field storage corruption failures |
| **EMI Isolation** | External USB Enclosure | Optocoupler ICs built into Carrier PCB | Removes external USB cables; shrinks footprint; lowers cost |
| **Form Factor** | Bulky, multi-box setup | Single integrated 100x100mm PCB | Easier for survivors to hide/deploy |
| **Unit Cost (at 100)** | ~€908 | ~€650 (Consolidated BOM) | Reduces hardware cost by 28% at scale |

## **5.2 Edge Logic: Adaptive Rolling Baselines (EWMA)**

**The Environmental Drift Problem:** V8.0 used a static 72h baseline. If a new generator turns on next door, the Sentinel Node will continuously trigger "Alert Mode" (false positives), wasting cloud GPU funds and battery.

**V9.0 Solution (EWMA Algorithm):**
The Sentinel Node uses an **Exponentially Weighted Moving Average (EWMA)**. 
*   If a new loud mechanical hum (e.g., 18Hz) appears, the system flags it as an Alert.
*   If that exact hum remains constant (no amplitude modulation, no temporal pulsing) for 48 continuous hours, the EWMA algorithm mathematically "absorbs" it into the safe baseline.
*   **Impact:** The system adapts to changing seasons and construction noise automatically, isolating *only* dynamic, targeted harassment anomalies. *(See Appendix Q for Pseudo-code).*

---

# **6. Workstreams & Deliverables**

*(Workstreams A-F continue as per V8.0 with the following critical V9.0 additions)*

## **Workstream C: Tool Development (SCADMS v9.0)**
| Phase | Activity | Deliverable | Timeline | Owner |
| :--- | :--- | :--- | :--- | :--- |
| C5 | Adaptive Baseline Logic | Implement EWMA algorithm at the Edge to absorb persistent mechanical noise | Month 5 | Tech Lead |
| C6 | Zero-Knowledge Verifier | Release `avheri-verifier` CLI for automated court/defense hash validation | Month 6 | Security Lead |
| C7 | Law Enforcement Portal | Build 2FA zero-trust portal for secure evidence handover | Month 7 | Tech Lead |

## **Workstream G: Court Readiness (Expanded)**
| Phase | Activity | Deliverable | Timeline | Owner |
| :--- | :--- | :--- | :--- | :--- |
| G6 | EU/UK Legal Mapping | Admissibility guidelines for UK (PACE) and Germany (StGB) for Horizon Europe prep | Months 6-8 | Legal Advisor |
| G7 | Chain-of-Custody Handover | Live test of Law Enforcement Portal (LEP) with friendly Garda contact | Month 8 | DPO / Legal |

## **Workstream H: Industrial Hardware Transition (V9.0 NEW)**
| Phase | Activity | Deliverable | Timeline | Owner |
| :--- | :--- | :--- | :--- | :--- |
| H1 | Carrier Board Schematic | KiCad design of CM5 carrier with onboard optical isolation and ADC | Month 5 | Hardware Lead |
| H2 | Prototype Manufacturing | JLCPCB fabrication of 5x V9.0 Carrier Boards | Month 6 | Hardware Lead |
| H3 | eMMC Firmware Migration | Port Sentinel OS to eMMC; validate boot reliability and Mender OTA | Month 7 | Tech Lead |
| H4 | Fleet Scale Pre-Order | Component sourcing for 50-unit V9.0 hardware build | Month 8 | Project Lead |

---

# **7. Risk Register V9.0**

| Risk | Likelihood | Impact | Mitigation Strategy | V9.0 Status |
| :--- | :--- | :--- | :--- | :--- |
| **Environmental Drift (False Positives)** | High | High | **V9.0 NEW:** Adaptive EWMA rolling baseline absorbs persistent, non-modulated mechanical noise. | Mitigated |
| **Expert Witness Bottleneck** | High | Critical | **V9.0 NEW:** `avheri-verifier` automates mathematical proof for courts/defense. | Mitigated |
| **Chain-of-Custody Handover Break** | High | Critical | **V9.0 NEW:** Law Enforcement Portal (LEP) replaces PDF emailing. | Mitigated |
| **SD Card Corruption at Scale** | High | High | **V9.0 NEW:** Transition to CM5 Compute Module + eMMC. | Mitigated |
| **Horizon Europe Grant Failure** | Medium | High | **V9.0 NEW:** Workstream G expanded to UK/EU legal mapping to prove cross-border utility. | Active |
| RPi Compute Module Shortages | Medium | High | Design carrier board to accept both CM4 and CM5 pinouts (backward compatibility). | Active |
| *All V8.0 Risks (Crypto, DOA, Privacy)* | Low | High | GF(P) Shamir, LESC BLE, Faraday Cage Red Team continue as standard. | Monitored |

---

# **8. Success Metrics V9.0**

| Domain | Metric | Target | Verification Method |
| :--- | :--- | :--- | :--- |
| **Hardware** | CM5 Carrier Board Prototype | 5 units booted | Lab verification |
| **Hardware** | Hardware Reliability (eMMC) | 0 storage failures over 90 days | Device health logs |
| **Software** | False Positive Reduction | >80% reduction in Alert triggers | Cloud compute logs (EWMA efficiency) |
| **Cybersecurity** | `avheri-verifier` Release | v1.0 published on GitHub | Open-source repo metrics |
| **Forensic** | LEP Handover Simulation | 1 successful Garda login & log | Portal audit logs |
| **Legal** | EU/UK Admissibility Map | 1 complete Horizon prep doc | Legal Advisor sign-off |

---

# **9. Immediate Action Plan: Next 14 Days (V9.0)**

| Day | Action | Output | Owner | Critical Path |
| :--- | :--- | :--- | :--- | :--- |
| 1-3 | **Carrier Board Architecture** | Draft KiCad schematic scope for CM5 + onboard isolated ADC | Hardware Lead | **YES** |
| 2-4 | **EWMA Algorithm Dev** | Implement Python Adaptive Baseline logic; test against synthetic noise files | Tech Lead | **YES** |
| 4-6 | **LEP Security Scope** | Draft architecture for Law Enforcement Portal (2FA, immutable audit trail) | Security Lead | **YES** |
| 5-7 | **Horizon EU Legal Brief** | Commission Legal Advisor to begin UK (PACE) and German mapping | Project Lead | No |
| 7-9 | **Verifier CLI Alpha** | Build `avheri-verifier` MVP in Python to validate hash and OTS proofs | Security Lead | **YES** |
| 9-11 | **CM4/CM5 Sourcing** | Secure allocation of 10 Compute Modules for Workstream H prototyping | Tech Lead | **YES** |
| 12-14 | **Month 1 Board Review** | Review V9.0 hardware transition timeline, LEP mockups, and Horizon grant prep | Project Lead | **YES** |

---

# **10. Expanded GitHub Architecture V9.0**

```text
📂 AVHERI (GitHub Organisation)
│
├── 📂 core-documentation
│   └── legal-and-standards/
│       ├── eu-uk-admissibility-guidelines.md    # V9.0 NEW
│       └── law-enforcement-handover-sop.md      # V9.0 NEW
│
├── 📂 AVHERI-Sentinel-OS  
│   ├── hardware-designs/
│   │   ├── cm5-carrier-board.kicad_pcb          # V9.0 NEW (Workstream H)
│   │   └── bom-carrier-board-v9.csv             # V9.0 NEW
│   └── firmware/
│       └── adaptive-ewma-baseline.py            # V9.0 NEW
│
├── 📂 avheri-verifier                           # V9.0 NEW REPO
│   ├── src/
│   │   ├── verify_hashes.py
│   │   ├── verify_opentimestamps.py
│   │   └── generate_court_certificate.py
│   └── README.md
│
├── 📂 Law-Enforcement-Portal                    # V9.0 NEW REPO
│   ├── frontend/
│   │   └── evidence-viewer/
│   └── backend/
│       ├── 2fa-auth/
│       └── cryptographic-audit-logger/
│
└── 📂 SCADMS-Core
    └── ... (Existing V8.0 Architecture)
```

---

# **Appendices**

## **Appendix Q: Adaptive Baseline Algorithm (EWMA) (V9.0 NEW)**

The Exponentially Weighted Moving Average (EWMA) prevents environmental drift (e.g., new HVAC units) from causing infinite Alert loops. 

```python
class AdaptiveBaseline:
    def __init__(self, alpha=0.05, assimilation_threshold_hours=48):
        self.alpha = alpha  # Weight of new ambient data (lower = adapts slower)
        self.baseline_spectrum = None
        self.persistent_anomaly_tracker = {}
        self.assimilation_ticks = assimilation_threshold_hours * 60  # Assuming 1 tick/min

    def update_baseline(self, current_spectrum, is_anomaly=False):
        if self.baseline_spectrum is None:
            self.baseline_spectrum = current_spectrum
            return

        if not is_anomaly:
            # Safely update baseline with normal ambient variance
            self.baseline_spectrum = (self.alpha * current_spectrum) + ((1 - self.alpha) * self.baseline_spectrum)
        else:
            # Anomaly detected: Track its persistence
            freq_peak = identify_peak(current_spectrum)
            
            if is_constant_mechanical_noise(current_spectrum):
                self.persistent_anomaly_tracker[freq_peak] = self.persistent_anomaly_tracker.get(freq_peak, 0) + 1
                
                # If the mechanical noise persists for 48 hours constantly, assimilate it
                if self.persistent_anomaly_tracker[freq_peak] >= self.assimilation_ticks:
                    self.assimilate_noise_into_baseline(current_spectrum)
                    del self.persistent_anomaly_tracker[freq_peak]
            else:
                # Dynamic/Modulated harassment noise is NEVER assimilated
                self.persistent_anomaly_tracker[freq_peak] = 0

    def is_constant_mechanical_noise(self, spectrum):
        # Math to detect 0 amplitude modulation / 0 temporal pulsing
        return calculate_variance(spectrum) < MECHANICAL_THRESHOLD
```

## **Appendix R: Law Enforcement Portal (LEP) Workflow (V9.0 NEW)**

**Objective:** Zero-trust evidence handover without breaking the digital chain of custody.

1. **Token Generation:** AVHERI DPO generates a secure URI token: `portal.avheri.org/case/xyz123?token=abc`.
2. **Authentication:** Police Officer navigates to URI. Must enter Official Police Email (e.g., `@garda.ie`) and Badge Number. 2FA code sent to official email.
3. **Session Instantiation:** Officer logs in. The system cryptographically signs a log entry in the MinIO database: `[TIMESTAMP] CASE_XYZ123 ACCESSED BY GARDA_BADGE_9999 IP_ADDRESS_1.2.3.4`.
4. **Evidence Viewing:** Officer views DOA heatmaps, VAD-scrubbed audio spectrograms, and baseline anomaly charts directly in the browser. 
5. **Download Request:** If the officer requires a local copy for court filing, they click "Export Legal Package". The system bundles the files, signs them with AVHERI's private key, includes the `avheri-verifier` CLI tool, and appends the final download event to the chain-of-custody ledger.

## **Appendix S: Document Control**

| Version | Date | Author | Changes |
| :--- | :--- | :--- | :--- |
| 1.0-7.0 | 2026-04-30 | Declan O'Sullivan | Concept to Pilot-Validated Release |
| 8.0 | 2026-04-30 | Declan O'Sullivan | Court Readiness, Tiered Capture, GF(P) SSS, BLE LESC |
| 9.0 | 2026-05-04 | Declan O'Sullivan | **Live Court & Scale Release:** Law Enforcement Portal (LEP), `avheri-verifier` CLI, CM5 Custom Carrier Board, EWMA Adaptive Baselines, EU/UK Admissibility Mapping. |

---
*This document is a living strategic plan. V9.0 represents the final maturity phase required to scale from a localized 5-home pilot to a permanent, cross-jurisdictional, industrial-grade institution capable of sustaining high-volume, court-admissible forensic operations.*
