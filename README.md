# SNF Skills for Claude Code

**Open-source AI skill packs for skilled nursing facilities.**
Teach Claude the working knowledge of your admissions office, your MDS
coordinator, your managed-care team, and your compliance nurse — then hand it
the packet.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude_Code-plugin_marketplace-d97757.svg)](https://claude.com/claude-code)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-blue.svg)](CONTRIBUTING.md)
[![Maintained by Exponential Care](https://img.shields.io/badge/maintained_by-Exponential_Care-8A2BE2.svg)](https://exponentialcare.ai)

Built and maintained by [Exponential Care](https://exponentialcare.ai) as a
public good for the post-acute community. Free for any facility, operator, or
consultant. No product attached, no sign-up, no strings — just the domain
knowledge, open-sourced.

---

## Why this exists

Every SNF runs on the same hard-won knowledge: how to read a hospital packet,
what an NTA point is worth, which contract clauses quietly cost you money, when
the 5-day assessment window closes. That knowledge lives in a handful of
overworked people per building — and AI assistants don't have it out of the box.

These packs close that gap. Each one is a **skill**: a structured playbook that
loads into Claude the moment your question touches its domain, so the answer you
get is the one a seasoned admissions director, MDS coordinator, or managed-care
negotiator would give — with worksheets, evidence, and the caveats that matter.

## Quick start

In [Claude Code](https://claude.com/claude-code) (terminal, desktop, or web):

```
/plugin marketplace add Exponential-Care/snf-skills
/plugin install referral-triage@snf-skills
```

Install as many packs as you want — each is independent. Then just work
naturally:

> **You:** Here's a referral packet from Example Hospital (referral.pdf) — should we take this patient?
>
> **Claude:** *(referral-packet-review activates)* Reading the packet… Here's my screen:
> **Clinical fit** — IV antibiotics ×10 days and a wound vac: confirm your building
> supports negative-pressure wound therapy. **Financial fit** — Medicare Advantage
> (Sample Health Plan): authorization required before admit; expect a level or
> case rate, not PDPM. **Red flags** — no H&P in the packet, med list is 4 days
> old. **Recommendation:** conditionally accept pending auth; here's the
> missing-documents request to send back to the case manager…

## The packs

| Pack | What Claude learns | Try asking |
|---|---|---|
| **referral-triage** | Screen a hospital packet end-to-end: clinical fit, financial fit, red flags, missing docs, and a structured accept/decline decision memo | *"Here's a packet from Example Hospital — should we take it?"* |
| **pdpm-revenue** | The full PDPM model: all six components, GG function scores, CMG classification, variable per-diem math, stay-revenue worksheets | *"What would Medicare pay for this admission?"* |
| **nta-capture** | The complete CMS NTA comorbidity list and where each condition hides in hospital records — with quoted evidence, MDS item sources, and a missed-points audit mode | *"Find every NTA point in this discharge summary"* |
| **insurance-contracts** | Managed-care contract anatomy: rate methodologies, levels, carve-outs, auth rules, timely filing, the clauses that cost you money — plus patient leveling and negotiation prep | *"Summarize this contract and tell me what to renegotiate"* |
| **compliance** | MDS/PPS/OBRA assessment scheduling, PBJ deadlines, Five-Star mechanics, survey readiness, F-tags, and Plan of Correction drafting | *"Build the assessment calendar for these five admissions"* |
| **census-operations** | Occupancy, payer-mix, and skilled-mix analysis from a raw census export, with trends, red flags, and backfill math | *"Analyze this month's census — what should worry me?"* |
| **prior-auth** | Initial auth packets, continued-stay reviews, peer-to-peer prep, and appeal letters built strictly from your clinical facts | *"Draft the continued-stay review for this resident"* |
| **eligibility** | Medicare benefit-day math, qualifying-stay traps (observation days!), MA plan nuances, and Medicaid-pending risk | *"Does this patient have benefit days left?"* |

Nine skills across eight packs. Each skill carries its reference tables with it
(the NTA point list, the PDPM CMG grids, a 40-term managed-care glossary), so
Claude reads the source material instead of guessing from memory.

## Design principles

1. **Public knowledge, rigorously curated.** Everything comes from published CMS
   methodology and general industry practice — the RAI manual's structure, the
   PDPM final-rule classification logic, the survey process. Nothing proprietary,
   nothing scraped.
2. **No stale numbers.** Rates, coinsurance amounts, and wage indexes change
   every fiscal year, so the skills never hardcode them — they ask for your
   current figures or point you at the current final rule.
3. **Accurate capture, never upcoding.** The billing-adjacent skills are explicit:
   every point, level, and code must be supported by real documentation. The NTA
   skill quotes its evidence line by line for exactly this reason.
4. **Estimates labeled as estimates.** Pre-admission PDPM math is a forecast until
   the MDS is done, and the skills say so.
5. **Your judgment stays in charge.** These are decision-support playbooks, not
   decision-makers. Clinical, billing, and legal calls belong to your licensed
   humans.

## Working with PHI

Skills are prompts and reference files — they transmit nothing anywhere by
themselves. But the documents you'll analyze with them (referral packets, census
exports) usually contain protected health information. Use them the way your
organization already governs AI: under your Claude commercial terms/BAA, with
minimum-necessary data, never in an unmanaged consumer account. When in doubt,
de-identify first.

## Contributing

Corrections, new workflows, and new packs are all welcome — from operators, MDS
coordinators, billers, and builders alike. A rule that changed in this year's
final rule? An issue with a citation is a gift. See
[CONTRIBUTING.md](CONTRIBUTING.md) for ground rules and how to test a change
locally.

## Disclaimer

Educational reference material only — **not** clinical, billing, coding, or
legal advice. Payment rules, rates, and deadlines change every year; always
verify against the current CMS SNF PPS final rule, the current RAI manual, your
state's regulations, and your actual payer contracts. Coding and claims must
always reflect what is genuinely documented in the medical record.

## About Exponential Care

We're the team behind **Referral Triage Pro** — AI-native referral triage and
revenue intelligence for skilled nursing facilities
([exponentialcare.ai](https://exponentialcare.ai)). We work in this industry
every day; these skills open-source the parts of that knowledge that belong to
everyone. If your facility wants the fully automated version — live referral
ingestion, AI extraction, PDPM scenarios priced off your actual contracts —
come say hi.

Licensed under the [MIT License](LICENSE).
