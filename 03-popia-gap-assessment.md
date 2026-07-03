Condition 1: Accountability (POPIA s8)

Requirement summary: 

The Responsible Party (or Operator) must ensure  POPIA's conditions for lawful processing are complied with, both when  determining the purpose and means of processing, and throughout the  processing itself.

Current state: 

Data protection queries are handled informally and on  an ad hoc basis by the CEO, who has no formally documented responsibility  for this function. There is no designated Information Officer, no deputy,  and no written escalation path for POPIA-related requests.

Gap identified: 

No Information Officer has been formally registered  with the Information Regulator. Because accountability for POPIA compliance  sits with no single formally responsible person, there is no mechanism to  ensure oversight across any of the other 7 conditions — this is a  foundational gap rather than an isolated one.

Risk rating:  High 

Accountability is the foundational condition;  without a designated owner, there is no mechanism to ensure oversight,  drive remediation, or respond to regulatory or data subject requests  across any of the other 7 conditions.

Recommendation: 

Register the CEO as Information Officer with the  Information Regulator, appoint a Deputy Information Officer to share  operational responsibility, and establish a documented escalation path  (including a data subject request response procedure) so POPIA-related  matters have clear ownership and a defined process rather than relying  on informal, ad hoc handling.















Condition 2: Processing Limitation (POPIA s9–12)

Requirement summary: 

Personal information must be processed lawfully  and without excessive infringement of privacy, collection must be minimal  (only what's necessary for the purpose), a valid legal basis must exist  (consent, contract necessity, legal obligation, or legitimate/vital  interest), and data should be collected directly from the data subject  where reasonably possible.

Current state:

There is no defined policy governing how much medical  detail is captured for sick leave documentation. Some client HR admins may  upload full medical certificates with diagnosis details, while others may  record only leave dates — the level of detail collected is inconsistent  and left to individual admin discretion rather than a documented  minimum-necessary standard.

Gap identified:

Two distinct gaps exist under this condition. First, there is a risk of over-collection of special personal information  (medical/health data) since no defined minimum necessary standard governs  how much detail HR admins capture for sick leave documentation. Second,  while valid legal bases exist for processing core payroll data (contract  necessity for banking/salary data, legal obligation for tax/statutory  data), this has not been formally documented — meaning Khaya Payroll  cannot readily demonstrate which legal basis applies to which data  category if challenged by the Information Regulator or a data subject.

Risk rating: Medium-High 

While less foundational than the  Accountability gap (Condition 1), unauthorized processing or  over-collection of special personal information (health data) carries  elevated regulatory and reputational consequences under POPIA due to the  sensitivity of the data category, even though likelihood of a specific  incident is currently unconfirmed.

Recommendation:

Define and document a minimum-necessary standard for  medical/leave data collection (e.g. capturing only leave dates and general  fitness-for-duty status rather than full diagnostic detail) to align with  the special personal information requirements under POPIA s26. Separately,  create a data category-to-legal-basis mapping record — documenting that  contract necessity applies to core payroll data (banking, salary) and  legal obligation applies to statutory/tax data — so Khaya Payroll can demonstrate a defensible legal basis for each processing activity if challenged.


















Condition 3: Purpose Specification (POPIA s13–14)

Requirement summary: 

Personal information must be collected for a  specific, explicitly defined, and lawful purpose, and the data subject  must be made aware of that purpose. Personal information may not be  retained longer than necessary to achieve that purpose, unless a law  (e.g. SARS record-keeping requirements) requires longer retention.

Current state:

As the Responsible Party, each client company is  legally responsible for informing employees about the purpose, extent,  and retention period of their data processing. However, Khaya Payroll  (as Operator) does not currently provide any privacy notice template,  in-platform disclosure, or documentation to support clients in meeting  this obligation. No data retention policy exists to define how long  former employees' payroll and HR records are retained after their  employment ends or after a client company offboards them from the  platform. Records persist indefinitely by default, with no scheduled deletion, archival, or review process in place.

Gap identified:

There is no standard privacy notice or disclosure  process to help client companies inform employees what data is collected, for what purpose, and for how long — leaving most employees unaware of how their information is being used. There is also no data retention policy governing what happens to an employee's records once they leave a client company, meaning records are neither reviewed, updated, nor securely deleted, and simply persist indefinitely by default. (Note: this connects to a related access control gap — see Condition 7 — where departed staff's system access is also not consistently deprovisioned.)

Risk rating: Medium-High 

Similar severity to Condition 2, since  the absence of a retention policy means the pool of exposed personal  information (including banking details, ID numbers, and salary history) grows continuously over time with no review or deletion checkpoint, compounding risk the longer it remains unaddressed.

Recommendation:

Provide client companies with a standard privacy notice template covering what data is collected, for what purpose, and for how long, to support their Responsible Party obligations under POPIA. Implement a documented data retention policy specifying a 5-year retention period aligned with SARS record-keeping requirements, with two distinct triggers: (1) system access must be removed within 2 weeks of an employee being flagged as terminated (urgent, security-driven), and (2) the employee's full data record must undergo a documented review within the retention cycle to determine deletion or continued archival (compliance-driven, tracked but not urgent).














Condition 4: Further Processing Limitation (POPIA s15)

Requirement summary:

Personal information collected for one purpose may not be processed for a different, incompatible purpose without a new legal basis or the data subject's awareness, unless the new purpose is 
compatible with the original one (assessed by factors such as the relationship between purposes, the nature of the data, and data subject expectations).

Current state:

Khaya Payroll integrates with several third-party sub-processors (Intercom, SendGrid, Payment Gateway) that receive or process data originating from the payroll/HR platform. No due diligence 
has been conducted on these providers' own data processing practices, retention terms, or further-use policies — for example, whether Intercom uses support ticket content (which may include employee PII pasted in by admins) for product improvement, analytics, or model training.

Gap identified:

There is no sub-processor risk assessment process to evaluate whether third-party tools handling Khaya Payroll data might process that data for purposes beyond the original payroll/HR function it was collected for. Without reviewing each provider's terms and data processing agreements, Khaya Payroll cannot confirm whether further processing is occurring, nor can it demonstrate compliance with POPIA's Further Processing Limitation condition to the Information Regulator or to client companies acting as Responsible Parties.

Risk rating: Medium-High 

while no evidence currently suggests active misuse by third-party sub-processors, the absence of any vendor due diligence process means Khaya Payroll cannot demonstrate compliance if questioned by the Information Regulator or a client, and any PII inadvertently shared with these tools (e.g. via support tickets) sits entirely outside Khaya Payroll's visibility or control.

Recommendation:

Establish Data Processing Agreements (DPAs) with all third-party sub-processors (Intercom, SendGrid, Payment Gateway) as required under POPIA s21, ensuring each provider is contractually bound to maintain equivalent security safeguards. Supplement this with a vendor due diligence process — requesting evidence such as SOC 2 Type II reports or ISO 27001 certification — before onboarding, and require the same vetting for any new third-party tools added in future.



















Condition 5: Information Quality (POPIA s16)

Requirement summary:

A Responsible Party (and Operators acting on their behalf) must take reasonably practicable steps to ensure personal information is complete, accurate, not misleading, and updated where necessary, considering the purpose for which it is collected or used.

Current state:

There is no dedicated individual or process responsible for validating data accuracy after entry. Employees can update their own information — such as banking details or ID numbers — via the self-service portal, and HR admins can also make changes directly, but no validation step (e.g. confirmation checks, secondary approval, or periodic accuracy reviews) exists once data is entered.

Gap identified: 

Because no validation step exists, Khaya Payroll cannot demonstrate that reasonably practicable steps have been taken to ensure data accuracy and integrity, as required under POPIA s16. This creates risk of mispayments, financial harm to employees, and the operational burden of manually tracing and correcting errors after the fact.

Risk rating: Medium-High 

While a single inaccurate record may cause limited, contained harm (one employee, one payment cycle), the risk scales with the volume of change events (e.g. bulk updates during retrenchments, restructuring, or high staff turnover among client companies), where the absence of validation could result in multiple simultaneous mispayments across many employees at once.

Recommendation:

Implement a confirmation step for sensitive field updates — when an employee changes banking details, ID number, or tax number via self-service, require a secondary confirmation (e.g. email or in-app verification) before the change takes effect. Supplement this with a periodic automated data quality scan that flags incomplete or missing required fields, and identifies anomalies such as duplicate bank account numbers across different employee records (which could indicate a conflicting or fraudulent update) — with flagged records routed for manual review before the next payroll run.



















Condition 6: Openness (POPIA s17–18)

Requirement summary:

The Responsible Party must maintain documentation of all processing operations (a Record of Processing Activities), and data subjects must be notified of specific information at the point of collection, including the purpose of processing, whether providing information is mandatory or voluntary, and their rights (e.g. access, correction, objection).

Current state: 

No Record of Processing Activities (ROPA) exists documenting the categories of personal information processed, the purpose and legal basis for each processing activity, which parties (internal or third-party) have access to the data, and how long it is retained. Building on the gap identified in Condition 3, employees are also not informed of their rights under POPIA, including the right to access their own data, request correction of inaccurate information, or object to certain processing activities.

Gap identified:

Without a ROPA, Khaya Payroll cannot readily demonstrate to the Information Regulator what data is processed, for what purpose, and by whom, if investigated or audited. Without informing employees of their rights, Khaya Payroll and its client companies (as Responsible Parties) risk non-compliance with POPIA's Openness condition, and have no defined process to handle a rights request if an employee were to exercise a right (such as requesting access to their data) that they were never informed they had in the first place.

Risk rating: High 

This finding compounds the risks already identified in Condition 1 (no accountable owner) and Condition 3 (no purpose disclosure); without documentation of processing activities or awareness of data subject rights, Khaya Payroll has no defensible position if the Information Regulator investigates, and employees have no practical means of exercising rights (access, correction, objection) they don't know exist.

Recommendation:

The Information Officer (once designated per Condition 1) should own the creation and ongoing maintenance of a Record of Processing Activities (ROPA), documenting data categories, purpose, legal basis, third-party access, and retention periods for each processing activity. Separately, publish a clear, accessible summary of employee data subject rights (access, correction, objection) within the self-service portal, and support the rollout with an HR-led workshop for client companies to ensure awareness and correct implementation going forward.
















Condition 7: Security Safeguards (POPIA s19–22)

Requirement summary:

The Responsible Party (and Operators) must implement appropriate technical and organizational measures to prevent loss, damage, or unauthorized access to personal information; ensure Operators process data under written contract with equivalent security standards; and notify the Information Regulator and affected data subjects as soon as reasonably possible in the event of a security compromise.

Current state:

Access to the platform is currently controlled only by username and password, with no multi-factor authentication (MFA) and no confirmed encryption of sensitive fields (banking details, ID numbers). As identified in Condition 3, there is no consistent process for revoking departed employees' access. Internally, Khaya Payroll staff at admin level and above have broad, standing access to production data across all client accounts, with no logging in place to record what data was viewed, edited, or by whom. No documented incident response plan exists for handling a security compromise — including steps for containment (e.g. a lost or stolen device with database access), internal escalation, or investigation. While POPIA does not prescribe a fixed notification deadline, the absence of any documented plan or internal timeline makes it difficult to demonstrate that Khaya Payroll acted without unreasonable delay.

Gap identified:

Across both technical and organizational dimensions, Khaya Payroll cannot demonstrate that reasonable security safeguards are in place as required under POPIA s19. On the technical side, single-factor authentication, unconfirmed encryption of sensitive fields, and broad unlogged internal access to production data create multiple avenues for unauthorized access or undetected misuse. On the organizational side, the absence of a documented incident response plan means that even if a compromise occurred, Khaya Payroll has no defined process for containment, investigation, or timely notification to the Information Regulator and affected data subjects under s22.

Risk rating: High  

This finding combines multiple compounding weaknesses (weak authentication, no encryption confirmation, unlogged broad access, and no incident response capability) affecting the entire platform's ~40,000 employee records across all 180 client companies. While rated at the same tier as Conditions 1 and 6, this finding carries the broadest technical exposure in the assessment, since it affects prevention and response simultaneously rather than a single control area.

Recommendation:

Implement multi-factor authentication (MFA) for all platform logins, enforce role-based access control (RBAC) so access is scoped to only what each user's role requires, and encrypt sensitive data fields (banking details, ID numbers) both at rest and in transit. Implement logging of all changes made to employee records — capturing what was changed, by whom, and when — with logs reviewed on a weekly basis. Develop and document a formal incident response plan covering scenarios such as lost or stolen hardware, unauthorized access, and data compromise, incorporating a self-imposed 72-hour notification benchmark aligned with international best practice (GDPR) to demonstrate a diligent, well-managed response consistent with POPIA s22's "reasonably possible" standard.






Condition 8: Data Subject Participation (POPIA s23–25)

Requirement summary:

A data subject has the right to request confirmation of, and access to, personal information held about them (s23); to request correction, deletion, or destruction of inaccurate, irrelevant, excessive, outdated, incomplete, misleading, or unlawfully obtained information (s24); and must be notified of the action taken in response to such a request (s25).

Current state:

There is no standard procedure for handling data subject requests — including requests to access, correct, or delete personal information under POPIA s23–24. When a client's employee raises such a request, it often goes unmet or unresolved, since there is no defined process, owner, or timeline for actioning it. Additionally, when corrections are made to sensitive employee data, there is no confirmation sent back to the employee to verify the action was completed, as required under s25.

Gap identified: 

Without a defined data subject request process, Khaya Payroll and its client companies risk reputational harm — loss of trust among employees and the broader community — as well as direct legal exposure if the Information Regulator receives a complaint from an employee whose request went unanswered. This gap is compounded by the finding in Condition 6: employees are not even informed that these rights exist in the first place, meaning the absence of a request process is currently masked by low awareness — but that risk will surface as awareness improves unless this operational gap is fixed in parallel.

Risk rating:  High 

Comparable in severity to Conditions 6 and 7, though slightly dependent on Condition 6's rollout (awareness), since this operational gap becomes more consequential as employees learn their rights exist.

Recommendation:

Implement a data subject request form accessible directly through the employee self-service portal, allowing employees to formally request access to, correction of, or deletion of their personal information without requiring an in-person meeting. Route submitted requests to the Information Officer (or Deputy Information Officer, per Condition 1) for action within a self-imposed 72-hour benchmark, exceeding POPIA's "reasonable time" standard to demonstrate proactive compliance. For correction requests specifically, implement a confirmation notification sent to the employee once the update is completed, allowing them to review and confirm accuracy (with deletion/removal requests routed through a separate, more controlled review process, given the higher risk of irreversible action).













