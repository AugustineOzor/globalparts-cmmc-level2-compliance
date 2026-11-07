# Evidence Register
**GlobalParts Manufacturing** · Document ID: GP-CMMC-EVD-001 · Version 1.0 · Classification: Internal (portfolio sample — contains no real CUI)

## Purpose
Assessment evidence supporting the control effectiveness ratings. CMMC assessors use the examine, interview and test methods from NIST SP 800-171A. This register holds the *examine* artefacts and covers failing controls as well as effective ones.

## Evidence Summary

| ID | Title | Type | Control | CMMC Practice | Collected | Supports |
|---|---|---|---|---|---|---|
| [EV-01](#ev-01) | Q3 programme access review — CUI enclave security group membership export | Export | [CC-01](CMMC-Controls.md#cc-01) | AC.L2-3.1.1 | 2026-10-06 | 🟢 Effective |
| [EV-02](#ev-02) | Conditional Access policy configuration — MFA for CUI enclave and privileged roles | Configuration | [CC-02](CMMC-Controls.md#cc-02) | IA.L2-3.5.3 | 2026-10-08 | 🟡 Partially Effective |
| [EV-03](#ev-03) | CUI marking spot audit — shop-floor drawings and CAM files (Michigan & Ohio) | Report | [CC-04](CMMC-Controls.md#cc-04) | MP.L2-3.8.4 | 2026-09-24 | 🔴 Ineffective |
| [EV-04](#ev-04) | OT/CNC network segmentation — firewall rule set and penetration test result | Configuration | [CC-08](CMMC-Controls.md#cc-08) | SC.L2-3.13.1 | 2026-09-30 | 🟢 Effective |
| [EV-05](#ev-05) | Monthly authenticated vulnerability scan reports and remediation SLA tracker | Report | [CC-11](CMMC-Controls.md#cc-11) | RA.L2-3.11.2 | 2026-10-03 | 🟢 Effective |
| [EV-06](#ev-06) | System Security Plan v0.8 with POA&M | Document | [CC-14](CMMC-Controls.md#cc-14) | CA.L2-3.12.4 | 2026-10-10 | 🟡 Partially Effective |

**Coverage:** 6 of 14 controls have evidence on file. Controls without evidence yet: [CC-03](CMMC-Controls.md#cc-03), [CC-05](CMMC-Controls.md#cc-05), [CC-06](CMMC-Controls.md#cc-06), [CC-07](CMMC-Controls.md#cc-07), [CC-09](CMMC-Controls.md#cc-09), [CC-10](CMMC-Controls.md#cc-10), [CC-12](CMMC-Controls.md#cc-12), [CC-13](CMMC-Controls.md#cc-13).

## Evidence Details

### EV-01
**Q3 programme access review — CUI enclave security group membership export**

| Field | Value |
|---|---|
| Type | Export |
| Related control | [CC-01](CMMC-Controls.md#cc-01) (platform ID `CTL-mw6833l9`) |
| CMMC L2 practice | AC.L2-3.1.1 |
| Owner | IT Manager |
| Location | `https://globalparts.sharepoint.us/sites/CMMC-Evidence/AC/EV-01_Q3-Access-Review.xlsx` |
| Collected | 2026-10-06 |
| Evidence period | Jul – Sep 2026 |
| Supports rating | 🟢 Effective |

Entra ID export of all 9 programme security groups (212 members) reconciled to the HR roster and signed off by each Programme Manager. Sample of 25 grants traced to approved tickets with zero exceptions. Demonstrates authorised users are identified and access is limited to them.

### EV-02
**Conditional Access policy configuration — MFA for CUI enclave and privileged roles**

| Field | Value |
|---|---|
| Type | Configuration |
| Related control | [CC-02](CMMC-Controls.md#cc-02) (platform ID `CTL-mw68477q`) |
| CMMC L2 practice | IA.L2-3.5.3 |
| Owner | IT Manager |
| Location | `https://globalparts.sharepoint.us/sites/CMMC-Evidence/IA/EV-02_ConditionalAccess-Policies.json` |
| Collected | 2026-10-08 |
| Evidence period | Point in time |
| Supports rating | 🟡 Partially Effective |

JSON export of policies CA-01 to CA-04 showing MFA required for all users on GCC High and the file gateway, FIDO2 required for admin roles, and legacy authentication blocked. Includes a sign-in log sample. The gap is visible here: ERP/MES local admin logons are outside these policies.

### EV-03
**CUI marking spot audit — shop-floor drawings and CAM files (Michigan & Ohio)**

| Field | Value |
|---|---|
| Type | Report |
| Related control | [CC-04](CMMC-Controls.md#cc-04) (platform ID `CTL-mw686b8h`) |
| CMMC L2 practice | MP.L2-3.8.4 |
| Owner | Quality Director |
| Location | `https://globalparts.sharepoint.us/sites/CMMC-Evidence/MP/EV-03_CUI-Marking-Audit.pdf` |
| Collected | 2026-09-24 |
| Evidence period | Point in time |
| Supports rating | 🔴 Ineffective |

Audit of 40 printed drawings at CNC cells and 25 derivative CAM files. 17 printed drawings lacked banner or cover sheet, and 0 of 25 CAM files carried markings. Includes photos and a corrective action request. Evidence of the control gap that supports the Ineffective rating.

### EV-04
**OT/CNC network segmentation — firewall rule set and penetration test result**

| Field | Value |
|---|---|
| Type | Configuration |
| Related control | [CC-08](CMMC-Controls.md#cc-08) (platform ID `CTL-mw68aj8o`) |
| CMMC L2 practice | SC.L2-3.13.1 |
| Owner | Network Engineer |
| Location | `https://globalparts.sharepoint.us/sites/CMMC-Evidence/SC/EV-04_OT-Firewall-Rules_and_PenTest.zip` |
| Collected | 2026-09-30 |
| Evidence period | Rules: point in time · Pen test: Sep 2026 |
| Supports rating | 🟢 Effective |

Firewall rule export for the OT boundary (deny-by-default, 6 allow rules for MES/DNC), network diagram, and an independent penetration test excerpt confirming CNC controllers are unreachable from the corporate VLAN. Supports Specialized Asset treatment in the SSP.

### EV-05
**Monthly authenticated vulnerability scan reports and remediation SLA tracker**

| Field | Value |
|---|---|
| Type | Report |
| Related control | [CC-11](CMMC-Controls.md#cc-11) (platform ID `CTL-mw68eo8e`) |
| CMMC L2 practice | RA.L2-3.11.2 |
| Owner | IT Security Lead |
| Location | `https://globalparts.sharepoint.us/sites/CMMC-Evidence/RA/EV-05_Vuln-Scans_Oct25-Sep26/` |
| Collected | 2026-10-03 |
| Evidence period | Oct 2025 – Sep 2026 |
| Supports rating | 🟢 Effective |

Twelve monthly credentialed scan reports with scan-coverage reconciliation to the CMDB and an SLA tracker showing 96% of critical findings remediated within 15 days. Exceptions are recorded on the POA&M.

### EV-06
**System Security Plan v0.8 with POA&M**

| Field | Value |
|---|---|
| Type | Document |
| Related control | [CC-14](CMMC-Controls.md#cc-14) (platform ID `CTL-mw68j20t`) |
| CMMC L2 practice | CA.L2-3.12.4 |
| Owner | Compliance Manager |
| Location | `https://globalparts.sharepoint.us/sites/CMMC-Evidence/CA/EV-06_SSP-v0.8_and_POAM.docx` |
| Collected | 2026-10-10 |
| Evidence period | Version dated 2026-10-10 |
| Supports rating | 🟡 Partially Effective |

Current SSP describing the CUI boundary, network diagrams, asset categories, data flows and implementation statements for 94 of 110 requirements, with a linked POA&M. Primary document for the C3PAO pre-assessment. Not final: 16 requirements and the GCC High shared-responsibility matrix are outstanding.

> Locations are illustrative paths in a GCC High SharePoint evidence library. CUI evidence must remain inside the enclave.

---

← Previous: [Supply Chain](Supply-Chain-Vendor-Assessment.md) · [↑ Overview](README.md) · **Next: [SSP & C3PAO Readiness](SSP-and-C3PAO-Readiness.md) →**
