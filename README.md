# Healthcare Cyber Risk Program: An OSINT Case Study

**What this is:** a cyber risk program for a regional nonprofit health system, built only from passive, public, sector-level sources. The organization is a **fictional composite** called "Composite Regional Health System" (CRHS). It is not a real employer, and no real hospital's findings are included.

**Who it's for:** hiring managers for cyber risk, GRC, vulnerability management and HIPAA compliance roles in healthcare.

## The 60-second version

| Question | Answer |
|---|---|
| Top risk | Ransomware and vendor outages that take down the EHR or claims flow. The 2024 Change Healthcare attack showed one vendor can stall a whole sector. |
| Cheapest big win | One list of every vendor that touches patient data, tiered by impact, with a business associate agreement on file for each. |
| How vulns get ranked | **CISA KEV first** (attackers already use it), then internet exposure and patient-care impact, then the **EPSS** chance of exploitation. No formulas. |
| Fix targets | Emergency in 7 days, High in 15, Medium in 30–45, Low in 90. Medical devices follow vendor-approved paths plus segmentation. |
| Proof for auditors | A HIPAA Security Rule evidence library mapped to NIST CSF 2.0 and HHS 405(d) HICP. 12 months of proof can earn HITECH "recognized security practices" credit. |
| First 90 days | Listen and map, then stand up a weekly KEV review and an exceptions process, then prove it with a restore test and a metrics pack. |

## What's inside

| # | Document | What it shows |
|---|---|---|
| 1 | [OSINT method and ethics](docs/01-osint-method.md) | Passive-only rules, source categories, source log |
| 2 | [Composite organization profile](docs/02-composite-org-profile.md) | The fictional health system and why it's realistic |
| 3 | [Program scope, stakeholders, RACI](docs/03-program-scope-and-stakeholders.md) | How a program manager frames the work |
| 4 | [Risk profile](docs/04-risk-profile.md) | 8 ranked risks, likelihood/impact in words, HIPAA / NIST CSF 2.0 / RMF / HICP mapping |
| 5 | [Vulnerability management program](docs/05-vulnerability-management.md) | Lifecycle, KEV + EPSS prioritization, SLA tiers, exceptions |
| 6 | [RMF and HIPAA audit evidence](docs/06-rmf-hipaa-audit-evidence.md) | Evidence library, system review package, HITECH credit |
| 7 | [30/60/90 day plan and recommended actions](docs/07-30-60-90-plan.md) | Sequenced actions with owners, effort, dependencies, success measures |
| 8 | [Metrics](docs/08-metrics.md) | 7 plain-language measures for leadership |
| 9 | [How I'd apply this to a real employer](docs/09-applying-to-a-real-employer.md) | Turning a composite into a real-world plan, ethically |

## Skills demonstrated
- Cyber risk assessment (likelihood and impact, ranked with rationale and owners)
- Vulnerability management program design (CISA KEV, EPSS, SLAs, exceptions, metrics)
- HIPAA Security Rule, HITECH, NIST CSF 2.0, NIST SP 800-37 RMF, HHS 405(d) HICP, HPH Cybersecurity Performance Goals
- Third-party / business associate risk
- Ethical, passive OSINT with a source log and confidence levels
- Program management: scope, stakeholder map, RACI, sequenced roadmap
- Writing for non-technical leaders

## Ground rules this case study follows
- **Passive and public only.** No scanning, probing, login attempts, IP lookups, subdomain discovery, or breach-dump and credential searches.
- **Organization level only.** No individual people are named or profiled.
- **Fictional composite.** CRHS is invented, and the sector facts are cited.
- **No fabrication.** Facts link to sources (accessed Oct 22, 2026). Inferences are labeled.

## Related projects
- [AI Supply Chain Risk Assessment](https://github.com/Starboy1968/ai-supply-chain-risk-assessment): nine scored AI-related supply chain risks, with controls, warning indicators (KRIs) and a 30/60/90-day plan.
- [AI-Assisted Risk Analysis](https://github.com/Starboy1968/ai-assisted-risk-analysis): a reusable risk-analysis prompt and a worked example where an AI first draft is checked and corrected by a human reviewer.
- [Reading the Room: Power and Behavior Risk Indicators](https://github.com/Starboy1968/power-behavior-risk-indicators): observable signs of how power, incentives and group behavior shape risk decisions, and how to turn them into solid findings.
- [Behavioral Supply Chain Risk: Human Factors, AI, and Audit](https://github.com/Starboy1968/behavioral-supply-chain-risk-audit-ai): how bias and pressure create supply chain risk, and how AI triage, audit evidence and human review help catch it.
- [Playing the Risk Game: Game Theory for Supply Chain Risk and AI Governance](https://github.com/Starboy1968/supply-chain-ai-governance-strategy): plain-language game theory that explains why supply chain and AI risks persist, and which incentives to change.
- [AI in Supply Chain Operations: A Strategist's Field Guide](https://github.com/Starboy1968/ai-in-supply-chain-operations): how a supply chain manager can use AI in six everyday jobs, and what to check before trusting it.
- [AI for CISA and IT Auditors: Creative Workflow Accelerators](https://github.com/Starboy1968/ai-for-it-auditors): nine practical ways AI can speed up IT audit work, from walkthroughs and SOC 2 review to auditing AI, with a human check at every step.
- [grc-control-mapper](https://github.com/Starboy1968/grc-control-mapper): maps policy text to NIST 800-53 Rev 5 with gap analysis and a review queue
- [two-suppliers-one-factory](https://github.com/Starboy1968/two-suppliers-one-factory): finding hidden tier-2 single points of failure
- [emudhra-weak-key-incident-analysis](https://github.com/Starboy1968/emudhra-weak-key-incident-analysis): third-party post-mortem of a CA weak-key incident
- [supply-web-audit](https://github.com/Starboy1968/supply-web-audit): plain-English supply risk audit for small and mid-size businesses
- [va-incident-mapper](https://github.com/Starboy1968/va-incident-mapper): helps cyber-crime victims document what happened

---

**Author:** Rashon Alsberry, supply chain and third-party risk analyst · [starboy1968.github.io](https://starboy1968.github.io)
