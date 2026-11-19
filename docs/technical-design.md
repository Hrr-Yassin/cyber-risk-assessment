# Technical design

**Phase 0 specification**

Run a context and BIA workshop on confidentiality, integrity, availability and critical dependencies. Propose order-portal RTO 8 hours and RPO 4 hours as fictional objectives to validate with service owners. Record threat source, event, pathway, asset, business impact, current controls, likelihood evidence and uncertainty. Map control gaps to an owner and evidence artifact. Choose avoid, reduce, transfer or accept, then reassess residual risk after evidence, set review dates and obtain explicit sign-off above threshold. Document policies for access, backup, incident escalation and supplier review, with review cadence and authority. Proposed KPIs: percentage of treatment actions past due, quarterly restore success rate, MFA coverage over in-scope accounts, and incident escalation time.

## Fictional 5 × 5 risk matrix

Rows are likelihood (1 rare, 2 unlikely, 3 possible, 4 likely, 5 frequent over the agreed horizon). Columns are impact (1 minor, 2 limited, 3 material, 4 major, 5 severe), anchored in business downtime, financial loss and data sensitivity. Assess horizon and uncertainty in the record.

| Likelihood / Impact | 1 | 2 | 3 | 4 | 5 |
| --- | ---: | ---: | ---: | ---: | ---: |
| 1 | 1 | 2 | 3 | 4 | 5 |
| 2 | 2 | 4 | 6 | 8 | 10 |
| 3 | 3 | 6 | 9 | 12 | 15 |
| 4 | 4 | 8 | 12 | 16 | 20 |
| 5 | 5 | 10 | 15 | 20 | 25 |

Multiplication is an ordinal prioritization aid, not a loss estimate. Proposed decision bands are 1–4 low, 5–9 moderate, 10–14 high and 15–25 critical. Assign high/critical reviews to executive ownership. Material but low-likelihood outcomes still warrant review.

## Technology rationale

Use ISO/IEC 27001:2022 with Amendment 1:2024 as the ISMS reference, 27002:2022 for control guidance and 27005:2022 for risk management. NIST CSF 2.0 describes target outcomes. CIS Controls v8.1 offers prioritized safeguards. ANSSI EBIOS Risk Manager guide v1.5 (September 2024) supports structured scenario workshops. Maintain Markdown and a structured tabular register for low operating cost.

See [acceptance criteria](testing-strategy.md) and [authoritative references](references.md).

## Illustrative control mapping

| Scenario | Control intent | Illustrative mapping | Proposed evidence |
| --- | --- | --- | --- |
| SaaS account compromise | Restrict access and monitor account changes | CSF PR.AA, CIS Control 6 | Fictional ID inventory, MFA denominator and access review |
| Provider outage | Assign dependency owner and restore business service | CSF GV.SC and RC.RP, CIS Control 11 for data recovery | Supplier contact, tabletop timestamps and recovery check |
| Incident escalation delay | Establish and exercise incident roles | CSF RS.MA, CIS Control 17 | Role roster, escalation log and exercise findings |

Use the ISO/IEC 27002 control guidance and authorized texts for detailed mapping during a future review. Document plausible control limitations and measure their operational outcomes. Gap assessment should identify current evidence, target behavior, agreed action and due date.
