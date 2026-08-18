# Khaya Payroll — SOC 2 Gap Analysis

## 1. Purpose & Methodology

This document assesses Khaya Payroll's current security posture against the SOC 2 Trust Services Criteria, focused on **Security** (the mandatory Common Criteria, CC1–CC9) and **Availability** (selected per [`01-company-scope.md`](./01-company-scope.md) Section 7, given payroll's SLA-driven, must-run-on-time nature).

Each control category is assessed using the same five-part structure applied throughout the [POPIA Gap Assessment](./03-popia-gap-assessment.md):

1. **Requirement summary** — what the criterion requires, in plain English
2. **Current state** — what Khaya Payroll does today (fictional but realistic)
3. **Gap identified** — the specific delta between requirement and current state
4. **Risk rating** — Low / Medium / Medium-High / High, consistent with the scale used in the POPIA assessment
5. **Recommendation** — a specific, actionable fix

Findings are cross-referenced against the POPIA assessment where relevant, since several control areas (accountability, vendor risk, access control, incident response) overlap between the two frameworks.

## 2. Scope

Security (CC1–CC9) and Availability (A1). See [`01-company-scope.md`](./01-company-scope.md) for full company profile, data inventory, and architecture.

---

## 3. Category-by-Category Assessment

### CC1: Control Environment

**Requirement summary:** The organization must demonstrate a commitment to integrity and ethical values, maintain a defined organizational structure with assigned authority and responsibility (including for security specifically), and exercise oversight of the security program — typically evidenced through a formal security policy, assigned ownership, and structured governance activities (e.g. regular reporting or review).

**Current state:** No formal, board-approved security policy exists. No employee has security responsibility explicitly assigned to their role, even informally. Security is not discussed through any regular meetings or reporting structure to assess risks and mitigations — it is only addressed reactively, if and when an issue arises.

**Gap identified:** Without any assigned security ownership, Khaya Payroll cannot demonstrate a defined control environment for security specifically, as required under SOC 2 CC1. This is a related but distinct gap from POPIA Condition 1 (Information Officer): a Data Protection/Information Officer role is oriented toward data protection compliance and data subject rights, not technical security architecture decisions, incident detection, or infrastructure risk — meaning the absence of any security-specific ownership is not fully addressed simply by appointing an Information Officer.

**Risk rating:** High — this is the foundational control environment gap for security, directly analogous to POPIA Condition 1; without assigned ownership, no other security control (CC2–CC9, Availability) can be reliably driven, maintained, or reviewed.

**Recommendation:** Extend the Information Officer's mandate to include security oversight on an interim basis, given the overlapping but distinct skill sets typically required for data protection versus technical security governance. Schedule a formal review in 6 months to assess whether growth indicators — headcount, client volume, or security incident history — justify establishing a dedicated Security Lead role, rather than treating the combined role as a permanent structure.

---

### CC2: Communication & Information

**Requirement summary:** The organization must communicate information necessary to support the functioning of internal control over security, both internally (employees understand their responsibilities and have a way to escalate concerns) and externally (external parties have a clear, legitimate channel to report security concerns).

**Current state:** No security awareness training exists for staff, and there is no formal internal channel (e.g. dedicated email, reporting form) for employees to flag a suspected security issue. Externally, there is no published responsible disclosure policy or dedicated contact (e.g. a security@ email address) for clients, security researchers, or other external parties to report a suspected vulnerability or security concern — leaving no defined point of contact in the event of a disclosed issue or active incident.

**Gap identified:** Without internal security awareness training or a reporting channel, employees are unable to recognize potential security issues or escalate concerns even if they notice something wrong, leaving the organization reliant on chance rather than a functioning reporting culture. Without a published external disclosure channel, a security researcher or client who discovers a vulnerability has no private, responsible way to report it — increasing the likelihood that a real issue is either never reported at all, or is disclosed publicly before Khaya Payroll has an opportunity to remediate it, resulting in reputational damage and potential exploitation by bad actors before a fix is deployed.

**Risk rating:** Medium-High — a step below CC1's severity, since this gap doesn't remove security ownership entirely, but rather blocks the flow of information needed for that ownership to act. If a suspected issue arises, whether from an employee or an external party, there is no defined path to report it and trigger a response — which can delay or prevent mitigation of a real, active issue even if the organization would otherwise be capable of addressing it.

**Recommendation:** Implement regular security awareness training for staff, covering how to recognize common threats (e.g. phishing, suspicious access requests) and how to escalate concerns. Provide an anonymous internal reporting channel so employees can flag suspected issues without fear of appearing mistaken or facing repercussions. Externally, publish a responsible disclosure policy and designate a clear contact point (e.g. a dedicated security@ email address) so clients, researchers, or other external parties have a legitimate, private channel to report vulnerabilities before they are disclosed publicly.

---

*Remaining categories (CC3–CC9, Availability) in progress.*

---

*This assessment is a self-directed GRC portfolio exercise using a fictional company. It does not represent a real audit engagement or legal advice.*
