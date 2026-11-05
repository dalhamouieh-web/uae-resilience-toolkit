# The BIA impact matrix

The matrix answers one question for every service the bank offers: **how bad does it get, for whom, and how fast?**

It has three parts: six impact categories, a five-level severity scale, and eight points in time. You score each service in each category at each point in time, then apply three rules.

## 1. Six impact categories

The first two look outward. That is the difference between a traditional BIA, which asks "how long can my team cope?", and a resilience view, which asks "how long can our clients and the market cope?"

| Category | What it measures |
| --- | --- |
| Customer harm | Can customers pay, get paid, reach their money or use the service? |
| Market and financial system | Are other banks, payment systems or the wider market affected? |
| Financial loss | Direct loss, lost income, penalties, compensation, lost clients |
| Regulatory and legal | Breach of a regulatory, legal or contractual duty |
| Reputation | Media, social media, client and investor confidence |
| Operational backlog | Can the backlog be recovered, and is data lost? |

## 2. Five severity levels

| Category | 1 Minimal | 2 Minor | 3 Moderate | 4 Major | 5 Severe |
| --- | --- | --- | --- | --- | --- |
| Customer harm | No noticeable effect on customers | Some customers inconvenienced; a workaround exists | Many customers delayed; complaints rise | Large numbers of customers cannot pay, get paid or reach their money | Widespread harm: salaries or bills unpaid, penalties, vulnerable customers or businesses affected |
| Market and financial system | No effect outside the bank | Counterparties notice delays | Other banks or a payment system affected locally | Settlement failures affect other institutions or a payment system | Risk of contagion; disruption to the UAE financial system |
| Financial loss (illustrative) | Below AED 1m | AED 1m to 5m | AED 5m to 25m | AED 25m to 100m | Above AED 100m, or loss of key clients |
| Regulatory and legal | No breach | Breach of an internal policy only | Regulatory reporting late or a notification needed | Breach of a regulatory or legal duty; supervisory action likely | Serious breach: sanctions, licence conditions or criminal liability at risk |
| Reputation | No external attention | Local social media comment | National media coverage for a day | Sustained national coverage; clients start to leave | International coverage; loss of trust; Board and regulator involved |
| Operational backlog | Absorbed in normal work | Backlog cleared within a day | Backlog needs overtime or extra staff | Backlog creates errors; manual workarounds cannot be sustained | Backlog cannot be recovered, or data is lost |

**Calibrate before you use it.** The financial thresholds are illustrative. Set them from your own risk appetite, for example as a share of annual net income, and use the same scale as your enterprise risk framework so that a "Major" here means the same as a "Major" in the risk register. The risk committee should approve the scale before any workshop.

## 3. Eight points in time

1 hour, 2 hours, 4 hours, 8 hours, 1 day, 3 days, 1 week, 1 month.

The clock starts when the service stops for clients, **not** when someone notices or invokes the plan. Detection, escalation and decision time all count.

## 4. Three rules

**Rule 1: take the maximum, never the average.** At each point in time, the service's impact is its highest score across the six categories. An average of five low scores and one Severe looks Moderate, and a client who cannot be paid does not care that the backlog is fine.

**Rule 2: Critical Operation.** A service is a Critical Operation if any category reaches **Major (4) within one business day**. This is Edition 4's test in numbers: *if this stopped for a day, would the Board need to know before the end of that day?* The threshold is a parameter; set your own and record why.

**Rule 3: draft tolerance for disruption.** The draft tolerance is **the last point in time before any category reaches Severe (5)**. If payments reach Severe at 8 hours, the draft tolerance is 4 hours. The Board approves the final tolerance; it may be tighter, never looser without a written reason.

Then the BIA has to fit inside it: every process recovery time (RTO), every third party's contractual recovery time and every tested recovery must be within the tolerance, with a margin.

## 5. Scoring discipline

- **Score the worst realistic moment.** Payroll day, month end, quarter end, Ramadan, a sales weekend. Score a peak as its own line if it changes the answer (Bank Horizon scores "Salary and payroll processing (payroll day)").
- **Impact never falls over time.** If a score drops between two points in time, the scorer is describing recovery, not impact. The workbook flags it.
- **Every 4 or 5 needs a sentence of evidence.** "Thousands of employees unpaid by evening" is evidence. "Very important" is not.
- **Score without the controls.** Score what happens if the service stops, before any workaround. Workarounds belong in the continuity plan, and they are tested, not assumed.
- **The business scores; risk challenges.** Process owners and business heads score in a workshop; the second line challenges every score that looks too low or too convenient.

## A worked example: trade finance at Bank Horizon

| Category | 1h | 2h | 4h | 8h | 1 day | 3 days | 1 week | 1 month |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Customer harm | 1 | 2 | 2 | 3 | **4** | **5** | 5 | 5 |
| Market and financial system | 1 | 1 | 1 | 1 | 2 | 3 | 4 | 4 |
| Financial loss | 1 | 1 | 1 | 2 | 3 | **5** | 5 | 5 |
| Regulatory and legal | 1 | 1 | 1 | 2 | 2 | 3 | 4 | 4 |
| Reputation | 1 | 1 | 1 | 2 | 3 | 4 | 5 | 5 |
| Operational backlog | 1 | 1 | 2 | 3 | 4 | 5 | 5 | 5 |
| **Highest** | 1 | 2 | 2 | 3 | **4** | **5** | 5 | 5 |

- First Major at **1 day**, so it is a Critical Operation.
- First Severe at **3 days**, so the draft tolerance is **1 day**.
- The old BIA said "medium, recover in 5 days", because five days is how long the platform takes to restore. The matrix says the clients cannot wait that long. **That gap is the finding.**
