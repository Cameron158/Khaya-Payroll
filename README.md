# Khaya Payroll — POPIA & SOC 2 Readiness Assessment

A hands-on GRC portfolio project simulating a real-world compliance readiness assessment for a fictional South African HR/Payroll SaaS company, **Khaya Payroll (Pty) Ltd**.

This project was built as a self-directed case study to demonstrate practical GRC analyst skills: regulatory gap assessment, risk identification and rating, remediation planning, and GRC documentation — applied to a realistic South African SaaS business scenario.

## Project scenario

Khaya Payroll is a Cape Town-based SaaS platform providing cloud payroll and HR management to South African SMEs. After signing its first large enterprise client — whose procurement team requires proof of POPIA compliance and a SOC 2 report — Khaya Payroll commissioned a readiness assessment ahead of engaging an external auditor. No formal compliance assessment had previously been conducted; policies existed informally with no documentation.

Full company profile, data inventory, and technology scope are documented in [`01-company-scope.md`](./01-company-scope.md).

## What's in this repo

| File | Description |
|---|---|
| `01-company-scope.md` | Company profile, data inventory, architecture overview, and assessment scope |
| `02-data-flow-diagram/` | draw.io data flow diagram mapping personal information flows across internal systems and third-party sub-processors (source `.drawio` + exported `.svg`) |
| `03-popia-gap-assessment.md` | Full gap assessment across all 8 POPIA Conditions for Lawful Processing, with risk ratings and a phased remediation roadmap |
| `04-soc2-gap-analysis.md` | Gap analysis against SOC 2 Trust Services Criteria (Security + Availability) *(in progress)* |
| `risk_scorer.py` | Python script automating risk scoring and tiering for the project's risk register |

## Frameworks applied

- POPIA (Protection of Personal Information Act, No. 4 of 2013) — full 8-Condition assessment
- SOC 2 — Trust Services Criteria: Security (Common Criteria CC1–CC9) + Availability

## Methodology

Each finding follows a consistent structure to keep the assessment auditable and easy to navigate:

1. Requirement summary — what the framework actually requires, in plain English
2. Current state — what the (fictional) company does today
3. Gap identified — the specific delta between requirement and reality
4. Risk rating — Low / Medium / Medium-High / High, with explicit reasoning
5. Recommendation — a specific, actionable fix, not a vague statement

Findings are cross-referenced where they compound one another (e.g. the missing Information Officer affects multiple other findings), and consolidated into a phased remediation roadmap (Foundational → Short-term → Ongoing) sequenced by dependency and severity.

## Risk Register Auto-Scorer

To support the ongoing risk assessment work, a Python script was built to automate risk scoring and tiering, using the same rating scale established for this project (Low / Medium / Medium-High / High).

**Location:** `risk_scorer.py`

**Logic:**
- Risk Score = Likelihood Rating (1-5) × Impact Rating (1-5), giving a range of 1-25
- Tiers: Low (1-6), Medium (7-12), Medium-High (13-18), High (19-25)

**Usage:**
```bash
python3 risk_scorer.py risk_register.csv
