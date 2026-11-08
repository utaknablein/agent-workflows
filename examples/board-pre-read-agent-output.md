# Board pre-read agent: example output

> Spec: [`workflows/board-pre-read-agent.md`](../workflows/board-pre-read-agent.md). Lumen is a fictional company; see [examples/README.md](README.md).

## What triggered it

Fourteen days before Lumen's Q1 2026 board meeting (meeting 23 April, draft produced 9 April). The agent read the quarter's metrics from the finance warehouse and the product analytics store, the decision log, nine team updates, and the Q4 pre-read and minutes from the board portal. The draft went to the CEO (Alex Brandt) and nobody else. One item was escalated immediately rather than placed in the draft; it is marked below.

Numbers are invented. Every figure carries its source system, as the instructions require. Anything forward-looking is marked for CEO approval and was not included in the figures.

---

## The draft

**Draft pre-read for the 23 April board meeting. Prepared by the board pre-read agent. Not yet reviewed. CFO verification of every number pending.**

### 1. The quarter in two pages

**What happened**

Revenue was $27.1M against a plan of $28.4M, 4.6% below *(source: finance warehouse, closed books, 3 Apr)*. The miss is concentrated in new-subscriber acquisition: 71,200 new paying subscribers against a plan of 84,000 *(source: finance warehouse)*. Paid marketing spend was on plan; cost per new subscriber rose from $31 to $38 *(source: finance warehouse)*. Renewals were slightly ahead: 30-day renewal rate 83.1% against 82.0% plan *(source: product analytics store)*.

Gross margin improved to 68.2% from 66.9% *(source: finance warehouse)*, driven by the retirement of two of three analytics tools (decision log #10) and lower content licensing cost per listen.

**Why**

Team updates attribute the acquisition miss to two causes: the February price change for new subscribers (decision log #1, $89 to $99 annual) and weaker performance on one paid channel *(source: Growth team update, 28 Mar)*. The Growth update describes the price change as "the main driver." The finance data shows conversion on the pricing page fell from 4.1% to 3.4% after 27 January *(source: product analytics store)*, consistent with that view, but the channel decline began in mid-January, before the price change *(source: product analytics store, daily acquisition by channel)*. The two causes are not separated in any team update.

**What we are doing about it**

Per team updates: a pricing-page test with the $89 anchor restored for one segment began 24 March *(Growth update)*; the underperforming channel's budget was cut by 40% on 10 March *(Growth update)*. Neither has results yet.

**Decisions we need from the board**

Two, per the CEO's notes to the agent: approval of the Q2 hiring plan (eight roles, $1.9M annualized *source: People team update*), and a view on whether the annual price change should be reversed before the summer campaign. The second is a management decision; the agent has included it because the CEO asked for the board's view, not its approval.

### 2. Commitments check

From the Q4 pre-read and the 29 January minutes:

| Commitment | Status | Evidence |
|---|---|---|
| Consolidate three analytics tools to one by end of Q1 | **Delivered** | Decision log #10, decided 16 Mar; two tools switched off 28 Mar *(Engineering update)* |
| Launch Sleep Stories on both platforms by end of Q1 | **Missed** | Android only, launched 20 Feb; iOS not launched. Decision log #5 and #9 show the decision was made twice. No team update mentions the iOS date slipping; the Product update of 28 Mar lists Sleep Stories as "launched." |
| Reduce cost per new subscriber below $30 | **Missed** | $38 this quarter, up from $31 *(finance warehouse)*. Growth update does not reference the commitment. |
| Hire second data scientist for Discovery | **Delivered** | Decision log #3; start date 6 Apr *(People update)* |
| Present a retention cohort analysis to the board in Q1 | **Not found** | No team update, decision or document references it. Flagged for the CEO. |

> **Escalated to the CEO on 9 April, outside this draft:** the Sleep Stories iOS miss is not mentioned in any team update, and the Product update describes the feature as launched. Per the escalation rules, this went to the CEO directly.

### 3. Decisions this quarter

Ten decisions logged *(source: decision log)*. Median time from raised to decided: 9 days. Four were agent-assisted (median 7 days, none remade); six were prepared by people (median 16 days, one remade). The one remade decision is Sleep Stories (#5, remade as #9). Three decisions are one-way doors that the board may want to be aware of: retiring Recs v1 (#4), dropping Daily Mix (#7), and allowing the support agent to issue refunds under $20 without review (#8).

### 4. The ten hardest questions, ranked by discomfort

1. The price change cost us roughly 13,000 new subscribers against plan. Who owned that decision, what did we expect to happen, and why did it take two months to start a test?
2. Cost per new subscriber went from $31 to $38 while spend was on plan. What were we buying?
3. Sleep Stories was committed for both platforms. Why is iOS not launched, and why did the Product update call it launched?
4. The retention cohort analysis we asked for in January: where is it?
5. We decided the Sleep Stories launch twice. What stops that happening on a decision that matters more?
6. Renewal is ahead of plan while acquisition is behind. Are we becoming a smaller, more loyal business by accident?
7. The support agent can now refund up to $20 without a human. How many refunds has it issued, and who checks them? *(Agent note: no team update reports this number. The board will ask.)*
8. Gross margin is up partly because we licence less content per listen. Is that efficiency or a thinner product?
9. Eight new hires at $1.9M while revenue is 4.6% below plan. Which of these would you cut if Q2 misses too?
10. Four of ten decisions this quarter were drafted by an agent. Which ones, and how do we know they were good decisions rather than fast ones?

Questions 1, 3 and 4 are tied to specific past concerns of board members, per the January minutes (Marta Keller on pricing; David Osei on delivery commitments).

### 5. Inconsistencies between sources

| Item | Team update says | Source system says | Gap |
|---|---|---|---|
| New subscribers, Q1 | 73,500 *(Growth update, 28 Mar)* | 71,200 *(finance warehouse, closed 3 Apr)* | 2,300. Growth figure likely pre-refund. |
| Sleep Stories status | "Launched" *(Product update)* | Android only *(release log)* | Escalated, see above |
| 30-day renewal rate | 84% *(Product update)* | 83.1% *(product analytics store)* | Rounding, but the board pack should use one number |
| Refunds issued by support agent | Not reported | 1,140 refunds, $14,700 *(support platform)* | Not reported anywhere in team updates |

*Forward-looking statements requested by the CEO (Q2 revenue outlook, hiring impact) are not included. They require CEO approval per the agent's permissions and are listed in a separate note.*

---

## What happened at the checkpoint

The CFO corrected one number: the gross margin figure used a preliminary content-cost accrual; the final figure was 67.9%, not 68.2%. The CEO rewrote section 1 in her own voice, kept the commitments table unchanged, removed question 10 from the list sent to the board (and asked it internally instead), and added the retention cohort analysis to the agenda with an apology. Seven of the remaining nine predicted questions were asked in the meeting.
