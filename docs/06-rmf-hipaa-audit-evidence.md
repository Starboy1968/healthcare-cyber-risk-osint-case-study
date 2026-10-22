# 6. RMF and HIPAA audit evidence approach

## Evidence library (HIPAA Security Rule)
| Safeguard | Evidence | How often | Owner |
|---|---|---|---|
| Risk analysis, 164.308(a)(1)(ii)(A) | Enterprise risk analysis covering all ePHI systems | Yearly and after major change | Cyber Risk PM + Compliance |
| Risk management, 164.308(a)(1)(ii)(B) | Risk register, treatment decisions, signed exceptions | Monthly | Cyber Risk PM |
| Activity review, 164.308(a)(1)(ii)(D) | Log reviews, EHR access audit reports | Monthly | Privacy + InfoSec |
| Awareness, 164.308(a)(5) | Training completion, phishing results | Quarterly | InfoSec |
| Incidents, 164.308(a)(6) | IR plan, incident log, after-action reports | Per event, plus a yearly tabletop | CISO |
| Contingency, 164.308(a)(7) | Backup reports, **restore test results**, downtime drills | At least yearly per critical system | IT Infrastructure |
| Evaluation, 164.308(a)(8) | Assessment report and remediation tracker | Yearly | Internal Audit |
| BA contracts, 164.308(b), 164.314 | BAA inventory, vendor tiers, reviews | Yearly and at onboarding | Procurement + PM |
| Technical safeguards, 164.312 | Access reviews, MFA coverage, privileged account list | Quarterly | IT + EHR team |
| Documentation, 164.316 | Versioned policy library, **kept 6 years** | Ongoing | Compliance |

## RMF-style system review (light version for a hospital)
Based on [NIST SP 800-37 Rev. 2](https://csrc.nist.gov/pubs/sp/800/37/r2/final): Prepare → Categorize → Select → Implement → Assess → Authorize → Monitor.

**The one-packet review for a new system or vendor:**
1. What it is, what data it holds, and who owns it
2. How critical it is (patient care, PHI, internet-facing)
3. Which controls apply (a short list, mapped to NIST CSF 2.0 and HICP)
4. What was tested and what was found
5. Remaining risk in plain words
6. Sign-off by the system owner and the CISO (the "authorization to operate"), with a review date

## HITECH credit
Keep **12 months of proof** (reports, logs, tickets, not just policies) that HICP/NIST practices are actually in use. Under [P.L. 116-321](https://www.govinfo.gov/content/pkg/PLAW-116publ321/pdf/PLAW-116publ321.pdf), OCR must consider it.
