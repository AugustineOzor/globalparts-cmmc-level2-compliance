# CMMC Level 2 Controls
**GlobalParts Manufacturing** · Document ID: GP-CMMC-CTL-001 · Version 1.0 · Classification: Internal (portfolio sample — contains no real CUI)

## Purpose
Fourteen specific, testable controls implementing NIST SP 800-171 requirements for CMMC Level 2. Each control has a primary framework reference (ISO/IEC 27001:2022, NIST CSF 2.0 or CIS Controls v8) and a CMMC Level 2 practice mapping.

## Effectiveness Scale
| Rating | Meaning |
|---|---|
| 🟢 Effective | Operating as designed, tested with evidence |
| 🟡 Partially Effective | Operating, but coverage incomplete or gaps known |
| 🔴 Ineffective | Not operating, or failing tests |
| ⚪ Not Tested | Implemented but no test evidence yet |

## Control Summary

| ID | Control | Framework | Ref | CMMC L2 Practice | Effectiveness | Frequency | Owner |
|---|---|---|---|---|---|---|---|
| [CC-01](#cc-01) | Restrict CUI enclave access to authorised users via Entra ID security groups, approved per programme by the Programme Manager | ISO 27001 | A.5.15 | AC.L2-3.1.1 | 🟢 Effective | Continuous | IT Manager |
| [CC-02](#cc-02) | Enforce MFA for all users accessing CUI systems and for all privileged and remote access, using Microsoft Authenticator number matching or FIDO2 keys | NIST CSF | PR.AA-03 | IA.L2-3.5.3 | 🟡 Partially Effective | Continuous | IT Manager |
| [CC-03](#cc-03) | Block CUI from leaving the enclave using sensitivity labels and DLP policies that stop labelled files being emailed or shared with unapproved external domains | ISO 27001 | A.8.12 | AC.L2-3.1.3 | 🟡 Partially Effective | Continuous | IT Security Lead |
| [CC-04](#cc-04) | Mark all CUI — digital files, drawings and printed copies — with CUI banner markings and designation indicators per the DoD CUI Marking Guide | ISO 27001 | A.5.13 | MP.L2-3.8.4 | 🔴 Ineffective | Continuous | Quality Director |
| [CC-05](#cc-05) | Block removable media on CNC controllers and engineering workstations, except one controlled, logged media transfer station per plant | ISO 27001 | A.7.10 | MP.L2-3.8.7 | 🟢 Effective | Continuous | Plant Operations Manager (Ohio) |
| [CC-06](#cc-06) | Collect audit logs from all CUI and Security Protection Assets into the SIEM, retain them for 1 year, and review alerts weekly | CIS Controls | 8.2 | AU.L2-3.3.1 | 🟡 Partially Effective | Continuous | IT Security Lead |
| [CC-07](#cc-07) | Maintain baseline configurations and a complete inventory of all in-scope hardware and software, reviewed quarterly | CIS Controls | 4.1 | CM.L2-3.4.1 | 🟡 Partially Effective | Quarterly | IT Manager |
| [CC-08](#cc-08) | Segment the OT/CNC network from corporate IT and the internet, allowing only the DNC server and MES on defined ports, with deny-by-default firewall rules | CIS Controls | 12.2 | SC.L2-3.13.1 | 🟢 Effective | Continuous | Network Engineer |
| [CC-09](#cc-09) | Encrypt CUI at rest and in transit using FIPS 140-validated cryptographic modules on all CUI assets | NIST CSF | PR.DS-01 | SC.L2-3.13.11 | 🔴 Ineffective | Continuous | IT Security Lead |
| [CC-10](#cc-10) | Operate an incident response capability that reports cyber incidents affecting CUI to DoD via DIBNet within 72 hours and preserves images for 90 days | NIST CSF | RS.MA-01 | IR.L2-3.6.1 | ⚪ Not Tested | Annual | IT Security Lead |
| [CC-11](#cc-11) | Run authenticated vulnerability scans monthly on all in-scope IT assets and remediate critical findings within 15 days | CIS Controls | 7.5 | RA.L2-3.11.2 | 🟢 Effective | Monthly | IT Security Lead |
| [CC-12](#cc-12) | Revoke all CUI system access within 24 hours of termination or transfer, triggered by HR and confirmed by IT | CIS Controls | 6.2 | PS.L2-3.9.2 | 🟡 Partially Effective | Continuous | HR Director |
| [CC-13](#cc-13) | Flow down DFARS 252.204-7012 and CMMC Level 2 requirements to every sub-tier supplier handling CUI, and verify their SPRS score and certification status before releasing CUI | ISO 27001 | A.5.20 | DFARS 252.204-7012(m) / AC.L2-3.1.20 | 🟡 Partially Effective | Quarterly | Supply Chain Security Manager |
| [CC-14](#cc-14) | Maintain a System Security Plan describing the CUI boundary, all 110 NIST SP 800-171 requirements and their implementation, reviewed annually and on significant change | NIST CSF | GV.PO-01 | CA.L2-3.12.4 | 🟡 Partially Effective | Annual | Compliance Manager |

## Effectiveness Summary

| Effectiveness | Count | % |
|---|---|---|
| 🟢 Effective | 4 | 29% |
| 🟡 Partially Effective | 7 | 50% |
| 🔴 Ineffective | 2 | 14% |
| ⚪ Not Tested | 1 | 7% |
| **Total** | **14** | 100% |

## Coverage by NIST SP 800-171 Family

| Family | Controls |
|---|---|
| Access Control (AC) | [CC-01](CMMC-Controls.md#cc-01), [CC-03](CMMC-Controls.md#cc-03) |
| Identification & Authentication (IA) | [CC-02](CMMC-Controls.md#cc-02) |
| Media Protection (MP) | [CC-04](CMMC-Controls.md#cc-04), [CC-05](CMMC-Controls.md#cc-05) |
| Audit & Accountability (AU) | [CC-06](CMMC-Controls.md#cc-06) |
| Configuration Management (CM) | [CC-07](CMMC-Controls.md#cc-07) |
| System & Communications Protection (SC) | [CC-08](CMMC-Controls.md#cc-08), [CC-09](CMMC-Controls.md#cc-09) |
| Incident Response (IR) | [CC-10](CMMC-Controls.md#cc-10) |
| Risk Assessment (RA) | [CC-11](CMMC-Controls.md#cc-11) |
| Personnel Security (PS) | [CC-12](CMMC-Controls.md#cc-12) |
| Supply chain — DFARS 252.204-7012(m) flow-down (DFARS) | [CC-13](CMMC-Controls.md#cc-13) |
| Security Assessment (CA) | [CC-14](CMMC-Controls.md#cc-14) |

## Control Details

### CC-01
**Restrict CUI enclave access to authorised users via Entra ID security groups, approved per programme by the Programme Manager**

| Field | Value |
|---|---|
| Primary framework | ISO 27001 — A.5.15 |
| CMMC L2 / NIST 800-171 | AC.L2-3.1.1 |
| Effectiveness | 🟢 Effective |
| Frequency | Continuous |
| Owner | IT Manager |
| Linked assets | [A-01](Asset-Inventory.md#a-01), [A-02](Asset-Inventory.md#a-02) |
| Linked data flows | [DPA-01](CUI-Data-Flows.md#dpa-01), [DPA-02](CUI-Data-Flows.md#dpa-02) |
| Evidence | [EV-01](Evidence-Register.md#ev-01) |

**Description.** Access to GCC High CUI libraries and PLM projects is granted only through programme-specific security groups. Requests require Programme Manager approval in the ticketing system. There are no direct user assignments.

**Decision rationale.** Effective: sample of 25 access grants all had documented approval. Group membership reconciled against the HR roster with zero exceptions. Unauthorised-access test (non-programme user) was correctly denied.

### CC-02
**Enforce MFA for all users accessing CUI systems and for all privileged and remote access, using Microsoft Authenticator number matching or FIDO2 keys**

| Field | Value |
|---|---|
| Primary framework | NIST CSF — PR.AA-03 |
| CMMC L2 / NIST 800-171 | IA.L2-3.5.3 |
| Effectiveness | 🟡 Partially Effective |
| Frequency | Continuous |
| Owner | IT Manager |
| Linked assets | [A-01](Asset-Inventory.md#a-01), [A-02](Asset-Inventory.md#a-02), [A-03](Asset-Inventory.md#a-03), [A-05](Asset-Inventory.md#a-05) |
| Linked data flows | [DPA-01](CUI-Data-Flows.md#dpa-01), [DPA-04](CUI-Data-Flows.md#dpa-04) |
| Evidence | [EV-02](Evidence-Register.md#ev-02) |

**Description.** Conditional Access requires MFA for every sign-in to the GCC High tenant, the file transfer gateway and admin consoles. Privileged accounts use FIDO2 keys.

**Decision rationale.** Partially effective: enforced for the cloud enclave and gateway (100%). Local logons to the 12 ERP/MES admin servers still use password only. MFA for local and network access to privileged accounts is required by 3.5.3, so the requirement is not fully met.

### CC-03
**Block CUI from leaving the enclave using sensitivity labels and DLP policies that stop labelled files being emailed or shared with unapproved external domains**

| Field | Value |
|---|---|
| Primary framework | ISO 27001 — A.8.12 |
| CMMC L2 / NIST 800-171 | AC.L2-3.1.3 |
| Effectiveness | 🟡 Partially Effective |
| Frequency | Continuous |
| Owner | IT Security Lead |
| Linked assets | [A-02](Asset-Inventory.md#a-02), [A-05](Asset-Inventory.md#a-05) |
| Linked data flows | [DPA-01](CUI-Data-Flows.md#dpa-01), [DPA-04](CUI-Data-Flows.md#dpa-04) |
| Evidence | — |

**Description.** Microsoft Purview labels (CUI//SP-CTI) are applied on ingest. DLP blocks external sharing except to allow-listed prime and supplier domains, which must go through the secure gateway.

**Decision rationale.** Partially effective: DLP blocks labelled content reliably (10 of 10 test attempts blocked). However, 31% of legacy files in PLM are unlabelled, so DLP cannot see them. Effectiveness depends on CC-04 labelling coverage.

### CC-04
**Mark all CUI — digital files, drawings and printed copies — with CUI banner markings and designation indicators per the DoD CUI Marking Guide**

| Field | Value |
|---|---|
| Primary framework | ISO 27001 — A.5.13 |
| CMMC L2 / NIST 800-171 | MP.L2-3.8.4 |
| Effectiveness | 🔴 Ineffective |
| Frequency | Continuous |
| Owner | Quality Director |
| Linked assets | [A-01](Asset-Inventory.md#a-01), [A-03](Asset-Inventory.md#a-03), [A-04](Asset-Inventory.md#a-04) |
| Linked data flows | [DPA-02](CUI-Data-Flows.md#dpa-02), [DPA-03](CUI-Data-Flows.md#dpa-03), [DPA-05](CUI-Data-Flows.md#dpa-05) |
| Evidence | [EV-03](Evidence-Register.md#ev-03) |

**Description.** Templates in PLM and ERP apply CUI banners automatically. Shop-floor printouts carry CUI cover sheets. Derivative files inherit the source marking.

**Decision rationale.** Ineffective: audit of 40 shop-floor drawings found 17 without banner or cover sheet, and derivative CAM files are not marked. Marking is central to the CUI handling task and to effective DLP (CC-03). Remediation is the top priority.

### CC-05
**Block removable media on CNC controllers and engineering workstations, except one controlled, logged media transfer station per plant**

| Field | Value |
|---|---|
| Primary framework | ISO 27001 — A.7.10 |
| CMMC L2 / NIST 800-171 | MP.L2-3.8.7 |
| Effectiveness | 🟢 Effective |
| Frequency | Continuous |
| Owner | Plant Operations Manager (Ohio) |
| Linked assets | [A-01](Asset-Inventory.md#a-01), [A-04](Asset-Inventory.md#a-04) |
| Linked data flows | [DPA-03](CUI-Data-Flows.md#dpa-03) |
| Evidence | — |

**Description.** Endpoint policy and physical port blockers disable USB storage. Program transfers use the networked DNC server. The media station scans and logs every transfer.

**Decision rationale.** Effective: spot check of 15 CNC controllers and 20 workstations showed USB storage blocked. Media station log reconciles with transfer requests for the last 3 months.

### CC-06
**Collect audit logs from all CUI and Security Protection Assets into the SIEM, retain them for 1 year, and review alerts weekly**

| Field | Value |
|---|---|
| Primary framework | CIS Controls — 8.2 |
| CMMC L2 / NIST 800-171 | AU.L2-3.3.1 |
| Effectiveness | 🟡 Partially Effective |
| Frequency | Continuous |
| Owner | IT Security Lead |
| Linked assets | [A-01](Asset-Inventory.md#a-01), [A-02](Asset-Inventory.md#a-02), [A-03](Asset-Inventory.md#a-03), [A-05](Asset-Inventory.md#a-05), [A-06](Asset-Inventory.md#a-06) |
| Linked data flows | [DPA-06](CUI-Data-Flows.md#dpa-06) |
| Evidence | — |

**Description.** Logs are forwarded from GCC High, PLM, ERP, the file gateway and firewalls. Use-case rules cover failed logons, privilege changes and mass downloads. Weekly review is recorded in a ticket.

**Decision rationale.** Partially effective: 4 of 5 in-scope log sources are onboarded. CNC/OT network logs (A-04 segment) are not collected. Weekly reviews were evidenced for 11 of the last 12 weeks.

### CC-07
**Maintain baseline configurations and a complete inventory of all in-scope hardware and software, reviewed quarterly**

| Field | Value |
|---|---|
| Primary framework | CIS Controls — 4.1 |
| CMMC L2 / NIST 800-171 | CM.L2-3.4.1 |
| Effectiveness | 🟡 Partially Effective |
| Frequency | Quarterly |
| Owner | IT Manager |
| Linked assets | [A-01](Asset-Inventory.md#a-01), [A-02](Asset-Inventory.md#a-02), [A-03](Asset-Inventory.md#a-03), [A-04](Asset-Inventory.md#a-04), [A-05](Asset-Inventory.md#a-05), [A-06](Asset-Inventory.md#a-06) |
| Linked data flows | [DPA-02](CUI-Data-Flows.md#dpa-02), [DPA-03](CUI-Data-Flows.md#dpa-03) |
| Evidence | — |

**Description.** CIS-based baselines for Windows servers and workstations are deployed via Intune and GPO. The asset inventory in the CMDB is reconciled quarterly against network discovery scans.

**Decision rationale.** Partially effective: baselines exist for IT assets, but there is no documented baseline for CNC controllers. The last reconciliation found 6 unrecorded devices on the plant network.

### CC-08
**Segment the OT/CNC network from corporate IT and the internet, allowing only the DNC server and MES on defined ports, with deny-by-default firewall rules**

| Field | Value |
|---|---|
| Primary framework | CIS Controls — 12.2 |
| CMMC L2 / NIST 800-171 | SC.L2-3.13.1 |
| Effectiveness | 🟢 Effective |
| Frequency | Continuous |
| Owner | Network Engineer |
| Linked assets | [A-03](Asset-Inventory.md#a-03), [A-04](Asset-Inventory.md#a-04) |
| Linked data flows | [DPA-03](CUI-Data-Flows.md#dpa-03) |
| Evidence | [EV-04](Evidence-Register.md#ev-04) |

**Description.** The OT VLAN is behind an internal firewall. Only MES to DNC to CNC flows are allowed. No direct internet or email access. Rule set reviewed quarterly.

**Decision rationale.** Effective: firewall rule review found no any-any rules. A penetration test from the corporate VLAN could not reach CNC controllers. This control compensates for the unpatchable legacy controllers documented as Specialized Assets.

### CC-09
**Encrypt CUI at rest and in transit using FIPS 140-validated cryptographic modules on all CUI assets**

| Field | Value |
|---|---|
| Primary framework | NIST CSF — PR.DS-01 |
| CMMC L2 / NIST 800-171 | SC.L2-3.13.11 |
| Effectiveness | 🔴 Ineffective |
| Frequency | Continuous |
| Owner | IT Security Lead |
| Linked assets | [A-01](Asset-Inventory.md#a-01), [A-03](Asset-Inventory.md#a-03), [A-05](Asset-Inventory.md#a-05) |
| Linked data flows | [DPA-02](CUI-Data-Flows.md#dpa-02), [DPA-04](CUI-Data-Flows.md#dpa-04), [DPA-05](CUI-Data-Flows.md#dpa-05) |
| Evidence | — |

**Description.** GCC High and the file gateway use FIPS-validated modules. Workstations use BitLocker in FIPS mode. Servers should use validated disk encryption and TLS configurations.

**Decision rationale.** Ineffective: the on-premises PLM server and ERP database use encryption that is not FIPS-validated, and FIPS mode is not enabled on engineering workstations. Encryption exists but not with validated modules, which is a common assessment failure.

### CC-10
**Operate an incident response capability that reports cyber incidents affecting CUI to DoD via DIBNet within 72 hours and preserves images for 90 days**

| Field | Value |
|---|---|
| Primary framework | NIST CSF — RS.MA-01 |
| CMMC L2 / NIST 800-171 | IR.L2-3.6.1 |
| Effectiveness | ⚪ Not Tested |
| Frequency | Annual |
| Owner | IT Security Lead |
| Linked assets | [A-02](Asset-Inventory.md#a-02), [A-06](Asset-Inventory.md#a-06) |
| Linked data flows | [DPA-06](CUI-Data-Flows.md#dpa-06) |
| Evidence | — |

**Description.** An IR plan defines roles, escalation and DFARS 252.204-7012 reporting. A DoD-approved medium-assurance certificate is held for DIBNet. A forensic retention procedure is in place.

**Decision rationale.** Not tested: plan approved, but no tabletop or live exercise has been run. 3.6.3 requires testing the IR capability. A tabletop with the prime contractor's security team is scheduled for next quarter.

### CC-11
**Run authenticated vulnerability scans monthly on all in-scope IT assets and remediate critical findings within 15 days**

| Field | Value |
|---|---|
| Primary framework | CIS Controls — 7.5 |
| CMMC L2 / NIST 800-171 | RA.L2-3.11.2 |
| Effectiveness | 🟢 Effective |
| Frequency | Monthly |
| Owner | IT Security Lead |
| Linked assets | [A-01](Asset-Inventory.md#a-01), [A-02](Asset-Inventory.md#a-02), [A-03](Asset-Inventory.md#a-03), [A-05](Asset-Inventory.md#a-05), [A-06](Asset-Inventory.md#a-06) |
| Linked data flows | [DPA-02](CUI-Data-Flows.md#dpa-02), [DPA-05](CUI-Data-Flows.md#dpa-05) |
| Evidence | [EV-05](Evidence-Register.md#ev-05) |

**Description.** Credentialed scans cover servers, workstations and network devices. Findings are ticketed with SLAs: critical 15 days, high 30 days. OT assets are scanned passively only.

**Decision rationale.** Effective: 12 consecutive monthly scans completed. Critical-finding SLA met for 96% of findings, with exceptions on the POA&M. Scan coverage matches the CMDB.

### CC-12
**Revoke all CUI system access within 24 hours of termination or transfer, triggered by HR and confirmed by IT**

| Field | Value |
|---|---|
| Primary framework | CIS Controls — 6.2 |
| CMMC L2 / NIST 800-171 | PS.L2-3.9.2 |
| Effectiveness | 🟡 Partially Effective |
| Frequency | Continuous |
| Owner | HR Director |
| Linked assets | [A-01](Asset-Inventory.md#a-01), [A-02](Asset-Inventory.md#a-02), [A-03](Asset-Inventory.md#a-03) |
| Linked data flows | [DPA-02](CUI-Data-Flows.md#dpa-02) |
| Evidence | — |

**Description.** HR offboarding ticket triggers account disablement in Entra ID and ERP. Badges and hardware are collected on the last day.

**Decision rationale.** Partially effective: cloud accounts were disabled within 24 hours for 18 of 20 sampled leavers. ERP accounts averaged 4 days because ERP is not connected to the identity provider. Transfers between programmes are not consistently triggering access removal.

### CC-13
**Flow down DFARS 252.204-7012 and CMMC Level 2 requirements to every sub-tier supplier handling CUI, and verify their SPRS score and certification status before releasing CUI**

| Field | Value |
|---|---|
| Primary framework | ISO 27001 — A.5.20 |
| CMMC L2 / NIST 800-171 | DFARS 252.204-7012(m) / AC.L2-3.1.20 |
| Effectiveness | 🟡 Partially Effective |
| Frequency | Quarterly |
| Owner | Supply Chain Security Manager |
| Linked assets | [A-05](Asset-Inventory.md#a-05) |
| Linked data flows | [DPA-04](CUI-Data-Flows.md#dpa-04) |
| Evidence | — |

**Description.** Purchase-order terms include 7012 and CMMC clauses. Supplier onboarding checks the SPRS score and CMMC status. CUI is released only through the secure gateway, and only to approved suppliers.

**Decision rationale.** Partially effective: flow-down clauses are in 100% of active POs, but SPRS or CMMC status is verified for only 9 of 14 CUI-handling suppliers. Two suppliers are still receiving drawings by email pending gateway onboarding.

### CC-14
**Maintain a System Security Plan describing the CUI boundary, all 110 NIST SP 800-171 requirements and their implementation, reviewed annually and on significant change**

| Field | Value |
|---|---|
| Primary framework | NIST CSF — GV.PO-01 |
| CMMC L2 / NIST 800-171 | CA.L2-3.12.4 |
| Effectiveness | 🟡 Partially Effective |
| Frequency | Annual |
| Owner | Compliance Manager |
| Linked assets | [A-01](Asset-Inventory.md#a-01), [A-02](Asset-Inventory.md#a-02), [A-03](Asset-Inventory.md#a-03), [A-04](Asset-Inventory.md#a-04), [A-05](Asset-Inventory.md#a-05), [A-06](Asset-Inventory.md#a-06) |
| Linked data flows | [DPA-01](CUI-Data-Flows.md#dpa-01), [DPA-02](CUI-Data-Flows.md#dpa-02), [DPA-03](CUI-Data-Flows.md#dpa-03), [DPA-04](CUI-Data-Flows.md#dpa-04), [DPA-05](CUI-Data-Flows.md#dpa-05), [DPA-06](CUI-Data-Flows.md#dpa-06) |
| Evidence | [EV-06](Evidence-Register.md#ev-06) |

**Description.** The SSP documents the system boundary, network diagrams, asset categories, data flows and an implementation statement per requirement, with a linked POA&M for open items. It is the primary document reviewed by the C3PAO.

**Decision rationale.** Partially effective: SSP v0.8 covers the boundary and 94 of 110 requirements. Implementation statements for the 16 remaining requirements, OT Specialized Asset treatment and the shared-responsibility matrix for GCC High are outstanding.

> References: ISO/IEC 27001:2022 Annex A · NIST CSF 2.0 · CIS Controls v8 · CMMC Level 2 practices (NIST SP 800-171 Rev 2).

---

← Previous: [CUI Data Flows](CUI-Data-Flows.md) · [↑ Overview](README.md) · **Next: [Supply Chain](Supply-Chain-Vendor-Assessment.md) →**
