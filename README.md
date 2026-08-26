# SNF Skills for Claude Code

**Open-source AI skill packs for skilled nursing facilities.** Built and maintained by
[Exponential Care](https://exponentialcare.ai) as a public good for the post-acute
community — free for any facility, operator, or consultant to use.

Each pack teaches Claude the working knowledge of a specific SNF discipline —
referral triage, PDPM reimbursement, NTA capture, managed-care contracts,
compliance, census operations, prior authorization, and eligibility — so your team
can hand Claude a hospital packet, a payer contract, or a census export and get
back structured, defensible work product in minutes.

## Quick start

In [Claude Code](https://claude.com/claude-code) (CLI, desktop, or web):

```
/plugin marketplace add Exponential-Care/snf-skills
/plugin install referral-triage@snf-skills
```

Install as many packs as you want — each is independent. Once installed, just talk
to Claude naturally ("here's a referral packet from Example Hospital — should we
take it?") and the right skill activates on its own.

## The packs

| Pack | What it does |
|---|---|
| **referral-triage** | Screen a hospital referral packet end-to-end: clinical fit, financial fit, red flags, missing documentation, and a structured accept/decline decision memo. |
| **pdpm-revenue** | Estimate the Medicare PDPM per-diem from referral documentation — all six components, variable per-diem adjustments, and a stay-revenue worksheet. |
| **nta-capture** | Find every legitimately documented NTA comorbidity in the hospital record, with quoted evidence, MDS item sources, and a missed-points audit mode. |
| **insurance-contracts** | Extract the terms that matter from a managed-care contract (rates, levels, carve-outs, auth rules, timely filing), level patients against it, and prep negotiations. |
| **compliance** | Build MDS/PPS assessment calendars, track PBJ deadlines, run survey-readiness checks, and draft Plans of Correction. |
| **census-operations** | Turn a census export into occupancy, payer-mix, and skilled-mix analysis with trends, red flags, and backfill math. |
| **prior-auth** | Assemble initial-auth and continued-stay packets, prep peer-to-peer reviews, and draft appeal letters from your clinical facts. |
| **eligibility** | Reason through Medicare SNF coverage: qualifying stays, benefit-day math, coinsurance windows, MA plan nuances, and Medicaid-pending risk. |

## Working with PHI

These skills are prompts and reference material — they send nothing anywhere by
themselves. But the documents you analyze with them (referral packets, census
exports) usually contain protected health information. Use them the same way your
organization already governs AI usage: under your Claude commercial terms/BAA,
with the minimum necessary data, and never in a consumer account that isn't
covered by your compliance program. When in doubt, de-identify first.

## Disclaimer

Everything here is educational reference material drawn from publicly available
CMS methodology and general industry practice. It is **not** clinical, billing,
coding, or legal advice. Payment rules, rates, and deadlines change every year —
always verify against the current CMS SNF PPS final rule, the current RAI manual,
your state's regulations, and your actual payer contracts. Coding and claims must
always reflect what is genuinely documented in the medical record.

## Contributing

Issues and pull requests are welcome — from operators, MDS coordinators, billers,
and builders alike. See [CONTRIBUTING.md](CONTRIBUTING.md). If a skill gave you a
wrong or outdated answer, an issue with the specifics is a gift.

## About

Maintained by [Exponential Care](https://exponentialcare.ai), the team behind
Referral Triage Pro — AI-native referral triage and revenue intelligence for
skilled nursing facilities. We build in this industry every day; these skills
share the parts of that knowledge that belong to everyone.

Licensed under the [MIT License](LICENSE).
