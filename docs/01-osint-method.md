# 1. OSINT method and ethics

## Rules first
1. **Passive only.** Read what is already public. Never touch the organization's systems. That means no port or vulnerability scanning, no Shodan/Censys lookups of their IP addresses, no subdomain brute forcing, and no login attempts.
2. **No breach dumps or credential searches.** Breach *databases run by regulators* (like the HHS OCR portal) are fine. Leaked data is never fine.
3. **Organization level only.** Public pages often list executives, board members, staff and even patients. None of them get named or profiled.
4. **Cite everything.** Each fact gets a link and an access date. Anything I worked out myself is labeled **Inference**.
5. **Check the name.** Many health systems share similar names. Confirm every finding by location and context before you use it.
6. **Be careful with absence.** "No public breach found" does not mean "never breached." OCR only lists breaches affecting 500 or more people.

## Source categories

| Source type | Examples | What it's good for | Watch out for |
|---|---|---|---|
| Public records | Job postings, facility pages, CMS hospital info | Tech stack signals (EHR, ITSM, HR systems), facility types | Postings show intent, not proof of maturity |
| Breach databases | [HHS OCR breach portal](https://ocrportal.hhs.gov/ocr/breach/breach_report.jsf) (current and archive, CSV export); state AG notice pages | Reported HIPAA breaches, including ones caused by business associates | "500" is often a placeholder. Some states have no public list. |
| Threat intel feeds | [CISA KEV](https://www.cisa.gov/known-exploited-vulnerabilities-catalog), [FIRST EPSS](https://www.first.org/epss/), [CISA #StopRansomware](https://www.cisa.gov/stopransomware), [Health-ISAC](https://health-isac.org/) public reports, HHS HC3 alerts | What attackers are actually using | HC3's 2026 status is unclear, so cross-check with CISA |
| Org social media and press | Newsroom, press releases, patient scam warnings | Major IT projects, vendor changes, patient-facing threats | Marketing tone |
| Corporate / nonprofit filings | IRS Form 990 via [ProPublica Nonprofit Explorer](https://projects.propublica.org/nonprofits/) | Size, revenue, affiliates | Filings lag 1–2 years |
| News | Local and trade press | Incidents, financial pressure, vendor transitions | Paywalls. Verify against primary sources. |

## Source log (sector sources used in this case study, accessed Oct 22, 2026)

| Source type | What was checked | What was found | Confidence |
|---|---|---|---|
| Breach database | [HHS OCR breach portal](https://ocrportal.hhs.gov/ocr/breach/breach_report.jsf) archive (CSV) | Change Healthcare listed as a business associate breach, 192,700,000 individuals | High |
| Regulator FAQ | [HHS Change Healthcare FAQ](https://www.hhs.gov/hipaa/for-professionals/special-topics/change-healthcare-cybersecurity-incident-frequently-asked-questions/index.html) | 192.7M individuals impacted (updated Jul 31, 2025) | High |
| Industry survey | [AHA survey, Mar 2024](https://www.aha.org/news/news/2024-03-15-aha-survey-change-healthcare-cyberattack-having-significant-disruptions-patient-care-hospitals-finances) | 94% of hospitals reported financial impact and 74% reported patient care impact | High |
| Threat intel | [CISA KEV JSON feed](https://www.cisa.gov/known-exploited-vulnerabilities-catalog) | Catalog v2026.10.21: 1,754 entries, 361 flagged as used in ransomware | High |
| Threat intel | [CISA AA25-203A Interlock](https://www.cisa.gov/news-events/cybersecurity-advisories/aa25-203a) | Co-authored by HHS. Fake updates, ClickFix, credential theft, VM encryption, double extortion | High |
| Sector guidance | [405(d) HICP 2023](https://405d.hhs.gov/cornerstone/hicp) | 10 practices, including Vulnerability Management and Network Connected Medical Devices | High |
| Sector guidance | [HPH Cybersecurity Performance Goals](https://hhscyber.hhs.gov/cybersecurity-performance-goals.html) | Essential and Enhanced goals (for example, mitigate known vulnerabilities, MFA, vendor requirements) | High |
| Framework | [NIST CSF 2.0](https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.29.pdf) | Subcategory IDs used in this repo checked against the PDF | High |
| Framework | [NIST SP 800-37 Rev. 2](https://csrc.nist.gov/pubs/sp/800/37/r2/final) | RMF steps: Prepare, Categorize, Select, Implement, Assess, Authorize, Monitor | High |
| Regulation | [Reginfo RIN 0945-AA22](https://www.reginfo.gov/public/do/eAgendaViewRule?RIN=0945-AA22&pubId=202510) | HIPAA Security Rule NPRM (Jan 6, 2025) is not final. Long-Term Actions, target Jul 2027. | High |
| Law | [Public Law 116-321](https://www.govinfo.gov/content/pkg/PLAW-116publ321/pdf/PLAW-116publ321.pdf) | OCR must consider recognized security practices in place for the prior 12 months | High |
| Enforcement | [Nixon Peabody, Jul 2026](https://www.nixonpeabody.com/insights/articles/2026/07/21/health-plan-settlement-marks-ocrs-20th-ransomware-and-14th-risk-analysis-initiative) | OCR's 14th Risk Analysis Initiative action and 20th ransomware action | High |
| News | [Healthcare Dive, Aug 2026](https://www.healthcaredive.com/news/health-systems-warn-patients-of-mychart-phishing-scam/828597/) | A dozen-plus health systems warned patients about portal-branded phishing | High |

## Lesson learned while doing real OSINT
When I searched for one regional health system's name, I found **several unrelated organizations** with nearly the same name, and each had its own breach news. A careless analyst would pin someone else's ransomware incident on the wrong employer. **Always confirm by city, state and facility names.**
