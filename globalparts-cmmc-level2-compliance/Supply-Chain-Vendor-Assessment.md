<p align="center"><img src="assets/banner.jpg" alt="CMMC Level 2 Compliance & Supply Chain Security — GlobalParts Manufacturing" width="100%"></p>

[Overview](README.md) · [Asset Inventory](Asset-Inventory.md) · [CUI Data Flows](CUI-Data-Flows.md) · [CMMC Controls](CMMC-Controls.md) · **Supply Chain** · [Evidence](Evidence-Register.md) · [SSP & C3PAO Readiness](SSP-and-C3PAO-Readiness.md)

---

# Supply Chain & Vendor Assessment
**GlobalParts Manufacturing** · Document ID: GP-CMMC-VND-001 · Version 1.0 · Classification: Internal (portfolio sample — contains no real CUI)

## Purpose
Assesses sub-tier suppliers and service providers that handle CUI or have access to CUI systems. DFARS 252.204-7012(m) requires the clause to be flowed down to subcontractors handling covered defence information, and CMMC requires subcontractors to hold the CMMC level appropriate to the information they handle.

## Assessment Criteria
| Criterion | What is checked |
|---|---|
| CUI access | Does the supplier receive, store or process CUI, or administer CUI systems? |
| SPRS score | NIST SP 800-171 assessment score in SPRS (range −203 to 110) |
| CMMC Level 2 status | Final, Conditional (open POA&M), self-assessment only, or none |
| DFARS 7012 flow-down | Clause present in purchase order or master services agreement |
| CUI transfer method | Secure gateway vs. non-compliant channels (e.g., email) |

## Supplier Summary

| ID | Name | Service | Criticality | Status | Renewal | SPRS | CMMC L2 | Rating |
|---|---|---|---|---|---|---|---|---|
| [V-01](#v-01) | Precision Thermal Treating Inc. | Heat treatment and stress relieving of machined aircraft and vehicle components (sub-tier supplier) | 🔴 Critical | 🟢 Active | 2027-03-31 | 104 | Final Level 2 (C3PAO) certification — valid | 🟢 Low Risk |
| [V-02](#v-02) | Midwest Plating & Anodizing LLC | Cadmium-alternative plating and anodizing of aluminium housings (sub-tier supplier) | 🟠 High | 🟡 Under Review | 2026-12-31 | -12 | Not assessed — self-assessment only | 🔴 High Risk |
| [V-03](#v-03) | NorthStar IT Managed Services | Managed security service provider: SIEM monitoring, patching and help desk for CUI enclave (External Service Provider) | 🔴 Critical | 🟢 Active | 2027-06-30 | 98 | Conditional Level 2 (C3PAO) — 2 POA&M items open | 🟡 Medium Risk |

## Supplier Details

### V-01
**Precision Thermal Treating Inc.**

| Field | Value |
|---|---|
| Service | Heat treatment and stress relieving of machined aircraft and vehicle components (sub-tier supplier) |
| Criticality | 🔴 Critical |
| Owner | Supply Chain Security Manager |
| Status | Active |
| Contract renewal | 2027-03-31 |
| CUI access | Yes — heat-treat specs and part drawings (CUI//SP-CTI) |
| SPRS score | 104 / 110 |
| CMMC L2 status | Final Level 2 (C3PAO) certification — valid |
| DFARS 7012 flow-down | Yes — in all POs |
| CUI transfer method | Secure file transfer gateway |
| Assessment rating | 🟢 Low Risk |
| Governing control | [CC-13](CMMC-Controls.md#cc-13) |

**Notes.** Sole qualified heat-treater for 3 military programmes, so supply continuity is critical. Holds CMMC Level 2 C3PAO certification; certificate and SPRS score verified in SPRS/eMASS. 6 points short of perfect score due to two documented POA&M items (FIPS encryption on one workstation; IR test overdue), both within the 180-day closeout window. Uses the GlobalParts gateway for all drawings.

**Required actions.** Re-verify certification and POA&M closeout before renewal. Qualify a second heat-treat source to reduce single-supplier dependency.

### V-02
**Midwest Plating & Anodizing LLC**

| Field | Value |
|---|---|
| Service | Cadmium-alternative plating and anodizing of aluminium housings (sub-tier supplier) |
| Criticality | 🟠 High |
| Owner | Supply Chain Security Manager |
| Status | Under Review |
| Contract renewal | 2026-12-31 |
| CUI access | Yes — plating specifications and drawings (CUI//SP-CTI) |
| SPRS score | -12 / 110 |
| CMMC L2 status | Not assessed — self-assessment only |
| DFARS 7012 flow-down | Yes — clause added at last PO revision |
| CUI transfer method | Email (non-compliant) — gateway onboarding pending |
| Assessment rating | 🔴 High Risk |
| Governing control | [CC-13](CMMC-Controls.md#cc-13) |

**Notes.** SPRS self-assessment score of −12 indicates major gaps (no MFA, no SIEM, incomplete SSP). Still receiving CUI drawings by unencrypted email, breaching GlobalParts' CUI handling procedure and AC.L2-3.1.3/SC.L2-3.13.8 expectations. Contract renewal is in 2 months.

**Required actions.** Stop CUI email transfers immediately; onboard to secure gateway within 30 days. Require a documented POA&M and evidence of progress toward Level 2 before renewal. If no credible plan, limit to non-CUI work or source an alternative supplier.

### V-03
**NorthStar IT Managed Services**

| Field | Value |
|---|---|
| Service | Managed security service provider: SIEM monitoring, patching and help desk for CUI enclave (External Service Provider) |
| Criticality | 🔴 Critical |
| Owner | IT Security Lead |
| Status | Active |
| Contract renewal | 2027-06-30 |
| CUI access | Yes — administrative access to CUI and Security Protection Assets |
| SPRS score | 98 / 110 |
| CMMC L2 status | Conditional Level 2 (C3PAO) — 2 POA&M items open |
| DFARS 7012 flow-down | Yes — DFARS 7012 and CMMC clauses in MSA |
| CUI transfer method | Not applicable — remote admin via PAM with MFA and session recording |
| Assessment rating | 🟡 Medium Risk |
| Governing control | [CC-13](CMMC-Controls.md#cc-13) |

**Notes.** As an External Service Provider with admin access, NorthStar is in GlobalParts' CMMC assessment scope and must be listed in the SSP with a customer responsibility matrix. Conditional certification: 2 open POA&M items (audit-log retention, vulnerability-scan coverage) must close within 180 days or status lapses.

**Required actions.** Obtain and attach the shared responsibility matrix to the SSP. Track POA&M closure monthly. Confirm all NorthStar staff accessing CUI are US persons per ITAR/export-control requirements.

## Key Finding
**V-02 Midwest Plating & Anodizing** is still receiving CUI drawings by unencrypted email and has an SPRS self-assessment score of −12, with renewal due 2026-12-31. Stop email transfers immediately, and make renewal conditional on gateway onboarding and a credible POA&M toward Level 2.

> Suppliers are fictional.

---

← Previous: [CMMC Controls](CMMC-Controls.md) · [↑ Overview](README.md) · **Next: [Evidence](Evidence-Register.md) →**
