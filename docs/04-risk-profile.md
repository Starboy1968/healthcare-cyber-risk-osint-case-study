# 4. Risk profile (CRHS, fictional composite)

Ratings are in words. **Likelihood** means how likely over the next 1–2 years. **Impact** means how bad for patients, money and compliance. All rankings are **inference** from sector sources. Owners are roles.

## Sector evidence behind the rankings

| # | Sector signal | Source | Confidence |
|---|---|---|---|
| S1 | One clearinghouse attack (Change Healthcare, Feb 2024) affected 192.7M people. 94% of hospitals reported financial impact. | [HHS FAQ](https://www.hhs.gov/hipaa/for-professionals/special-topics/change-healthcare-cybersecurity-incident-frequently-asked-questions/index.html), [AHA](https://www.aha.org/news/news/2024-03-15-aha-survey-change-healthcare-cyberattack-having-significant-disruptions-patient-care-hospitals-finances) | High |
| S2 | Ransomware groups using fake updates, ClickFix, stolen credentials and VM encryption, in a joint advisory with HHS | [CISA AA25-203A](https://www.cisa.gov/news-events/cybersecurity-advisories/aa25-203a) | High |
| S3 | 361 vulnerabilities on CISA KEV are flagged as used in ransomware campaigns (Oct 2026) | [CISA KEV](https://www.cisa.gov/known-exploited-vulnerabilities-catalog) | High |
| S4 | Patient-portal-branded phishing warnings from a dozen-plus health systems (2026) | [Healthcare Dive](https://www.healthcaredive.com/news/health-systems-warn-patients-of-mychart-phishing-scam/828597/) | High |
| S5 | OCR enforcement focused on risk analysis (14 actions by mid-2026) | [Nixon Peabody](https://www.nixonpeabody.com/insights/articles/2026/07/21/health-plan-settlement-marks-ocrs-20th-ransomware-and-14th-risk-analysis-initiative) | High |
| S6 | Many OCR-listed breaches are reported through business associates (vendors) | [OCR breach portal](https://ocrportal.hhs.gov/ocr/breach/breach_report.jsf) | High |

## Ranked risks

| Rank | Risk | Likelihood | Impact | Rationale | Owner |
|---|---|---|---|---|---|
| 1 | Ransomware causing EHR / clinical downtime | Medium-High | Very High | S2, S3. Downtime means diversions and paper charting. Small rural hospitals have thin staff. | CISO + IT Infrastructure |
| 2 | Third-party / clearinghouse / business associate failure | High | High | S1, S6. One vendor can stop cash flow or expose PHI. | Vendor Mgmt + InfoSec. Revenue Cycle for the clearinghouse |
| 3 | Phishing and AI-enabled impersonation | High | Medium-High | S4. Mailboxes and help desks are common ways in. AI makes lures cheaper. | InfoSec + Compliance + Communications |
| 4 | EHR access misuse and identity gaps | Medium | High | Thousands of users. Stale or over-broad access. | EHR team + Privacy |
| 5 | Unpatched known-exploited vulnerabilities (internet-facing) | Medium-High | High | S3. Remote access and file-transfer tools are common targets. | Cyber Risk PM (program) + IT (fix) |
| 6 | Medical device / IoT that can't be patched normally | Medium | High | Old operating systems and vendor-controlled patching. | Biomed + InfoSec |
| 7 | Legacy systems and leftover data or interfaces | Medium | Medium | Replatforming and mergers leave orphaned accounts and copies. | IT Applications |
| 8 | Audit / regulatory finding | Medium | Medium | S5. The HIPAA Security Rule update is still pending. | Compliance + PM |

## Framework mapping
NIST CSF 2.0 IDs were checked against the [CSF 2.0 PDF](https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.29.pdf). HIPAA citations are [45 CFR 164 Subpart C](https://www.ecfr.gov/current/title-45/subtitle-A/subchapter-C/part-164/subpart-C).

| Risk | HIPAA Security Rule | NIST CSF 2.0 | NIST SP 800-37 step | 405(d) HICP practice |
|---|---|---|---|---|
| 1 Ransomware | 164.308(a)(7) contingency; 164.308(a)(6) incidents | PR.DS-11, RS.MA-01, RC.RP-01 | Implement, Monitor | SOC and Incident Response; Endpoint Protection |
| 2 Third party | 164.308(b), 164.314 BA contracts | GV.SC-07, GV.SC-10 | Prepare, Authorize | Cybersecurity Oversight and Governance |
| 3 Phishing | 164.308(a)(5) awareness | PR.AT-01 | Implement | Email Protection Systems |
| 4 EHR access | 164.312(a), 164.312(b), 164.308(a)(4) | PR.AA-05 | Select, Assess | Access Management; Data Protection and Loss Prevention |
| 5 Known exploited vulns | 164.308(a)(1)(ii)(A)–(B) | ID.RA-01, ID.RA-05, ID.RA-06, ID.RA-08, PR.PS-02 | Assess, Monitor | Vulnerability Management |
| 6 Medical devices | 164.308(a)(1); 164.310 | ID.AM-01, ID.AM-08, PR.IR-01 | Categorize, Select | Network Connected Medical Devices; Network Management; Asset Management |
| 7 Legacy | 164.308(a)(1); 164.310(d) | ID.AM-08, PR.PS-02 | Monitor, Authorize | Asset Management |
| 8 Audit finding | 164.308(a)(8); 164.316 | GV.OV-03, GV.PO-02, ID.IM-02 | Assess, Authorize | Cybersecurity Oversight and Governance |

## Regulatory status (checked Oct 22, 2026)
- **HIPAA Security Rule update:** the NPRM was published Jan 6, 2025 and is **not final**. HHS moved it to Long-Term Actions with a July 2027 target ([reginfo](https://www.reginfo.gov/public/do/eAgendaViewRule?RIN=0945-AA22&pubId=202510)). The current rule still applies. Use the proposal as a preview, not as law.
- **HITECH recognized security practices** ([P.L. 116-321](https://www.govinfo.gov/content/pkg/PLAW-116publ321/pdf/PLAW-116publ321.pdf)): OCR must consider NIST- or HICP-aligned practices in place for the prior 12 months. Good evidence can lower penalties.
