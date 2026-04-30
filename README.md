# AVHERI Project Plan V3.0
## Acoustic Violence, Harassment & Exploitation Research Initiative

**Version:** 3.0 | **Date:** 2026-04-30 | **Status:** Strategic Enhancement Release

---

## Executive Summary

AVHERI V3.0 represents a comprehensive strategic upgrade integrating institutional credibility safeguards, privacy-preserving technology architecture, survivor-centered design principles, and a validated funding pipeline. This plan addresses critical gaps identified in V2.0: legal entity formation, GDPR/wiretapping risk mitigation, survivor co-design, and phased institutional engagement.

---

## 1. Project Overview & Mission

**Project Name:** AVHERI — Acoustic Violence, Harassment & Exploitation Research Initiative

**Mission:** To systematically research, document, and combat acoustic violence and tech-facilitated acoustic abuse through an empirically rigorous, privacy-preserving, and forensic-grade knowledge base that empowers survivors, informs policy, and equips legal and law enforcement frameworks.

**Core Philosophy:** *Survivor-Centered, Forensically Sound, Academically Anchored, Privacy-Preserving, Legally Compliant.*

---

## 2. Core Goals & Focus Areas

| # | Goal | Description | Priority | Status |
|---|------|-------------|----------|--------|
| 1 | **Legal Entity & Governance** | Register AVHERI as a Company Limited by Guarantee (CLG); establish Ethics Review Subcommittee and appoint Data Protection Officer (DPO) | **Critical (Immediate)** | Not Started |
| 2 | **Academic Anchoring & IRB** | Secure a core university partnership (TCD, DCU, or UCD) to act as Institutional Review Board (IRB) host | **Critical (Immediate)** | Not Started |
| 3 | **Privacy-Preserving Technology** | Build forensic-grade detection tools with Edge VAD speech-scrubbing, spectrogram-first logging, and zero raw audio retention | **Critical** | Scoping |
| 4 | **Survivor-Centered Design** | Establish Lived Experience Advisory Panel; co-design all intake, tools, and referral pathways | **Critical** | Not Started |
| 5 | **Research & Documentation** | Establish peer-reviewed knowledge base covering audible, infrasound (<20Hz), and ultrasound (>20kHz) mechanisms | High | Not Started |
| 6 | **Triage & Survivor Support** | Develop standardized, evidence-based triage protocols with legal/referral pathways | High | Not Started |
| 7 | **Public & Institutional Awareness** | Educate public, policymakers, and law enforcement on Tech-Facilitated Acoustic Abuse & Anti-Social Behaviour | High | Not Started |
| 8 | **Policy & Sustainable Funding** | Secure multi-tier funding (bootstrap → seed → research → scale) for long-term legislative impact | Medium | Not Started |

---

## 3. Legal & Governance Infrastructure

### 3.1 Legal Entity: Company Limited by Guarantee (CLG)

**Rationale:** A CLG is the minimum viable legal structure for grant eligibility, limited liability, and institutional credibility in Ireland. [^11^]

| Requirement | Details | Timeline | Cost |
|-------------|---------|----------|------|
| **Director Residency** | At least one EEA-resident director required (Declan O'Sullivan qualifies as Ireland-based) | Immediate | — |
| **Registered Office** | Dublin-based registered office address (professional service recommended for privacy) | Immediate | ~€300/year |
| **Company Constitution** | Objects clause must include research, advocacy, and technology development | Week 1 | Legal fees ~€500 |
| **CRO Filing** | Submit Form A1, constitution, and fee via CRO online portal | Week 1–2 | €50 filing fee |
| **IPN/VIF (if needed)** | Identified Person Number for non-EEA directors (not applicable) | N/A | N/A |

**Total Estimated Setup Cost:** €1,500–€2,000

**Alternative Structures Considered:**
- *Unincorporated Association:* Zero cost, no liability protection, cannot hold grants directly — rejected for insufficient credibility
- *Fiscal Host (Open Collective):* Grant-eligible but less credibility with Irish agencies — rejected for jurisdiction mismatch

### 3.2 Governance Structure

```
Board of Directors (CLG)
├── Chair (Independent — legal/compliance background)
├── Project Lead (Declan O'Sullivan)
├── Research Director (University partner)
├── Survivor Advocate (Lived Experience Panel representative)
└── Independent Member (Data protection / ethics expert)

Executive Team
├── Project Lead (Declan O'Sullivan)
│   ├── Academic & Research Director
│   │   ├── University Liaison (IRB Coordinator)
│   │   ├── Frequency Analysts (Infrasound/Ultrasound)
│   │   └── Forensic Standards Team
│   ├── Technology & Privacy Lead
│   │   ├── SCADMS / Edge VAD Developers
│   │   ├── Hardware Integration (Sensors)
│   │   └── Infrastructure & Cryptographic Hashing
│   ├── Survivor Triage & Advocacy Lead
│   │   ├── Intake Coordinator (Triage Protocol)
│   │   ├── Legal Policy Advisor
│   │   └── NGO Coordination
│   └── Communications & Grant Director
│       ├── EU/IRC/EPA Grant Writing
│       ├── Agency Outreach (EPA, Gardaí)
│       └── Digital Content Team

Independent Oversight
├── Ethics Review Subcommittee
│   ├── Survivor Advocate (paid honoraria)
│   ├── Data Protection Officer (DPO) — mandatory under GDPR
│   └── Independent Acoustic Engineer
└── Lived Experience Advisory Panel (3–5 members)
```

### 3.3 Data Protection Officer (DPO) — Mandatory Appointment

Under GDPR Article 37, a DPO is mandatory when processing special category data (health data from acoustic harassment reports) on a large scale.

| DPO Responsibility | Implementation |
|---------------------|----------------|
| Privacy Impact Assessment (PIA) | Conduct before any data collection begins |
| Data Retention Policy | 90-day auto-destruct for raw spectrograms; 7-year retention for hashed metadata |
| Subject Access Requests | 30-day response protocol |
| Breach Notification | 72-hour reporting to Data Protection Commission |
| Annual Compliance Audit | Independent review of all data handling practices |

**DPO Appointment:** External consultant (€5,000–€10,000/year) or trained internal staff member with no conflict of interest.

---

## 4. Survivor-Centered Design (V3.0 Critical Addition)

### 4.1 Lived Experience Advisory Panel

| Element | Specification |
|---------|--------------|
| **Composition** | 3–5 survivors recruited via SAFE Ireland, Threshold, or FLAC referral |
| **Recruitment** | Trauma-informed approach; no obligation to share personal stories |
| **Compensation** | €150 per session honorarium; travel expenses covered |
| **Meetings** | Monthly for first 6 months; quarterly thereafter |
| **Scope** | Review all intake forms, tool UX, referral pathways, and public messaging |

### 4.2 Trauma-Informed Principles

All staff and volunteers must complete HSE-approved trauma-informed care training before engaging with survivors.

### 4.3 Granular Consent Model

Survivors choose their participation level at intake:

| Level | Data Shared | Use Case |
|-------|-------------|----------|
| **A — Anonymous Research Only** | Spectrogram metadata, dB logs, no identifiers | Aggregate research; policy advocacy |
| **B — Identifiable Legal Support** | Contact details + evidence package | Legal referral; individual advocacy |
| **C — Full Research Participation** | All data + interview consent | Longitudinal study; peer-reviewed publication |

**Safe Exit Protocol:** Any survivor can request complete data deletion and disengagement without penalty or explanation. Deletion confirmed within 72 hours.

### 4.4 Revised Triage Protocol v1.1

```
Step 1: SAFETY CHECK
├── Immediate risk assessment (self-harm, physical danger)
├── Emergency services referral if required
└── Crisis support resources provided

Step 2: CONSENT & DATA CONTROL
├── Explain granular consent model (A/B/C)
├── Document consent digitally with timestamp
└── Provide Safe Exit information

Step 3: ENVIRONMENTAL CONTEXT
├── Housing type (apartment, house, shared accommodation)
├── Known or suspected sources
├── Duration and pattern of incidents
├── Previous reports (Gardaí, landlord, EPA)
└── Existing documentation (photos, videos, logs)

Step 4: MEASUREMENT FEASIBILITY
├── Hardware availability (UMIK-1, smartphone, none)
├── Technical capacity assessment
├── Installation support offered
└── Calibration schedule established

Step 5: SUPPORT NEEDS MAPPING
├── Legal (housing, harassment order, criminal complaint)
├── Medical (sleep clinic, ENT, mental health)
├── Housing (relocation, landlord negotiation)
├── Mental health (counseling, peer support)
└── Disability supports (if applicable)

Step 6: EVIDENCE PACKAGE GENERATION (if consented)
├── Spectrogram and dB log capture
├── Cryptographic hashing (SHA-256 + Blake3)
├── Timestamp attestation (OpenTimestamps)
├── Chain-of-custody documentation
└── Legal review flag (if Level B or C)

Step 7: REFERRAL PATHWAY ACTIVATION
├── Automated NGO matching based on needs + location
├── Direct introduction to legal aid (FLAC, PILA)
├── Housing advocacy (Threshold, Simon Communities)
├── Disability rights (DFI, Inclusion Ireland)
└── Follow-up scheduling (7-day, 30-day, 90-day)
```

---

## 5. Workstreams & Deliverables

### Workstream A: Research & Evidence Base

| Phase | Activity | Deliverable | Timeline | Owner |
|-------|----------|-------------|----------|-------|
| A1 | **Academic Anchor & IRB Approval** | Formal MOU with university; full Ethical Review clearance | Months 1–2 | Research Director |
| A2 | **Literature Review & Gap Analysis** | Annotated bibliography (infrasound, ultrasound, targeted acoustic tech) | Months 1–3 | Research Team |
| A3 | **Triage Protocol Development** | Standardized intake metrics; survivor panel review; v1.1 release | Months 2–3 | Triage Lead |
| A4 | **Field Study Protocol** | Standardized measurement arrays; health impact correlation datasets | Months 4–12 | Research Team |
| A5 | **Forensic & Evidentiary Standards** | Chain-of-custody protocols; cross-jurisdictional admissibility guidelines | Months 6–12 | Forensic Team |
| A6 | **Peer Review & Publication** | Methodology paper; health impact study; conference presentations | Months 9–18 | Research Director |

**Key Research Questions:**
1. Psychoacoustic mechanisms of harassment (masking, amplitude modulation, directional audio, bone conduction)
2. Health impacts: sleep architecture disruption, HRV stress markers, cortisol elevation, PTSD symptomatology
3. Infrasound (<20Hz) and ultrasound (>20kHz) detection in residential environments
4. EM-acoustic correlation patterns in reported harassment cases
5. Legal definitions and evidentiary standards across Irish, UK, and EU jurisdictions
6. Intersection with disability rights (sensory processing conditions, autism, hyperacusis)

### Workstream B: Public Awareness & Institutional Education

| Phase | Activity | Deliverable | Timeline | Owner |
|-------|----------|-------------|----------|-------|
| B1 | **Brand & Messaging Framework** | Style guide; survivor-sensitive language; "Tech-Facilitated Abuse" framing | Month 1 | Communications Lead |
| B2 | **Digital Presence** | Central hub website; open-source repositories; educational resources | Months 1–2 | Tech Lead |
| B3 | **Survivor Triage Portal** | Secure, guided intake form; GDPR-compliant; legally admissible logging | Month 3 | Triage Lead |
| B4 | **Law Enforcement & Agency Training** | Modules for Gardaí, EPA, housing associations — framed around modern ASB | Months 6–12 | Advocacy Lead |
| B5 | **Media Engagement** | Press kits; expert spokesperson training; embargo protocols | Months 9–12 | Communications Lead |

**Awareness Campaign Themes:**
- **"Sound Can Be a Weapon"** — Public education on non-obvious acoustic threats
- **"Document, Don't Suffer"** — Empowering survivors with forensic tools
- **"Hear the Unheard"** — Advocacy for regulatory recognition of infrasound/ultrasound
- **"Tech-Facilitated Abuse"** — Framing that resonates with existing domestic violence and cybercrime frameworks

### Workstream C: Tool Development (Privacy-Preserving Tech Stack)

#### SCADMS v3.0 Architecture

| Layer | V2.0 Specification | V3.0 Enhancement | Rationale |
|-------|-------------------|------------------|-----------|
| **Speech Scrubbing** | Silero VAD | Silero VAD + on-device Whisper Tiny verification | False negatives in VAD could leak speech; secondary verification eliminates residual risk |
| **Storage** | SQLite local | SQLite + encrypted S3-compatible backup (MinIO) with survivor-controlled encryption keys | Local-only risks evidence loss; encrypted cloud with client-side keys maintains zero-knowledge for AVHERI |
| **Hashing** | SHA-256 | SHA-256 + Blake3 + OpenTimestamps attestation | Multiple hash algorithms resist future cryptanalysis; timestamp attestation proves temporal existence |
| **Frequency Coverage** | UMIK-1 (20Hz–20kHz) | UMIK-1 + Infiltec INFRASONIC MIC-1 + Knowles SPU0410LR5H-QB | Full spectrum coverage; modular hardware abstraction layer |
| **Data Retention** | Unspecified | 90-day auto-destruct for raw spectrograms; 7-year for hashed metadata | GDPR Article 5(1)(e) storage limitation; minimizes breach impact |
| **Output Format** | Spectrogram + dB log | Spectrogram + dB log + EM correlation flag + weather data (Met Éireann API) | Environmental context strengthens forensic validity |

**SCADMS v3.0 Pseudocode:**

```python
class SCADMSPipeline:
    def __init__(self):
        self.vad = SileroVAD(threshold=0.5)
        self.whisper = WhisperTiny(local=True, quantized=True)
        self.hasher = MultiHash(sha256=True, blake3=True)
        self.retention = RetentionPolicy(raw_days=90, metadata_years=7)
        self.storage = EncryptedStorage(
            local_path="./evidence",
            remote_endpoint="minio.avheri.org",
            client_side_encryption=True,
            survivor_key_escrow=True
        )

    def process(self, audio_buffer: AudioBuffer) -> EvidencePackage:
        # Layer 1: Real-time VAD
        speech_prob = self.vad(audio_buffer)
        if speech_prob > 0.5:
            return PrivacyEvent("SPEECH_DETECTED", scrub=True, log_only=True)

        # Layer 2: Secondary verification
        whisper_segments = self.whisper.transcribe(audio_buffer, max_length=3)
        if whisper_segments and whisper_segments[0].confidence > 0.3:
            return PrivacyEvent("SPEECH_VERIFIED", scrub=True, log_only=True)

        # Layer 3: Safe processing
        spectrogram = generate_spectrogram(
            audio_buffer,
            freq_range=(0.1, 96000),
            resolution="high",
            format="lossless_png"
        )
        db_log = extract_db_metrics(audio_buffer, 
                                   bands=["infrasound", "audible", "ultrasound"])
        em_reading = get_em_correlation()  # Optional EM sensor
        weather = get_met_eireann_data()   # Environmental context

        # Layer 4: Cryptographic sealing
        evidence_package = self.hasher.seal({
            'spectrogram': spectrogram,
            'db_log': db_log,
            'em_reading': em_reading,
            'weather': weather,
            'timestamp': utc_now(),
            'gps': get_location(accuracy="building_level"),
            'hardware_config': get_hardware_profile(),
            'software_version': SCADMS_VERSION
        })

        # Layer 5: Secure storage with retention
        self.storage.write(evidence_package)
        self.retention.schedule_destruction(evidence_package.id)

        return evidence_package
```

#### Complete Tool Ecosystem

| Tool | Description | Tech Stack | Hardware | Status | License |
|------|-------------|------------|----------|--------|---------|
| **SCADMS v3.0** | Real-time acoustic attack detection with full privacy stack | Python, Silero VAD, Whisper Tiny, SQLite, MinIO | UMIK-1, Infiltec MIC-1, Knowles ultrasonic | Scoping | AGPL-3.0 |
| **AuraConv** | Web-based audio filter with polarity inversion and customizable masking | JavaScript/JSFX, Cloudflare Workers | Browser-only | In Dev | MIT |
| **Forensic Audio Web App** | One-click emergency recorder with chain-of-custody | HTML5, Web Audio API, Web Crypto API | Smartphone microphone | In Dev | MIT |
| **Survivor Portal** | Secure intake, consent management, referral matching | Next.js, PostgreSQL, Row-Level Security | Web browser | Planned | AGPL-3.0 |
| **Evidence Validator** | Third-party verification of evidence package integrity | Python, standalone CLI | None | Planned | MIT |

### Workstream D: Organizational Engagement & Funding Pipeline

#### Target Stakeholder Map

| Category | Organizations | Engagement Objective | Phase |
|----------|---------------|---------------------|-------|
| **Academic Anchor** | TCD Acoustics & Physics, DCU Forensic Science, UCD | IRB approval, lab calibration, joint research, PhD supervision | Phase 1 (Silent) |
| **Government/Regulatory** | EPA, Dept of Justice, An Garda Síochána, Dept of Housing | Policy inclusion, noise enforcement guidelines, training | Phase 3–4 |
| **NGOs & Legal** | FLAC, SAFE Ireland, Threshold, Simon Communities, Pavee Point | Survivor referral, joint advocacy, rights defense | Phase 2–3 |
| **Disability Rights** | Disability Federation of Ireland, Inclusion Ireland, AsIAm | Intersectional advocacy, accessibility standards | Phase 2–3 |
| **Professional Bodies** | Irish Acoustical Society, Engineers Ireland | Technical credibility, expert witness pool | Phase 2 |
| **International** | WHO, EU FRA, Council of Europe, ENNHRI | Standards alignment, cross-border cases | Phase 4 |

#### Phased Institutional Engagement: Credibility Ladder

**Phase 1 (Months 1–3): Silent Research**
- No public claims or media engagement
- University MOU negotiation (TCD Physics / DCU Forensic Science)
- IRB application preparation
- Tool alpha testing with closed survivor group (5–10 participants)
- Lived Experience Panel establishment

**Phase 2 (Months 4–6): Academic Validation**
- First peer-reviewed submission (methodology paper)
- Conference poster (Irish Acoustical Society annual meeting)
- Quiet briefing to EPA technical staff (relationship-building, not advocacy)
- NGO partnership MOUs (FLAC, Threshold)

**Phase 3 (Months 7–9): Controlled Visibility**
- White paper release with university co-branding
- Survivor Portal public beta
- Media engagement via university press office only
- Community workshop pilots (housing associations, disability groups)

**Phase 4 (Months 10–12): Policy Entry**
- Formal EPA consultation submission
- Gardaí training module (only after peer-reviewed publication)
- Oireachtas committee briefing request
- EU FRA stakeholder engagement

**Critical Rule:** No law enforcement or government training engagement until at least one peer-reviewed publication exists. Premature engagement risks dismissal and permanent credibility damage.

---

## 6. Funding Strategy: Tiered & Parallel

### 6.1 Funding Tiers

| Tier | Source | Amount | Purpose | Timeline | Probability |
|------|--------|--------|---------|----------|-------------|
| **Bootstrap** | Founder/Personal | €5,000 | CLG registration, initial hardware, honoraria, DPO retainer | Immediate | 100% |
| **Seed** | Community Fundraising (Open Collective) + IHREC Grant | €15,000–€29,000 | SCADMS v3.0 development, survivor panel, legal review | Months 1–3 | 70% |
| **Research** | IRC Enterprise Partnership Scheme | €80,000–€150,000 | PhD/postdoc salary, university overhead, field study | Next call (Sept 2026) | 40% |
| **Scale** | EU Horizon Europe Cluster 3 (2027 call) | €2M–€5M | Multi-country study, policy toolkit, commercialization | 2027 | 25% |
| **Environmental** | EPA Research Programme 2027 | €330,000–€660,000 | Noise pollution intersection, environmental health | 2027 call | 35% |
| **Tech** | NGI (Next Generation Internet) / SFI | €50,000–€200,000 | Privacy-preserving tech, open-source tooling | Rolling | 30% |
| **Rights** | IHREC Human Rights & Equality Grants | €7,000–€22,000 | Disability rights intersection, digital rights advocacy | Annual (May deadline) | 60% |

### 6.2 Active Funding Opportunities (Verified)

#### IHREC 2026-27 Human Rights & Equality Grants Scheme [^14^]
- **Deadline:** 3pm, Tuesday 19 May 2026
- **Total Pool:** €350,000
- **Small Grants:** Up to €7,000
- **General Grants:** Up to €22,000
- **Eligible:** CLG-registered civil society organizations
- **Relevant Strand:** "Advancing the promotion and protection of human rights and equality in the digital environment, including the application of artificial intelligence"
- **Action Required:** Register for info session (15, 16, or 21 April 2026); submit application by 19 May 2026
- **Strategic Fit:** AVHERI's privacy-preserving tech and digital rights framing aligns with Strand 3

#### EPA Research Call 2026 [^1^] [^4^]
- **Status:** OPEN (opened 2 April 2026)
- **Deadline:** 28 May 2026, 16:00 IST
- **Total Pool:** €10.5 million
- **Relevant Themes:**
  - *Policy Implementation, Effective Regulation and Innovative Governance Models* (€330,000, 24 months)
  - *Strengthening the Environmental Dimension of One Health in a Changing Climate* (€660,000, 48 months)
- **Strategic Fit:** Acoustic violence as environmental health threat; noise pollution as public health issue
- **Constraint:** Requires academic partner as lead applicant; AVHERI would be enterprise partner
- **Action Required:** Immediate outreach to TCD/DCU/UCD to co-develop proposal by 28 May 2026

#### IRC Enterprise Partnership Scheme [^6^] [^7^]
- **Next Call:** Expected September 2026 (for funding from September 2027)
- **Amount:** €22,000/year stipend + €3,250 research expenses + fee contribution
- **Enterprise Partner Contribution:** €9,500/year (waivable for NGOs in Year 1)
- **Strategic Fit:** PhD researcher focused on acoustic forensics; AVHERI as enterprise host
- **Action Required:** Identify academic supervisor by June 2026; draft proposal by August 2026

#### EU Horizon Europe Cluster 3 (2027 Call) [^12^] [^15^] [^19^]
- **Relevant 2027 Topics:**
  - HORIZON-CL3-2027-01-FCT-03: Open topic on enhanced prevention, detection and deterrence of societal issues related to various forms of crime (RIA, ~€3M)
  - HORIZON-CL3-2027-01-FCT-04: Open topic on increasing security of citizens against terrorism, including in public spaces (IA, ~€4M)
- **Eligibility:** Requires 2+ Police Authorities and 2+ CSOs from 3+ EU member states
- **Timeline:** Opens 5 May 2027; deadline 4 November 2027
- **Strategic Fit:** Multi-country acoustic harassment detection; community policing integration
- **Action Required:** Begin consortium building in Q3 2026; identify Police Authority partners

### 6.3 Funding Timeline

```
Month 1–2:  Bootstrap (€5,000) + IHREC application (€22,000)
Month 3:    IHREC outcome (June 2026)
Month 4–5:  EPA application with academic partner (€330,000–€660,000)
Month 5:    EPA outcome (November 2026)
Month 6–8:  IRC Enterprise Partnership preparation
Month 9:    IRC application (September 2026)
Month 12:   IRC outcome (June 2027)
Year 2 Q1:  Horizon Europe consortium building
Year 2 Q2:  Horizon Europe application (May 2027)
Year 2 Q4:  Horizon Europe outcome (2028)
```

---

## 7. Risk Register V3.0

| Risk | Likelihood | Impact | Mitigation Strategy | Owner | Trigger |
|------|------------|--------|---------------------|-------|---------|
| **GDPR / Wiretapping Enforcement** | Medium | Critical | DPO appointment; PIA completion; Edge VAD + Whisper verification; spectrogram-only storage; 90-day retention; Data Protection Authority pre-notification | DPO | Any data breach; regulatory inquiry |
| **"Credibility Trap"** (Conspiracy association) | High | Critical | Strict triage protocol; tier-1 University IRB; no public claims without peer review; survivor panel vetting of all outputs | Research Director | Media inquiry; stakeholder skepticism |
| **Survivor Re-traumatization** | Medium | Critical | Trauma-informed training; mandatory supervision; opt-out at any stage; 72-hour deletion guarantee; no mandatory storytelling | Triage Lead | Survivor complaint; staff observation |
| **Academic Partner Withdrawal** | Medium | High | Dual-track negotiations (TCD + DCU); non-exclusive MOU; 30-day transition clause | Research Director | Partner signals withdrawal |
| **Funding Shortfall** | High | High | Diversified 7-tier pipeline; bootstrap reserve; volunteer model; phased delivery; IHREC as immediate target | Grant Director | <50% of Q1 budget secured |
| **Hardware Supply Chain Failure** | Low | Medium | Pre-order sensors; identify EU-based alternatives (Infiltec DE); 3D-printable microphone capsules; UMIK-1 as fallback | Tech Lead | 4-week delivery delay |
| **Hostile Actor Infiltration** | Medium | High | Contributor verification (GitHub); code signing; no raw audio in repositories; air-gapped evidence processing | Security Lead | Suspicious contributor; code anomaly |
| **Media Misrepresentation** | Medium | High | Embargo protocols; pre-approved quotes only; university press office gatekeeping; no freelance interviews | Communications Lead | Unsolicited media contact |
| **Legal Action by Accused Parties** | Medium | High | Defamation insurance (€500,000 coverage); careful language ("reported," "alleged"); legal defense fund; CLG liability shield | Legal Advisor | Cease and desist received |
| **False Positive Evidence** | Medium | Medium | Rigorous calibration; clear disclaimers; expert validation layer; confidence scoring in evidence packages | Forensic Team | Evidence challenged in legal context |

---

## 8. Success Metrics V3.0 (Year 1)

| Domain | Metric | Target | Verification Method |
|--------|--------|--------|---------------------|
| **Governance** | CLG registered with CRO | 100% | CRO filing confirmation |
| **Governance** | DPO appointed and PIA completed | 100% | Appointment letter; PIA document |
| **Research** | IRB approval obtained | 1 | Ethics committee approval letter |
| **Research** | Peer-reviewed submissions | 2 | Journal submission receipts |
| **Research** | Conference presentations/posters | 1 | Acceptance notification |
| **Funding** | Grant applications submitted | 3 (IHREC, EPA, IRC) | Submission confirmations |
| **Funding** | Seed funding raised | €29,000 | Bank statements |
| **Technical** | SCADMS v3.0 alpha released | 1 | GitHub release tag |
| **Technical** | Full-spectrum hardware tested | 3 sensor types | Calibration certificates |
| **Technical** | Privacy audit passed | 100% | Independent auditor report |
| **Survivor** | Lived Experience Panel convened | 5 members | Signed participation agreements |
| **Survivor** | Triage intakes processed | 50 | Anonymized case logs |
| **Survivor** | Evidence packages generated | 150 | Database query |
| **Survivor** | Referrals activated | 100 | NGO confirmation receipts |
| **Impact** | EPA technical briefing | 1 | Meeting minutes |
| **Impact** | NGO partnership MOUs signed | 3 | Signed agreements |

---

## 9. Immediate Action Plan: Next 30 Days

| Day | Action | Output | Owner | Dependency |
|-----|--------|--------|-------|------------|
| 1–2 | Register AVHERI CLG with CRO | Company number assigned; certificate of incorporation | Project Lead | None |
| 2–3 | Open business bank account | Account active; bootstrap funds deposited | Project Lead | CLG registration |
| 2–3 | Draft TCD/DCU partnership proposal (2-page) | Proposal document; target: Physics/Forensic Science | Research Director | None |
| 3–5 | Set up GitHub organization + 4 repos | `AVHERI` org live; initial READMEs; AGPL-3.0 + MIT licenses | Tech Lead | None |
| 3–5 | Register for IHREC info session (15/16/21 April) | Session attendance confirmed; application pack received | Grant Director | None |
| 5–7 | Procure UMIK-1 + initial infrasound sensor | Purchase orders placed; delivery tracked | Tech Lead | Bootstrap funds |
| 5–7 | Draft IHREC grant application (General Grant €22,000) | Application document; budget; project narrative | Grant Director | CLG registration |
| 7–10 | Draft survivor intake form v1.1 | Markdown template; trauma-informed; GDPR-compliant consent flows | Triage Lead | None |
| 7–10 | Build Silero VAD + Whisper proof-of-concept | Python script; demo video; privacy audit checklist | Tech Lead | None |
| 10–12 | Submit IHREC grant application | Application submitted by 19 May 2026 deadline | Grant Director | CLG; intake form |
| 10–14 | Outreach to EPA research team | Expression of interest; academic partner introduction | Research Director | Academic partner identified |
| 12–14 | Submit IRC Enterprise Partnership pre-registration | EOI submitted; academic partner identified | Research Director | Academic partner commitment |
| 14–21 | EPA Research Call 2026 co-development | Joint proposal draft with academic partner | Research Director + Academic Partner | Academic partner MOU |
| 21–28 | EPA application submission | Full application submitted via EPA SmartSimple portal | Research Director | Proposal finalized |
| 28–30 | Month 1 review | Board meeting; milestone assessment; risk register update | Project Lead | All Month 1 deliverables |

---

## 10. GitHub Architecture V3.0

```
📂 AVHERI (GitHub Organization)
│
├── 📂 core-documentation
│   ├── whitepapers/
│   │   ├── acoustic-violence-definitions.md
│   │   ├── infrasound-ultrasound-health-impacts.md
│   │   └── legal-framework-comparison.md
│   ├── irb/
│   │   ├── ethical-review-application.md
│   │   ├── informed-consent-template.md
│   │   └── data-management-plan.md
│   ├── literature-reviews/
│   │   ├── annotated-bibliography.md
│   │   └── research-gaps-analysis.md
│   └── measurement-protocols/
│       ├── umiK-1-calibration-guide.md
│       ├── infrasound-sensor-setup.md
│       └── full-spectrum-array-standard.md
│
├── 📂 SCADMS
│   ├── src/
│   │   ├── pipeline/
│   │   │   ├── __init__.py
│   │   │   ├── vad_layer.py          # Silero + Whisper
│   │   │   ├── spectrogram_engine.py
│   │   │   ├── privacy_filter.py
│   │   │   ├── hashing.py            # SHA-256 + Blake3 + OpenTimestamps
│   │   │   ├── storage.py            # SQLite + MinIO client-side encryption
│   │   │   └── retention.py          # Auto-destruct scheduler
│   │   ├── hardware/
│   │   │   ├── umiK1.py
│   │   │   ├── infrasound.py         # Infiltec MIC-1
│   │   │   └── ultrasound.py         # Knowles SPU0410LR5H-QB
│   │   └── cli/
│   │       └── scadms.py
│   ├── tests/
│   │   ├── test_vad.py
│   │   ├── test_privacy.py
│   │   └── test_hashing.py
│   ├── docs/
│   │   ├── INSTALL.md
│   │   ├── PRIVACY.md
│   │   └── HARDWARE.md
│   ├── LICENSE (AGPL-3.0)
│   └── README.md
│
├── 📂 Forensic-Audio-App
│   ├── src/
│   │   ├── recorder.js
│   │   ├── custody.js                # Chain-of-custody logic
│   │   ├── crypto.js                 # Web Crypto API hashing
│   │   └── ui/
│   ├── tests/
│   ├── docs/
│   ├── LICENSE (MIT)
│   └── README.md
│
├── 📂 Survivor-Resources
│   ├── legal-guides/
│   │   ├── tenant-rights-ireland.md
│   │   ├── harassment-order-guide.md
│   │   ├── garda-reporting-pathway.md
│   │   └── evidence-admissibility.md
│   ├── intake-templates/
│   │   ├── triage-v1.1.md
│   │   ├── consent-form-a.md         # Anonymous
│   │   ├── consent-form-b.md         # Identifiable legal
│   │   └── consent-form-c.md         # Full research
│   ├── hardware-guides/
│   │   ├── umiK-1-setup.md
│   │   ├── smartphone-measurement.md
│   │   └── full-spectrum-upgrade.md
│   └── referral-directory/
│       ├── legal-aid.md
│       ├── housing-advocacy.md
│       ├── disability-rights.md
│       └── mental-health.md
│
└── 📂 .github
    ├── ISSUE_TEMPLATE/
    ├── PULL_REQUEST_TEMPLATE.md
    ├── CODE_OF_CONDUCT.md
    ├── CONTRIBUTING.md
    └── SECURITY.md
```

---

## 11. Appendices

### Appendix A: Glossary of Terms

| Term | Definition |
|------|------------|
| **Acoustic Violence** | The intentional use of sound, infrasound, or ultrasound to cause harm, distress, or coercion |
| **Tech-Facilitated Acoustic Abuse** | Acoustic violence enabled or amplified by digital technology (directional speakers, IoT devices, signal processing) |
| **Edge VAD** | Voice Activity Detection performed on-device, before any data leaves the local system |
| **Spectrogram** | Visual representation of the spectrum of frequencies in an audio signal as they vary with time |
| **Chain of Custody** | Documented trail showing the seizure, control, transfer, analysis, and disposition of evidence |
| **IRB** | Institutional Review Board — ethics committee approving human subjects research |
| **CLG** | Company Limited by Guarantee — Irish not-for-profit corporate structure |

### Appendix B: Hardware Specifications

| Sensor | Frequency Range | Cost (€) | Supplier | Use Case |
|--------|---------------|----------|----------|----------|
| miniDSP UMIK-1 | 20Hz–20kHz | ~€120 | miniDSP | Calibrated audible spectrum measurement |
| Infiltec INFRASONIC MIC-1 | 0.1Hz–20Hz | ~€450 | Infiltec (Germany) | Infrasound detection |
| Knowles SPU0410LR5H-QB | 20kHz–80kHz | ~€15 | Digi-Key/Mouser | Ultrasonic detection |
| RTL-SDR v3 | 500kHz–1.75GHz | ~€30 | Various | EM correlation detection |

### Appendix C: Legal Framework References

| Jurisdiction | Relevant Legislation | Application |
|--------------|---------------------|-------------|
| Ireland | Environmental Noise Regulations 2018 | Noise nuisance enforcement |
| Ireland | Non-Fatal Offences Against the Person Act 1997 | Harassment prosecution |
| Ireland | Domestic Violence Act 2018 | Coercive control including tech-facilitated abuse |
| EU | GDPR 2016/679 | Data protection for all evidence collection |
| EU | ePrivacy Directive 2002/58/EC | Wiretapping and interception restrictions |
| UK | Protection from Harassment Act 1997 | Cross-border case reference |

### Appendix D: Document Control

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2026-04-30 | Declan O'Sullivan | Initial project plan |
| 2.0 | 2026-04-30 | Declan O'Sullivan | Privacy tech, academic anchoring, frequency expansion |
| 3.0 | 2026-04-30 | Declan O'Sullivan | Legal entity, survivor-centered design, funding pipeline, risk hardening, governance structure |

---

*This document is a living strategic plan. All timelines, budgets, and targets should be reviewed monthly by the Board of Directors and updated based on actual progress and emerging opportunities.*
