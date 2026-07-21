<!-- ===== PROFILE HEADER ===== -->

<p align="center">
  <img src="https://raw.githubusercontent.com/warpedatom/warpedatom/main/Dread.png" alt="Velkris banner" width="100%">
</p>

<h1 align="center">Velkris | Offensive Security & Adversary Simulation</h1>

<p align="center">
  <strong>Enterprise Penetration Testing • Active Directory Security • Adversary Emulation • Detection Validation</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/RED_TEAM-C1121F?style=flat-square" alt="Red Team">
  <a href="https://attack.mitre.org/">
    <img src="https://img.shields.io/badge/MITRE_ATT%26CK-Adversary_Emulation-C1121F?style=flat-square" alt="MITRE ATT&CK">
  </a>
   <a href="https://www.powershellgallery.com/packages/OffsetInspect"><img src="https://img.shields.io/powershellgallery/v/OffsetInspect?logo=powershell&logoColor=white&label=OffsetInspect&style=flat-square&color=181717" alt="OffsetInspect on PSGallery"></a>
  <a href="https://crates.io/crates/offsetscan"><img src="https://img.shields.io/crates/v/offsetscan?logo=rust&logoColor=white&label=OffsetScan&style=flat-square&color=C1121F" alt="OffsetScan on crates.io"></a>
  <a href="https://www.linkedin.com/in/perry-jared-r">
    <img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?logo=linkedin&logoColor=white&style=flat-square" alt="LinkedIn">
  </a>
</p>

<p align="center">
  <strong><em>Intrā. Manē. Age.</em></strong><br>
  <sub>Get in. Stay in. Act.</sub>
</p>

---

## About

I am an offensive security practitioner focused on **enterprise penetration testing, Active Directory attack paths, adversary simulation, and detection-informed tradecraft**.

My work emphasizes controlled execution, repeatable methodology, evidence preservation, and clear technical reporting. Offensive security should do more than demonstrate that access is possible. It should identify meaningful attack paths, measure defensive visibility, and produce recommendations that materially reduce organizational risk.

My approach draws from the behaviors and operational patterns of mature criminal and state-sponsored adversaries while remaining bounded by authorization, defined objectives, and rules of engagement.

### Focus Areas

- Active Directory enumeration, exploitation, and privilege escalation
- Kerberos abuse and identity-based attack paths
- Credential access and lateral movement
- MITRE ATT&CK-aligned adversary emulation
- State-sponsored adversary tradecraft analysis
- Offensive tooling and workflow automation
- Windows telemetry and detection validation
- Evidence collection and remediation-focused reporting

---

## Operator Principles

> **Intrā. Manē. Age.**<br>
> **Gain access. Maintain operational influence. Accomplish the authorized objective.**

### Mission Before Technique

A vulnerability, shell, credential, or privileged account is not necessarily the objective. Techniques are selected according to the mission, the target environment, and the agreed rules of engagement.

The value of an operation is measured by whether it answers a meaningful security question—not by the number of tools executed or systems compromised.

### Emulate Behaviors, Not Reputation

Adversary emulation should reproduce relevant behaviors, decision patterns, and attack sequences without attempting to imitate recklessness or cause uncontrolled impact.

State-sponsored and advanced adversaries are studied for their:

- Operational sequencing
- Identity and access tradecraft
- Persistence strategies
- Command-and-control patterns
- Collection priorities
- Defensive evasion techniques
- Target selection and mission focus

The objective is to test whether the organization can recognize and interrupt those behaviors under controlled conditions.

### Assume Visibility, Then Validate It

Operate under the assumption that defensive controls and telemetry exist.

For each meaningful action, determine:

- Whether the behavior was prevented
- Whether telemetry was generated
- Whether an alert was created
- Whether the alert contained sufficient context
- Whether defenders could investigate and respond
- Whether the activity could be correlated across systems

Absence of an alert is a finding. An alert without actionable context may also be a finding.

### Preserve Optionality

Avoid unnecessary disruption, irreversible actions, and premature escalation.

A disciplined operator maintains multiple paths forward, minimizes avoidable exposure, and selects techniques proportionate to the objective. Access should be expanded deliberately rather than indiscriminately.

### Evidence Over Assumption

Every material conclusion should be supported by reproducible evidence.

Evidence should establish:

- What action was performed
- When it occurred
- Which system, identity, or control was involved
- What access or impact was demonstrated
- What telemetry or alerting resulted
- How the attack path could be reproduced
- What remediation would break or reduce the path

### Access Is Not the Finish Line

Initial access demonstrates entry. Persistence demonstrates resilience. Objective completion demonstrates risk.

A complete operation evaluates whether an adversary could:

1. **Get in** — establish an initial foothold
2. **Stay in** — maintain access and continue operating
3. **Act** — achieve the authorized operational objective

The ultimate outcome should be measurable security improvement.

### Authorization Is Absolute

All activity must remain within the approved scope, rules of engagement, and legal authority.

Operational realism never overrides:

- Safety
- Scope boundaries
- Data-handling requirements
- Client constraints
- Stop conditions
- Professional judgment

---

## Assessment Outcomes

A useful assessment should determine:

- Which attack paths present meaningful business risk
- Whether controls prevented, detected, or missed adversary behavior
- What telemetry and alerts were generated
- Whether alerts were timely and actionable
- Whether identities, privileges, or trust relationships could be chained
- Whether access could be maintained after initial compromise
- Whether critical business objectives could be reached
- Which changes would materially reduce the likelihood or impact of compromise

---

## Featured Tooling

A two-part analysis suite for **detection-boundary research and corpus-scale static triage** — read-only, authorization-bounded, built to answer *why* a control fires and *what* an artifact is.

### [OffsetInspect](https://github.com/warpedatom/OffsetInspect) · PowerShell · [PSGallery](https://www.powershellgallery.com/packages/OffsetInspect)

Detection-boundary and byte-offset analysis for authorized detection engineering.

- Maps UTF-8/UTF-16 byte offsets to exact source lines, characters, and bounded hex/ASCII context — streaming, never loading whole files
- Locates AMSI and Microsoft Defender detection boundaries and validates their stability through repeated prefix-search
- Correlates a boundary to the content that triggered it — PE section, pre-boundary entropy, candidate signature strings
- Journals detection drift and attributes change to file modification, signature update, or provider non-determinism
- Authorized signature-robustness testing entirely in memory — no variant written to disk
- Corpus scanning, cross-scan detection diffing, YARA/ClamAV, and Markdown/HTML engagement reports

### [OffsetScan](https://github.com/warpedatom/OffsetScan) · Rust · [crates.io](https://crates.io/crates/offsetscan)

The native, corpus-scale companion engine — JSON schema-compatible with OffsetInspect.

- Parallel PE parsing, entropy, string extraction, and IOC panels across thousands of files
- imphash verified byte-identical to pefile/VirusTotal, including special-library ordinal resolution
- Lenient header salvage recovers triage data from truncated or damaged samples
- Feature-gated `offsetscan yara` subcommand with output identical to OffsetInspect's
- `cargo install offsetscan`

---

## Current Research

- Active Directory compromise paths
- Kerberos authentication and ticket abuse
- Active Directory Certificate Services
- ACL, delegation, and trust abuse
- Cross-domain and cross-forest attack paths
- Lateral movement and remote execution
- Credential access and password auditing
- State-sponsored adversary behaviors
- MITRE ATT&CK technique mapping
- Command-and-control architecture
- PowerShell, Python, Bash, C#, and C
- Windows telemetry and detection validation
- Repeatable penetration testing methodology
- Evidence-driven technical reporting

---

## Technical Stack

### Offensive Security

`Kali Linux` • `Windows Active Directory` • `BloodHound` • `NetExec`
`Impacket` • `Rubeus` • `Mimikatz` • `Responder`
`Hashcat` • `Nmap` • `Nuclei` • `HTTPX` • `Burp Suite`

### Development and Automation

`PowerShell` • `Python` • `Bash` • `C#` • `C`
`Git` • `GitHub Actions` • `pipx` • `venv`

### Adversary Emulation and Detection

`MITRE ATT&CK` • `Windows Event Logs` • `Sysmon` • `Sigma`<br>
`Telemetry Analysis` • `Detection Validation` • `Threat-Informed Testing`

### Documentation and Reporting

`Markdown` • `Obsidian` • `Evidence Tracking`<br>
`Attack-Path Documentation` • `Reporting Templates` • `Remediation Guidance`

---

## Certifications and Training

| Certification / Training | Status |
|---|---|
| CompTIA Security+ | Completed |
| TCM Security PJPT | Completed |
| TCM Security PNPT | Completed |
| Altered Security CRTP | Completed |
| Zero-Point Security CRTO | In Progress |

### Current Development Path

`Active Directory Security → Enterprise Penetration Testing → Red Team Operations → Threat-Informed Adversary Emulation → Detection-Aware Tradecraft → Advanced Tooling`

---

## Connect

<p>
  <a href="https://www.linkedin.com/in/perry-jared-r">LinkedIn</a>
  &nbsp;•&nbsp;
  <a href="https://github.com/warpedatom/OffsetInspect">OffsetInspect</a>
  &nbsp;•&nbsp;
  <a href="https://github.com/warpedatom/Offsetscan">Offsetscan</a>
  &nbsp;•&nbsp;
  <a href="mailto:warped.atom@pm.me">Email</a>
</p>

---

<p align="center">
  <strong><em>Intrā. Manē. Age.</em></strong>
</p>

<p align="center">
  <sub>© 2026 Velkris | Authorized Offensive Security Research</sub>
</p>

<p align="center">
  <sub>
    All testing is performed under explicit authorization in approved professional,
    isolated, or lab-controlled environments for security research, professional
    development, and defensive improvement.
  </sub>
</p>
