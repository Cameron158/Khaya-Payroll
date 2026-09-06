**Khaya Payroll — Company & Scope Document**

---
1. Company Overview
Company Name: Khaya Payroll (Pty) Ltd Tagline: Payroll and HR, simplified for growing SA businesses. Founded: 2022 Headquarters: Cape Town, South Africa Team size: ~35 employees (engineering, customer success, sales, and a 2-person compliance/finance team)
Business description: Khaya Payroll is a cloud-based SaaS platform providing payroll processing and core HR management for South African SMEs (10–250 employees). The platform automates monthly payroll runs, PAYE/UIF/SDL statutory calculations and submissions to SARS, leave management, and employee self-service (payslips, leave requests, personal detail updates).
Customer base: ~180 SME clients, approximately 40,000 employee records processed monthly across all clients combined. Client industries include retail, hospitality, professional services, and a small number of NGOs.
---

3. Data Processed

## Data Classification & Sensitivity

| Data Category | Examples | Sensitivity Notes |
| :--- | :--- | :--- |
| **Identity data** | Full names, SA ID numbers, tax numbers | **High** — ID numbers are a POPIA-sensitive identifier |
| **Financial data** | Banking details, salary/remuneration history | **High** — direct fraud/financial harm potential |
| **Leave & medical data** | Sick leave records, some medical certificates | Potentially "special personal information" under POPIA s26 |
| **HR records** | Employment contracts, disciplinary records (subset of clients) | **Medium–High** |
| **Contact data** | Emergency contacts, personal email/phone | **Medium** |

3. Technology Architecture (High Level)
Hosting: AWS, af-south-1 (Cape Town region)
Application: Multi-tenant web app; tenant data logically separated by client ID in PostgreSQL
Third-party integrations:
Payment gateway (salary disbursement runs)
SARS eFiling API (statutory submissions)
SendGrid (transactional email — payslip notifications)
Intercom (customer support)

4. POPIA Roles
Khaya Payroll = Operator — processes personal information on behalf of clients, per client instruction
Each client company = Responsible Party — determines the purpose and means of processing their own employees' data
This dual-role relationship means Khaya Payroll requires operator agreements (POPIA s21) with each client, and this is expected to surface as an early gap

5. Assessment Trigger / Business Driver
Khaya Payroll has signed its first large enterprise client (a 200-person retail chain) whose procurement team has requested a SOC 2 report and proof of POPIA compliance as a condition of the contract. No formal compliance assessment has previously been conducted — policies exist informally (Slack messages, founder knowledge) but are undocumented. The founders have commissioned this readiness assessment ahead of engaging an external auditor for a future SOC 2 examination.
6. Assessment Scope
In scope:
Personal information processing activities related to payroll and HR functions
Application infrastructure hosted on AWS (af-south-1)
Third-party subprocessors listed in Section 3
Internal access controls and employee data-handling practices
Out of scope:
Marketing website and lead-generation systems (no employee PII processed there)
Physical office security (assessment is focused on the SaaS platform itself)

7. Frameworks Applied
POPIA (Protection of Personal Information Act, No. 4 of 2013) — full Conditions for Lawful Processing assessment
SOC 2 — Trust Services Criteria, Security (mandatory) + Availability (selected as relevant to a payroll SLA-driven product)




