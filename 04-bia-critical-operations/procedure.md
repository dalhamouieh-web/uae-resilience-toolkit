# Procedure: from the BIA to Critical Operations, in four stages

A step-by-step method for banks that already have a business impact analysis (BIA) and need Critical Operations, a tolerance for disruption the Board can approve, a list of critical systems, and evidence an inspector can test.

> Templates, not legal or regulatory advice. Bank Horizon is fictional. Check the official texts that apply to your licence.

**The logic in one line:** screen everything quickly, confirm what matters with scores *and* evidence, map what delivers it, then make every recovery time fit inside the tolerance.

| Stage | Question | Output | Workbook |
| --- | --- | --- | --- |
| 1. Screen | What could matter? | Short list of candidates | Sheet 3 |
| 2. Confirm | What really matters, and for how long? | Board-approved Critical Operations and tolerances | Sheets 4, 5 |
| 3. Map | What delivers it? | Process BIA and critical systems | Sheets 6, 7 |
| 4. Reconcile | Does it all fit? | RED / AMBER / GREEN for the Board | Sheet 8 |

---

## Why this order

Most banks already have a BIA, built for business continuity: department by department, process by process, each with a recovery time objective (RTO). It is the only document the business has already signed, so starting anywhere else wastes it. Industry practice agrees: in Deloitte's 2026 European survey on DORA, most firms identify their critical or important functions through a business-led approach grounded in the BIA.

But a traditional BIA answers *"how long can my team cope?"* The resilience rules ask *"how long can clients and the market cope?"* The international BIA guidance points the same way: ISO/TS 22317 starts at **products and services**, then works down to processes and activities. So the method goes **down**, from the service to the process to the system, and the recovery times must fit the tolerance, not the other way round.

| | Traditional BIA | This method |
| --- | --- | --- |
| Starts from | Departments and processes | Services clients and the market rely on |
| Main number | RTO: when a process or system is back | Tolerance for disruption: when harm becomes intolerable |
| Who sets it | Often what the platform can recover | The harm, backed by evidence, approved by the Board |
| Systems | Everything "important" | Critical only if no workaround or backup, or if bad data causes Major harm |
| How they connect | Separate documents | Every RTO fits inside its service's tolerance |

---

## Roles

| Activity | Business heads | Process owners | BCM team | IT and CISO | Finance | Compliance | Operational and ICT risk (2nd line) | Internal audit | Board |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Design the method and the scale | I | I | R | C | C | C | A | I | I (risk committee approves the scale) |
| Keep the function inventory | A | R | R | C | | | C | I | |
| Stage 1: screen | A | R | R (facilitates) | C | | | C | I | |
| Stage 2: score over time | A | R | R (facilitates) | C | C | C | C (challenges) | I | |
| Stage 2: evidence and challenge | C | C | R | C | R (income) | R (regulatory) | A | I | |
| Stage 2: approve list and tolerances | C | I | I | I | I | I | R | I | A |
| Stage 3: process BIA | A | R | R | R (systems) | | | C | I | |
| Stage 3: critical systems | C | C | C | A/R | | | C (challenges) | I | |
| Stage 4: reconcile and test | C | R | R | R | | | A (validates) | I | I |
| Independent assurance | | | | | | | | A/R | I |

R = does the work, A = accountable, C = consulted, I = informed. Finance challenges the financial scores and Compliance the regulatory ones: the people who know the numbers check them.

---

## Before you start (week 1)

- **Sponsor:** one executive (often the COO or CRO) who can make business heads turn up.
- **Scope:** all licensed activities and locations, including free-zone entities and services provided by the group.
- **Function inventory:** one list of everything the bank does, in two levels: domain (payments, cards, treasury, ...) and function or service ("Corporate clients obtain letters of credit"). Name services as clients see them, not as systems are called. Start from the existing BIA, the product catalogue and the organisation chart.
- **Impact scale:** take [`impact-matrix.md`](impact-matrix.md), calibrate the financial thresholds to your risk appetite, use the same labels as your enterprise risk matrix, and have the risk committee approve it **before** the first workshop.
- **Test the existing BIA** with five questions:

| Test | Question | If the answer is no |
| --- | --- | --- |
| Age | Updated since the last product launch, platform change or major vendor contract? | Rescore the affected services |
| Authors | Did the business fill it in, not only operations and IT? | The client view is missing; plan business workshops |
| Unit | Does it show services clients use from start to finish? | Group processes into services in the inventory |
| Recovery times | Were RTOs set by the harm, not by what the platform can restore? | Flag every RTO for Stage 4 |
| Gaps | Are cross-department processes (payroll, sanctions screening, end of day) and third parties, including intragroup, in it? | Add them; nobody owns them yet, which is the point |

---

## Stage 1: Screen (weeks 1 to 2)

**Question:** what could matter?

For every function in the inventory, one quick score per category (sheet 3): *if this stopped for one full day at the worst moment, how bad would it be, from 1 to 5?* The highest score decides.

- **Moderate (3) or more:** goes to Stage 2.
- **Below:** not critical for now; reviewed every year and whenever something changes.

Screening is deliberately generous. A false alarm costs one workshop; a miss costs a Critical Operation. New products are screened **before** launch.

**Output:** the candidate list. Bank Horizon: 16 functions shown in the example, 11 go to Stage 2.

---

## Stage 2: Confirm (weeks 2 to 5)

**Question:** what really matters, and for how long?

### 2a. Score impact over time

One 90-minute workshop per business line. For each candidate, score the six categories at eight points in time, from 1 hour to 1 month (sheet 4).

- Score the **worst realistic moment** (payroll day, month end, Ramadan, a sales weekend).
- Score **before** workarounds; workarounds are tested in Stage 3, not assumed here.
- Write a sentence of evidence for every 4 or 5.
- The clock starts when the service stops for clients, not when someone notices.

The formulas (sheet 5) then propose:

- **Critical Operation** if any category reaches Major (4) within one business day;
- **Draft tolerance** = the last point in time before any category reaches Severe (5).

### 2b. Check the scores against evidence

Scores are opinions until evidence backs them. For each candidate, the second line collects four facts for the moment the tolerance is reached:

| Evidence | Source | Illustrative threshold |
| --- | --- | --- |
| Share of customers affected | Customer and transaction data | 5% of customers |
| Share of annual income at risk | Finance | 2% of annual income |
| Other banks, payment systems or market infrastructure affected? | Payments, Treasury | Yes |
| Licence or serious regulatory breach? | Compliance | Yes |

The workbook combines scores and evidence into one decision:

| Scores say | Evidence says | Decision |
| --- | --- | --- |
| Critical | Meets a threshold | **Confirmed** |
| Critical | Not collected yet | **Provisional:** collect it before the Board |
| Critical | Below every threshold | **Challenge:** lower the scores with a written reason, or keep with a written reason |
| Not critical | Meets a threshold | **Upgrade:** the evidence wins |
| Not critical | Below every threshold | Not critical |

The thresholds are yours to set; the point is that they are written down **before** the workshops, so nobody tunes them to get the answer they want.

### 2c. Decide and approve

- **Cut the list.** A list that includes everything protects nothing.
- **Add what the rules miss.** Anything a regulator, a payment system or a group policy names as critical goes on the list.
- **Review the non-critical list too.** Once a year, read the full list of non-critical functions and look for anything that looks odd next to the critical ones.
- **Approve.** The Board approves the Critical Operations and their tolerances, and records the approval (sheet 5, yellow column).

**Output:** Board-approved Critical Operations and tolerances. Bank Horizon: five confirmed in the example; corporate lending passed screening but the evidence did not confirm it; the wallet is not assessed yet.

### Workshop questions (in this order)

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

---

## Stage 3: Map (weeks 5 to 7)

**Question:** what delivers it?

### 3a. Process BIA

For each Critical Operation, list the processes that deliver it (sheet 6), and for each one record:

| Field | Why it matters |
| --- | --- |
| Process owner | One named person |
| Peak periods | Recovery must work at the worst moment |
| RTO (hours) | Must fit inside the service's tolerance, with a margin for detection and decision |
| RPO (hours) | How much data can be lost; for payments, usually close to zero |
| Minimum staff and skills | Key-person dependencies |
| Key systems, data, sites | Feed the decision tree below and the map in Edition 5 |
| Third parties, including intragroup | With their contractual recovery time |
| Last tested recovery and date | Evidence, not intention |

**Rule:** RTOs are set **to fit the tolerance**. If a platform cannot recover inside it, that is a finding and an investment decision for the Board, not a reason to widen the tolerance.

### 3b. Which systems are critical? Three questions

For every application that supports a Critical Operation (sheet 7):

```
Does it support a confirmed Critical Operation?
   No  -> not critical (stays in the inventory)
   Yes ->
      Q1 If it is down, does a TESTED workaround keep the service within its tolerance,
         with the staff you actually have?
      Q2 Can another system, already classed as critical, take over?
         No to both       -> CRITICAL (availability)
      Q3 Would wrong, leaked or forged data in it cause Major harm?
         Yes              -> CRITICAL (data)
      Otherwise           -> supporting, not critical
```

Notes:

- **"Tested" means tested.** A workaround that exists only in a procedure, or that needs twice the staff you have, does not count.
- **Availability alone is the minimum.** Many firms stop there. For a bank, a system that is up but sends wrong amounts, leaks data or accepts forged instructions can do as much harm as an outage, so the workbook includes data by default (switch on sheet 2).
- **Every critical system inherits a recovery target:** within its service's tolerance, with a margin.
- **Keep the reason.** "Critical: no workaround or backup within tolerance" is what the inspector will ask for.

**Output:** the process BIA and the critical systems list. Bank Horizon: six critical systems out of eleven in the example; the card fraud engine and the dealing platform are supporting, each with its reason.

---

## Stage 4: Reconcile (week 8, then ongoing)

**Question:** does it all fit?

For each Critical Operation, the workbook (sheet 8) checks:

| Check | Fails when |
| --- | --- |
| Mapped | No process is linked to the Critical Operation |
| RTO | The longest RTO is longer than the tolerance |
| Third parties | A provider's contractual recovery is longer than the tolerance, or than the process RTO |
| Testing | A tested recovery is longer than the RTO or the tolerance, or a process was never tested |
| Approval | The tolerance is still a draft |

**RED** if the service cannot meet its tolerance, **AMBER** if it probably can but the evidence is incomplete, **GREEN** if it fits and has been tested.

Then:

- **Test** against the tolerance with severe but plausible scenarios, including a third-party failure and a cyber attack (Edition 9).
- **Report** the reconciliation as the "Critical Operations vs tolerance" block of the Board report (Edition 1).
- **Refresh** at least annually, and whenever a trigger occurs: a new product, a platform change, a new or changed material third party, a merger, a major incident, a new regulation.
- **Feed back:** next year's BIA starts from the approved Critical Operations and works down.

Bank Horizon's result: payments green; salary run red (no process mapped); cards red (the card processor recovers in 4 hours against 2); trade finance red (5 days against 1); treasury amber (one process never tested); wallet red (not assessed before launch).

---

## Quality checks before anything goes to the Board

| Red flag | Green flag |
| --- | --- |
| The service list is the IT application inventory | Services named as clients see them, each with a business owner |
| Scores filled in by IT or BCM alone | Business heads scored; Finance, Compliance and risk challenged; evidence recorded |
| Thresholds changed after the workshops | Thresholds approved before the first workshop |
| Impact scale differs from the enterprise risk scale | One scale, approved by the risk committee |
| RTOs set by what systems can do | RTOs set to fit the tolerance; gaps go to the Board |
| Every system marked critical | Critical systems chosen by the three questions, each with a reason |
| Workarounds assumed, never tested | Workarounds tested with real staff numbers |
| Third parties a footnote | Every material provider, including intragroup, with its recovery time |
| BIA and Critical Operations list disagree, and nobody noticed | One reconciled set, reported to the Board |

## Glossary

| Term | Meaning here |
| --- | --- |
| Business impact analysis (BIA) | Analysis of the impact of a disruption over time, used to set recovery priorities |
| Critical Operation | A service whose disruption would cause serious harm to clients, the market or the bank (CBUAE term; "critical or important function" under DORA; "critical business service" in the DFSA's proposed framework; "important business service" in the UK) |
| Tolerance for disruption | The longest a Critical Operation can be disrupted before harm becomes intolerable; approved by the Board |
| Maximum tolerable period of disruption (MTPD) | The business continuity term for the time after which impacts become unacceptable; close to the tolerance, but traditionally seen from the organisation's own point of view |
| Recovery time objective (RTO) | The target time to resume a process or system; must be shorter than the tolerance |
| Recovery point objective (RPO) | The maximum data loss, measured in time |
| Critical system | An application whose loss, or whose bad data, would push a Critical Operation beyond its tolerance |

## References

- CBUAE, Operational Risk Management Regulation (2026): identification and mapping of Critical Operations and their dependencies, operational resilience. Check the official text for the articles that apply to your licence.
- ISO 22301:2019, Business continuity management systems: requirements, including the BIA.
- ISO/TS 22317:2021, Guidelines for business impact analysis: product and service level, then processes and activities.
- BCI, Good Practice Guidelines (GPG 7.0, 2018): product and service, process and activity BIAs.
- Basel Committee, Principles for Operational Resilience (2021).
- EU, Digital Operational Resilience Act (DORA): critical or important functions, and identification and classification of the ICT assets that support them.
- Deloitte, European survey on DORA (2026).
- UK FCA SYSC 15A and PRA SS1/21: important business services and impact tolerances.
- NIST SP 800-34 Rev. 1, Contingency Planning Guide for Federal Information Systems: a free BIA template for systems.

*Part of the UAE Resilience Toolkit by Dima Alhamouieh, companion to The Resilience Bridge, Edition 4. CC BY 4.0.*
