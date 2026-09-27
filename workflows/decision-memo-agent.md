# Decision Memo Agent

Watches for debates that have stalled, and turns them into a one-page decision memo with the decision stated, the options laid out, and a suggested owner and date.

| Trigger | Owner | Output | Checkpoint |
|---|---|---|---|
| A thread passes 20 messages or 7 days without a decision | Chief of staff or CPO | Draft decision memo | Proposed decision owner |

## Trigger

A tracked email or chat thread crosses 20 messages or 7 days, and nobody has written down what is being decided. Anyone can also trigger it by tagging the thread. Most slow decisions are unowned decisions, and this is the moment they start to stall.

## Inputs and tools

| Reads | From | Access |
|---|---|---|
| The full thread | Email or team chat | Read only |
| Related documents linked in the thread | Document store | Read only |
| Decision memo template | [`product-operating-system`](https://github.com/utaknablein/product-operating-system/blob/main/templates/decision-memo.md) | Read only |
| Past decisions on the same topic | Decision log | Read only |

## Permissions

| May do alone | Needs human approval | Must never do |
|---|---|---|
| Read the thread and linked documents | Share the memo with the thread's participants | Recommend an option |
| Draft the memo | Assign the owner and the decision date | Post in the thread or reply on anyone's behalf |
| Check the decision log for prior decisions | Add the entry to the decision log | Summarize a person's position without quoting them |

## Instructions

```
Turn this thread into a one-page decision memo:
- Decision: one sentence, phrased as a question with a clear answer
- Why now: what happens if no decision is made
- Options: every option seriously proposed, plus "do nothing", with what each
  gets, costs, and rules out
- Where people stand: each person's position in one line, quoting them
  where possible. Keep disagreement visible.
- Open questions: facts the thread assumed but never established
- What would change the answer: the one or two facts that would flip it

Then report separately:
1. Is this one decision or several tangled together?
2. One-way door (hard to reverse) or two-way door?
3. Who is the natural owner, based on the thread?
4. Has this decision, or one like it, been made before? Check the decision log.

Do not recommend an option. Use only what is in the thread and linked documents.
```

## Hand-off

The draft goes to the proposed owner, not to the whole thread. They correct it, assign themselves or someone else, set a date, and share it.

## Human checkpoint

The owner checks that every person's position is fair, that "do nothing" is included, and that the decision is really one decision. People will read this memo about themselves. An unfair summary damages trust more than a slow decision.

## Escalation

The agent stops and flags instead of drafting when:
- The thread involves personnel matters, legal disputes or anything confidential
- It finds the same decision in the log from the last 90 days (a remade decision is a signal worth a human's attention)
- It cannot identify any clear decision in the thread

## Metrics

| Metric | Target |
|---|---|
| Days from trigger to decision, versus stalled threads before the agent | Falling |
| Memos accepted by the owner without substantial rework | Above 80% |
| Remade decisions flagged that a person confirmed | Tracked |

## Where it goes wrong

- **It picks a side.** Summaries lean toward whoever wrote the most or the last. That is why it may not recommend, and why positions are quoted.
- **It smooths disagreement.** "The team broadly agrees" is often false, and hidden disagreement comes back later.
- **It misses that there are two decisions.** Many stuck threads are stuck because two decisions are tangled together. Question 1 exists to catch this.
