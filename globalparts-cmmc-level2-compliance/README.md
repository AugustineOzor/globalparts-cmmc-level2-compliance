<p align="center"><img src="assets/banner.jpg" alt="CMMC Level 2 Compliance & Supply Chain Security — GlobalParts Manufacturing" width="100%"></p>

# GlobalParts Manufacturing — CMMC Level 2 Compliance & Supply Chain Security

**Overview** · [Asset Inventory](Asset-Inventory.md) · [CUI Data Flows](CUI-Data-Flows.md) · [CMMC Controls](CMMC-Controls.md) · [Supply Chain](Supply-Chain-Vendor-Assessment.md) · [Evidence](Evidence-Register.md) · [SSP & C3PAO Readiness](SSP-and-C3PAO-Readiness.md)

---

## Short Description
A CMMC Level 2 compliance case study for a Tier 2 defence manufacturer. It scopes the CUI environment, maps CUI data flows, implements and rates 14 NIST SP 800-171 controls, assesses sub-tier suppliers, builds an evidence register, and sets out SSP and C3PAO assessment readiness.

![CMMC](https://img.shields.io/badge/CMMC-Level%202-1f2a44) ![NIST](https://img.shields.io/badge/NIST-SP%20800--171%20Rev%202-1f2a44) ![DFARS](https://img.shields.io/badge/DFARS-252.204--7012-1f2a44) ![Frameworks](https://img.shields.io/badge/ISO%2027001%20%7C%20NIST%20CSF%20%7C%20CIS-mapped-1f2a44) ![Status](https://img.shields.io/badge/Status-Complete-2ea043)

## Organisation Context

| Attribute | Detail |
|---|---|
| Organisation | GlobalParts Manufacturing (fictional) |
| Sector | Defence manufacturing — Tier 2 supplier of precision components for military vehicles and aircraft |
| Footprint | HQ in Detroit; production facilities across Michigan and Ohio; 2,500 employees |
| Contract value at stake | ~$50M per year in DoD contracts |
| Requirement | CMMC Level 2 certification by a C3PAO to protect Controlled Unclassified Information (CUI) |
| Role | Compliance Manager |

## Objective
Achieve CMMC Level 2 certification by bringing GlobalParts into conformance with all 110 NIST SP 800-171 requirements. This includes protecting CUI across engineering, the shop floor and the supply chain, and preparing the SSP and evidence a C3PAO will assess.

## Scope
- Assess the current security posture against the 110 NIST SP 800-171 practices
- Implement controls for CUI handling and marking
- Secure the supply chain, including sub-tier suppliers
- Prepare System Security Plan (SSP) documentation
- Coordinate with the CMMC Third-Party Assessment Organization (C3PAO)

## Approach

```mermaid
flowchart LR
    A[Scope the CUI<br/>environment] --> B[Map CUI<br/>data flows]
    B --> C[Implement & rate<br/>controls]
    C --> D[Assess<br/>sub-tier suppliers]
    D --> E[Collect<br/>evidence]
    E --> F[SSP, POA&M &<br/>C3PAO readiness]
```

## Read in Order

| # | Document | What it contains |
|---|---|---|
| 1 | [Asset Inventory](Asset-Inventory.md) | 6 in-scope assets with CMMC asset categories and boundary diagram |
| 2 | [CUI Data Flows](CUI-Data-Flows.md) | 6 data-processing activities tracing CUI from prime to supplier |
| 3 | [CMMC Controls](CMMC-Controls.md) | 14 controls with framework references, CMMC practice mapping and effectiveness ratings |
| 4 | [Supply Chain](Supply-Chain-Vendor-Assessment.md) | 3 supplier assessments: SPRS, CMMC status, DFARS flow-down |
| 5 | [Evidence Register](Evidence-Register.md) | 6 evidence artefacts linked to controls |
| 6 | [SSP & C3PAO Readiness](SSP-and-C3PAO-Readiness.md) | SSP status, POA&M priorities and C3PAO coordination plan |

## Key Results

| Metric | Result |
|---|---|
| Assets in scope | 6 — 3 CUI Asset, 1 Specialized Asset (OT), 2 Security Protection Asset |
| CUI data flows mapped | 6 |
| Controls | 14 — 4 Effective · 7 Partial · 2 Ineffective · 1 Not Tested |
| Suppliers assessed | 3 — 1 Low · 1 Medium · 1 High risk |
| Evidence items | 6 covering 6 of 14 controls |
| SSP | v0.8 — 94 of 110 requirements documented |
| Readiness verdict | 🟠 Not yet ready for C3PAO — 6 priority remediations identified |

## Framework Alignment

| Framework | Use |
|---|---|
| CMMC 2.0 Level 2 (32 CFR Part 170) | Certification target and assessment rules |
| NIST SP 800-171 Rev 2 / 800-171A | 110 security requirements and assessment objectives |
| DFARS 252.204-7012 / 7019 / 7020 / 7021 | Safeguarding, incident reporting, SPRS, CMMC contract clauses |
| ISO/IEC 27001:2022 · NIST CSF 2.0 · CIS Controls v8 | Primary control references |
| DoD CUI Registry & Marking Guide | CUI categories and marking |

## Repository Structure

```
globalparts-cmmc-level2-compliance/
├── README.md
├── assets/
│   └── banner.jpg
├── Asset-Inventory.md
├── CUI-Data-Flows.md
├── CMMC-Controls.md
├── Supply-Chain-Vendor-Assessment.md
├── Evidence-Register.md
└── SSP-and-C3PAO-Readiness.md
```

## Skills Demonstrated
CMMC Level 2 scoping · NIST SP 800-171 control implementation · CUI handling and marking · Supply-chain risk management (DFARS flow-down, SPRS) · Evidence management · SSP and POA&M preparation · C3PAO assessment coordination · Multi-framework control mapping

## Disclaimer
GlobalParts Manufacturing and all suppliers are fictional. This repository contains no real CUI. Regulatory references are summarised for portfolio purposes and are not legal advice.

---

**Author:** Augustine Ozor — AI Governance & Cybersecurity GRC · [GitHub](https://github.com/AugustineOzor) · [LinkedIn](https://linkedin.com/in/augustinetettehozor)

---

**Start here → [Asset Inventory](Asset-Inventory.md)**
