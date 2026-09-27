# Due Diligence Agent

Prepares a briefing on a company before a partnership, acquisition, advisory or board conversation: strategy, product, leadership, risks, and the questions worth asking.

| Trigger | Owner | Output | Checkpoint |
|---|---|---|---|
| A meeting with an external company is scheduled with a tagged purpose | The executive taking the meeting | Company briefing | That executive, before the meeting |

## Trigger

A calendar event with an external company, tagged as partnership, acquisition, advisory or board. Runs five working days before the meeting, and refreshes the day before for anything new.

## Inputs and tools

| Reads | From | Access |
|---|---|---|
| Filings, earnings calls, press releases | Public sources, web search | Read only |
| Product announcements and release notes | Company website, web search | Read only |
| Leadership team and recent changes | Company website, news | Read only |
| Prior contact with this company | CRM and meeting notes | Read only |

## Permissions

| May do alone | Needs human approval | Must never do |
|---|---|---|
| Research public sources | Share the briefing beyond the meeting attendees | Contact the company or anyone at it |
| Read internal notes on prior contact | Store the briefing in shared systems | Research individuals beyond professional roles and public statements |
| Draft the briefing and questions | | Present undated information as current |

## Instructions

```
Brief me for a [purpose] conversation with [company] on [date], with [attendees].

1. The business: what they sell, to whom, how they make money, and how that is changing.
2. Strategy: what they say it is (quote their own words), what their actions
   suggest it actually is, and any gap between the two.
3. Product: what they shipped in the last 18 months, and what it signals.
4. Leadership: who runs the company, tenure, and recent changes.
5. Risks: financial, competitive, regulatory, and anything in the news.
6. AI: what they claim, and what evidence exists.
7. The ten best questions to ask, ranked by how much the answer would reveal.
   Focus where the public record is silent or contradictory.

Every factual claim needs a source and a date. Flag anything older than 12 months.
On refresh, report only what is new since the first briefing.
```

## Hand-off

The briefing goes to the executive taking the meeting, and to the other internal attendees if approved.

## Human checkpoint

The executive checks dates and opens the key sources, especially anything about people. They cut any question the company's own website answers. The best questions are the ones only a conversation can answer.

## Escalation

The agent flags to the executive immediately when it finds:
- Active litigation, a regulatory action or a major leadership departure in the last 90 days
- A conflict of interest with an existing partner, client or investment

## Metrics

| Metric | Target |
|---|---|
| Briefing facts found to be out of date at checkpoint | Falling to zero |
| Questions used in the meeting | Tracked |
| Material facts learned in the meeting that were public but missed | Zero |

## Where it goes wrong

- **Stale facts presented as current.** An executive who left last month, a strategy from two years ago. That is why every claim carries a date.
- **Repeating the company's own story.** Step 2 separates what they say from what they do. That gap is usually the most useful finding.
- **Drifting into dossiers on people.** The briefing is about the business. Professional roles and public statements only.
