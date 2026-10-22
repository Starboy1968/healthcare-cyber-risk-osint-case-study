# 3. Program scope, stakeholders and RACI

## Program scope

| Item | Detail |
|---|---|
| **Objective** | Stand up a risk-based cyber risk program (vulnerability management, HIPAA evidence, system reviews) that leaders can understand and IT can sustain. |
| **In scope** | Enterprise IT, the EHR and its interfaces, cloud/SaaS, business associates, networked medical devices (through Biomed), policies, audit evidence, metrics. |
| **Out of scope** | Running security tools day to day (the SOC/engineering teams do that), physical security operations, and clinical device engineering itself. |
| **Assumptions** | A scanner and ticketing system already exist. Leadership supports a tiered SLA. Biomed owns devices. |
| **Constraints** | Tight budget, change windows set around patient care, small rural sites with thin IT staff, and vendor approval needed for device patches. |

## Stakeholder map (roles only)

| Stakeholder | Cares about | Needs from this program |
|---|---|---|
| CISO / Manager of Information Security | A defensible program and fewer incidents | Clear risk picture and a reliable backup |
| CIO | Uptime, EHR stability, budget | Risk in terms of downtime and dollars |
| IT Infrastructure | Stability, change windows, workload | Short, ranked fix lists with fair deadlines |
| EHR team | Upgrades, clinician experience | Findings that fit the EHR release cycle |
| Clinical Engineering / Biomed | Device uptime and vendor rules | Compensating controls, not "just patch it" |
| Compliance / Privacy Officer | HIPAA and OCR | Evidence library, risk analysis, BAAs |
| Internal Audit | Independent assurance | Testable controls and an evidence trail |
| Legal | Liability, contracts, notification | Security terms in vendor contracts and decision logs |
| Procurement / Vendor Management | Cost and speed | A light, tiered vendor review |
| Clinical leadership | Patient safety | Downtime procedures that work |
| Board / Risk Committee | Mission and reputation | A few clear metrics and the top risks |

## RACI (R = does it, A = owns it, C = consulted, I = informed)

| Activity | Cyber Risk PM | CISO | CIO | IT Infra | EHR team | Biomed | Compliance | Internal Audit | Legal | Procurement | Clinical | Board |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| HIPAA risk analysis | R | A | C | C | C | C | C | I | I | I | C | I |
| Vulnerability program | R/A (program) | A (overall) | I | R (fix) | R (fix) | R (devices) | I | I | – | – | I | I |
| Risk exceptions | R (prepare) | A | C (high) | C | C | C | C | I | C | – | C | I (critical) |
| System review / authorization | R | A | C | C | C | C | C | I | – | C | C | – |
| Vendor security review | R | A | I | C | C | C | C | I | C | R (intake) | I | – |
| Audit evidence library | R | A | I | C | C | C | C | C | I | – | – | I |
| Policy updates | R (draft) | A | C | C | C | C | C | I | C | I | C | I |
| Metrics reporting | R | A | I | C | C | C | I | I | – | – | I | I |
