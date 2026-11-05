# BIA procedure: from processes to Critical Operations

A step-by-step method for banks that already have a business impact analysis (BIA) and need to turn it into Critical Operations with a tolerance for disruption that the Board can approve and an inspector can test.

**The logic in one line:** start from the BIA you have, test it against the money and the customer harm, set the tolerance at the service level, then make the BIA fit inside it.

> Templates, not legal or regulatory advice. Bank Horizon is fictional. Check the official texts that apply to your licence.

---

## Why this order

Most banks already have a BIA, built for business continuity: department by department, process by process, each with a recovery time objective (RTO). It is the only document the business has already signed, so starting anywhere else wastes it.

But a traditional BIA answers *"how long can my team cope?"* The operational resilience rules ask *"how long can clients and the market cope?"* The international BIA guidance points the same way: ISO/TS 22317 starts the analysis at the level of **products and services**, then works down to processes and activities. So the method goes **down**, not up:

```
Business strategy and income
        |
Services clients rely on  ->  impact over time  ->  Critical Operation?  ->  tolerance (Board)
        |
Processes behind each service  ->  RTO, RPO, people, systems, data, sites, third parties
        |
Reconcile: does every recovery time fit inside the tolerance?  ->  test  ->  report  ->  refresh
```

| | Traditional BIA | This method |
| --- | --- | --- |
| Starts from | Departments and processes | Services clients and the market rely on |
| Main number | RTO: when a process or system is back | Tolerance for disruption: the point where harm becomes intolerable |
| Who sets it | Often what the platform can recover | The harm, approved by the Board |
| How they connect | Separate documents | Every RTO must fit inside its service's tolerance |

---

## Roles

| Activity | Business heads | Process owners | BCM team | IT and CISO | Procurement | Operational risk (2nd line) | Internal audit | Board |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Approve the impact scale | C | I | R | I | I | A | I | I (risk committee approves) |
| Build the service list | A | C | R | I | I | C | I | I |
| Score impact over time | A | R | R (facilitates) | C | C | C (challenges) | I | |
| Propose Critical Operations and tolerances | A | C | R | C | C | C (challenges) | I | |
| Approve tolerances | C | I | I | I | I | R | I | A |
| Process BIA (RTO, RPO, dependencies) | A | R | R | R (systems) | R (third parties) | C | I | |
| Reconcile and test | C | R | R | R | C | A (validates) | I | I |
| Independent assurance | | | | | | | A/R | I |

R = does the work, A = accountable, C = consulted, I = informed.

---

## Step 0: prepare (week 1)

- **Sponsor:** one executive (often the COO or CRO) who can make business heads turn up.
- **Scope:** all licensed activities, all locations, including free-zone entities and intragroup services.
- **Impact scale:** take [`impact-matrix.md`](impact-matrix.md), calibrate the financial thresholds to your risk appetite, align the labels with your enterprise risk framework, and have the risk committee approve it **before** the first workshop. Changing the scale mid-way invalidates every score.
- **Calendar:** book one 90-minute workshop per business line now.

**Output:** approved scale, timeline, workshop calendar.

## Step 1: take out the BIA you already have, and test it (week 1)

Do not throw it away; interrogate it.

| Test | Question | If the answer is no |
| --- | --- | --- |
| Age | Updated since the last product launch, platform change or major vendor contract? | Mark the affected processes for rescoring |
| Authors | Did the business fill it in, not only operations and IT? | The client view is missing; plan business workshops |
| Unit | Does it show services clients use from start to finish? | Group processes into services in step 2 |
| Recovery times | Were RTOs set by the harm, not by what the platform can restore? | Flag every RTO for reconciliation in step 6 |
| Gaps | Are cross-department processes (payroll, sanctions screening, end of day) and third parties, including intragroup, in it? | Add them; nobody owns them yet, which is the point |

**Output:** a list of what you can keep, what to rescore and what is missing.

## Step 2: build the service list from the money and the customers (weeks 1 to 2)

Use four inputs, not one:

1. **The income statement** by business line: where the money is.
2. **The product catalogue and client segments:** what clients actually use.
3. **Obligations:** salary payments, sanctions screening, regulatory reporting, payment system membership.
4. **The existing BIA:** group its processes into the services they deliver.

Name each service as the client sees it ("Corporate clients obtain letters of credit"), not as the system is called ("Trade platform"). Give each one a business owner.

**Output:** a draft list of services with owners. Bank Horizon had 31 critical processes in the old BIA; grouped into services they became about 20 candidates.

## Step 3: score impact over time (weeks 2 to 4)

One workshop per business line. For each service, score the six categories at the eight points in time using the matrix.

- Score the **worst realistic moment** (payroll day, month end, quarter end, Ramadan, a sales weekend).
- Score **before** workarounds; workarounds are tested later, not assumed now.
- Write a sentence of evidence for every 4 or 5.
- The second line attends and challenges scores that look too low or too convenient.

**Output:** sheet 3 of the workbook, one block per service.

### Workshop questions (use them in this order)

1. Who uses this service, and how many of them?
2. When is the worst moment for it to stop?
3. After one hour, what do clients notice? After four? After a day?
4. When does a client start to suffer real harm: money not paid, a deadline missed, a penalty?
5. Do other banks, payment systems or markets depend on it?
6. Which legal or regulatory duty would we break, and when?
7. When would the media or social media notice?
8. Could we catch up on the backlog afterwards, or is something lost for good?
9. What do you depend on that you do not control: other teams, systems, vendors, group entities?
10. If this stopped for a day, would you want the Board to know before the end of that day?

## Step 4: classify and set the tolerance (week 5)

The workbook applies the rules automatically (sheet 4):

- **Critical Operation** if any category reaches Major (4) within one business day.
- **Draft tolerance** = the last point in time before any category reaches Severe (5).

Then apply judgement:

- **Cut the list.** A list that includes everything protects nothing. Bank Horizon went from about 20 candidates to 12 Critical Operations.
- **Add what the rules miss.** Anything a regulator, a payment system or a group policy names as critical goes on the list regardless of score. New products are scored before launch (Bank Horizon's wallet).
- **Challenge.** The second line writes a short challenge note for each tolerance.
- **Approve.** The Board approves the list and the tolerances, and records the approval.

**Output:** Board-approved Critical Operations and tolerances (sheet 4, yellow column).

## Step 5: process BIA for each Critical Operation (weeks 5 to 7)

Now go down. For each Critical Operation, list the processes that deliver it, and for each process record:

| Field | Why it matters |
| --- | --- |
| Process owner | One named person |
| Peak periods | Recovery must work at the worst moment |
| RTO (hours) | Must fit inside the service's tolerance, with a margin for detection and decision |
| RPO (hours) | How much data can be lost; for payments, usually close to zero |
| Minimum staff and skills | Key-person dependencies (Bank Horizon's Faisal) |
| Key systems | Feeds the IT recovery plan and the map in Edition 5 |
| Data | Where it lives and how it is restored |
| Sites | Office, data centre, alternate site |
| Third parties, including intragroup | With their contractual recovery time |
| Last tested recovery and date | Evidence, not intention |

**Rule:** RTOs are set **to fit the tolerance**, not the other way round. If a platform cannot recover inside the tolerance, that is a finding and an investment decision for the Board, not a reason to widen the tolerance.

**Output:** sheet 5 of the workbook.

## Step 6: reconcile (week 8)

For each Critical Operation, the workbook (sheet 6) checks:

| Check | Fails when |
| --- | --- |
| Mapped | No process is linked to the Critical Operation |
| RTO | The longest RTO is longer than the tolerance |
| Third parties | A provider's contractual recovery is longer than the tolerance, or than the process RTO |
| Testing | Tested recovery is longer than the RTO or the tolerance, or a process was never tested |
| Approval | The tolerance is still a draft |

Status: **RED** if the service cannot meet its tolerance, **AMBER** if it probably can but the evidence is incomplete, **GREEN** if it fits and has been tested.

Bank Horizon's result: payments green; salary run red (no process mapped); cards red (the card processor recovers in 4 hours against a 2-hour tolerance); trade finance red (5 days against 1 day); treasury amber (one process never tested); wallet red (not assessed before launch).

**Output:** the reconciliation, with an owner and a date for every red and amber.

## Step 7: test, report, refresh (ongoing)

- **Test** against the tolerance, using severe but plausible scenarios, including a third-party failure and a cyber attack (Edition 9).
- **Report** the reconciliation as the "Critical Operations vs tolerance" block of the Board report (Edition 1).
- **Refresh** at least annually, and whenever a trigger occurs: a new product, a platform change, a new or changed material third party, a merger or restructuring, a major incident, or a new regulation.
- **Feed back:** next year's BIA starts from the approved Critical Operations and works down, so it never drifts back to department-by-department.

---

## Quality checks before anything goes to the Board

| Red flag | Green flag |
| --- | --- |
| The service list is the IT application inventory | Services named as clients see them, each with a business owner |
| Scores were filled in by IT or BCM alone | Business heads scored; risk challenged; evidence recorded |
| Impact scale differs from the enterprise risk scale | One scale, approved by the risk committee |
| RTOs set by what systems can do | RTOs set to fit the tolerance; gaps go to the Board |
| Payroll, screening and end-of-day missing because nobody owns them | Cross-department processes mapped with an owner |
| Third parties a footnote | Every material provider, including intragroup, with its recovery time |
| No test evidence, or tests that only restore a server | Tests show the service back for clients within tolerance |
| BIA and Critical Operations list disagree, and nobody noticed | One reconciled set, reported to the Board |

## Glossary

| Term | Meaning here |
| --- | --- |
| Business impact analysis (BIA) | Analysis of the impact of a disruption over time, used to set recovery priorities |
| Critical Operation | A service whose disruption would cause serious harm to clients, the market or the bank (CBUAE term; "critical or important function" under DORA; "critical business service" in the DFSA's proposed framework; "important business service" in the UK) |
| Tolerance for disruption | The longest a Critical Operation can be disrupted before harm becomes intolerable; approved by the Board |
| Maximum tolerable period of disruption (MTPD) | The business continuity term for the time after which impacts become unacceptable; close to tolerance, but traditionally measured from the organisation's own point of view |
| Recovery time objective (RTO) | The target time to resume a process or system; must be shorter than the tolerance |
| Recovery point objective (RPO) | The maximum data loss, measured in time |

## References

- CBUAE, Operational Risk Management Regulation (2026): identification and mapping of Critical Operations and their dependencies, operational resilience. Check the official text for the exact articles that apply to your licence.
- ISO 22301:2019, Business continuity management systems: requirements, including the BIA.
- ISO/TS 22317:2021, Guidelines for business impact analysis: product and service level, then processes and activities.
- BCI, Good Practice Guidelines (GPG 7.0, 2018): product and service, process and activity BIAs.
- Basel Committee, Principles for Operational Resilience (2021).
- EU, Digital Operational Resilience Act (DORA): critical or important functions.
- UK FCA SYSC 15A and PRA SS1/21: important business services and impact tolerances, the model many regulators followed.
- NIST SP 800-34 Rev. 1, Contingency Planning Guide for Federal Information Systems: a free BIA template for systems (maximum tolerable downtime, RTO, RPO).

*Part of the UAE Resilience Toolkit by Dima Alhamouieh, companion to The Resilience Bridge, Edition 4. CC BY 4.0.*
