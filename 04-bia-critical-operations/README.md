# 04. BIA methodology: from processes to Critical Operations

Companion to *The Resilience Bridge*, Edition 4: **Follow the Money**.

Most banks already have a business impact analysis (BIA). This folder shows how to use it as the starting point for Critical Operations and the tolerance for disruption, then test it against the money and the customer harm, and reconcile the two so the Board sees one consistent picture.

> **The logic in one line:** start from the BIA you have, score each service's impact over time, set the tolerance at the service level, then make every recovery time in the BIA fit inside it.

![BIA logic](bia-logic.svg)

## What is inside

| File | What it is |
| --- | --- |
| [`procedure.md`](procedure.md) | The full procedure: eight steps, roles, workshop questions, quality checks, glossary, references |
| [`impact-matrix.md`](impact-matrix.md) | The impact matrix: six categories, five levels, eight points in time, three rules, and a worked example |
| [`bia-toolkit.xlsx`](bia-toolkit.xlsx) | The working model. Score services, and the formulas derive Critical Operations, draft tolerances and a RED / AMBER / GREEN reconciliation |
| [`bia-logic.svg`](bia-logic.svg) | The diagram above |
| `1-impact-scale.csv` to `5-reconciliation-results.csv` | The same data as CSV, for loading into a GRC tool |

## The workbook

| Sheet | What you do | What it calculates |
| --- | --- | --- |
| Start here | Read | |
| 1 Impact scale | Calibrate the descriptors to your risk appetite | |
| 2 Time buckets | Keep or change the points in time and the rule parameters | |
| 3 Service impact | Score each service, six categories, eight points in time | Flags any score that falls over time |
| 4 Service summary | Enter the Board-approved tolerance | Highest score per point in time, first Major impact, Critical Operation yes / no, draft tolerance |
| 5 Process BIA | Enter processes, RTO, RPO, systems, third parties, test results | Each process against its service's tolerance |
| 6 Reconciliation | Read and act | One status and reason per service: the Board report block |

Light yellow cells are inputs. Everything else is a formula.

## The three rules

1. **Highest score, never the average.** A client who cannot be paid does not care that the backlog is fine.
2. **Critical Operation:** any category reaches **Major (4) within one business day.** Edition 4's test: *if this stopped for a day, would the Board need to know before the end of that day?*
3. **Draft tolerance:** the **last point in time before any category reaches Severe (5).** The Board approves the final value.

## What Bank Horizon's example shows

Eight sample services, scored and reconciled:

| Service | Critical? | Tolerance | Status | Why |
| --- | --- | --- | --- | --- |
| Domestic payments | Yes | 4 hours | GREEN | Fits and tested |
| Salary and payroll (payroll day) | Yes | 4 hours | RED | No BIA process mapped: three departments each assumed another owned it |
| Cards authorisation | Yes | 2 hours | RED | The card processor's contract allows 4 hours |
| Trade finance issuance | Yes | 1 day | RED | The old BIA said recover in 5 days, because that is what the platform can do |
| Treasury and liquidity | Yes | 4 hours | AMBER | One process never tested |
| Digital wallet | Not assessed | | RED | Launches in December without a score |
| Corporate lending (new facilities) | No | 3 days | N/A | Clients can wait a day |
| Internal management reporting | No | Over 1 month | N/A | Harms nobody outside the bank |

## Further reading

- ISO/TS 22317:2021, *Guidelines for business impact analysis*: starts at products and services, then processes and activities.
- BCI, *Good Practice Guidelines* (GPG 7.0): product and service, process and activity BIAs.
- Andrew Hiles, *Business Continuity Management: Global Best Practices* (4th edition, Rothstein).
- NIST SP 800-34 Rev. 1: a free BIA template for systems.

> All data is fictional and illustrative. Templates, not legal or regulatory advice. Always check the official texts.

*Created by Dima Alhamouieh. CC BY 4.0.*
