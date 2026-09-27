# Board Pre-Read Agent

Drafts the board or leadership pre-read from the numbers, the decision log and team updates, checks last quarter's commitments, and predicts the hardest questions.

| Trigger | Owner | Output | Checkpoint |
|---|---|---|---|
| 14 days before a board meeting or quarterly review | CEO (or CPO for a product review) | Draft pre-read and question list | CEO, then CFO for every number |

## Trigger

Fourteen days before each board meeting or quarterly business review. The lead time matters: it leaves room to act on an uncomfortable finding, not just to word it carefully.

## Inputs and tools

| Reads | From | Access |
|---|---|---|
| Quarter's metrics against plan | Finance and analytics systems | Read only |
| Decisions made this quarter | Decision log | Read only |
| Team updates | Document store | Read only |
| Last quarter's pre-read and board minutes | Board portal | Read only |

Board material only runs in tools the company has approved for it. This is non-negotiable.

## Permissions

| May do alone | Needs human approval | Must never do |
|---|---|---|
| Read the inputs above | Share the draft with anyone besides the CEO and CFO | Send anything to board members |
| Draft the pre-read and question list | Include any forward-looking number | Change or restate a financial figure |
| Flag inconsistencies between sources | | Omit a missed commitment |

## Instructions

```
Draft the board pre-read for [meeting].

1. Two pages: what happened, why, what we are doing about it, and the decisions
   we need from the board. Lead with the misses, not the wins.
2. Commitments check: for every commitment in last quarter's pre-read and minutes,
   did we deliver? State plainly anything missed.
3. Decisions: summarize the major decisions from the decision log this quarter,
   including how long they took.
4. The ten hardest questions the board is likely to ask, based on the numbers
   and each member's past concerns. Rank by how uncomfortable they are.
5. Every number that is inconsistent between finance data and team updates.

Do not soften misses. Every number must cite its source system.
```

## Hand-off

The draft goes to the CEO, who writes the narrative. The CFO verifies every number against the source. Only then does it go to the board, from the CEO.

## Human checkpoint

- **CFO:** every number, against the system of record.
- **CEO:** the commitments check, and the story. The agent drafts. The CEO decides what the quarter means and signs it.

## Escalation

The agent flags to the CEO immediately, not in the draft, when:
- A commitment made to the board was missed and is not mentioned in any team update
- Finance and team numbers disagree by more than an agreed threshold

## Metrics

| Metric | Target |
|---|---|
| Numbers corrected by the CFO at checkpoint | Falling to zero |
| Board questions that were on the predicted list | Above 70% |
| Missed commitments surfaced by the agent before the board noticed | Tracked, and all of them |

## Where it goes wrong

- **It spins.** Drafts tend to lead with wins and bury misses. Boards notice. "Lead with the misses" is in the instructions for a reason.
- **Definitions differ.** Team updates often define metrics differently from finance. The consistency check catches some; the CFO catches the rest.
- **Generic questions.** "What is your AI strategy?" is always on the list. The useful questions are tied to this quarter's specific numbers.
