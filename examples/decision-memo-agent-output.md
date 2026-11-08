# Decision memo agent: example output

> Spec: [`workflows/decision-memo-agent.md`](../workflows/decision-memo-agent.md). Lumen is a fictional company; see [examples/README.md](README.md).

## What triggered it

The `#recs-migration` channel passed 20 messages on 4 March 2026 with no recorded decision (31 messages over 9 days, 6 participants). The agent checked the decision log, found no prior decision on the topic, and drafted the memo below. It was sent as a private message to the proposed owner, Dana Okafor, at 07:10 on 5 March. Nothing was posted in the channel.

The finished memo, after Dana and Priya Nair edited it, is in [`product-operating-system/examples/decision-memo-example.md`](https://github.com/utaknablein/product-operating-system/blob/main/examples/decision-memo-example.md). Comparing the two shows what the humans added: the recommendation, the owner, the date, and the guardrail numbers.

---

## The draft

**Draft decision memo from #recs-migration. Prepared by the decision memo agent. Not yet reviewed by a person.**

**Decision:** Do we retire the legacy recommendations service (Recs v1) and move all surfaces to Recs v2 before Q3?

**Why now:** Three facts in the thread set a deadline. Tomás Herrera wrote on 27 Feb that "the two v1 engineers move to Search in April unless we decide otherwise." Jon Adeyemi posted on 1 Mar that running both systems costs "about $38k a month in infra." Priya Nair wrote on 3 Mar that the Q3 Home redesign "cannot be planned while we have two ranking systems." If no decision is made by mid-March, v1 loses its engineers and becomes unowned while still running.

**Options proposed in the thread:**

| | Option | What it gets us (per the thread) | What it costs (per the thread) | What it rules out |
|---|---|---|---|---|
| A | Retire v1 by end of Q2; v2 on all surfaces | One system; $38k/month; two engineers freed (Tomás, 27 Feb) | "Four weeks of migration" (Tomás, 28 Feb); a cold-start gap for new subscribers that Mei Lin says is "bigger than we think" (2 Mar) | Running the planned Q3 A/B between v1 and v2 |
| B | Keep v1 for new subscribers only | Protects week-one engagement (Mei Lin, 2 Mar) | Both pipelines stay; v1 still needs an owner after April, and nobody in the thread volunteered | Freeing the engineers |
| C | Do nothing | Not proposed by anyone, included for completeness | $38k/month continues; v1 becomes unowned in April regardless (Tomás, 27 Feb) | The Q3 Home redesign, per Priya |

**Where people stand:**

- **Priya Nair (Product, Home):** for A. "We have been arguing about which row is right for a year." (3 Mar)
- **Tomás Herrera (Engineering, Discovery):** for A. "Six months ago I would have said B. The window has passed." (28 Feb)
- **Mei Lin (Data science):** against A as currently described. "v2 has only been measured on returning users. The cold-start gap is bigger than we think." (2 Mar) Has not stated support for B or C.
- **Jon Adeyemi (Finance):** position on options not stated. Supplied the cost figure and asked that "whatever we decide shows up against the migration cost in the Q2 review." (1 Mar)
- **Sam Whitfield (Design):** no position stated. Asked two questions about the Home layout (6 and 7 Mar), both unanswered.
- **Dana Okafor (VP Product):** no position stated in the thread. Tagged by Priya on 3 Mar: "Dana, we need you to call this."

**Open questions the thread assumed but did not establish:**

1. The size of the v2 cold-start gap on new subscribers. Mei Lin says it is large; no number was posted.
2. Whether the v1 engineers can be kept past April. Tomás states they cannot; nobody confirmed with the Search team.
3. Whether the $38k/month is the full cost of running both or infra only.

**What would change the answer (from the thread):** If the cold-start gap can be closed, Mei Lin's objection to A falls away (her message of 2 Mar: "if v2 can seed from onboarding I'd be fine"). If the engineers could be retained, Tomás's urgency falls away.

---

**Reported separately:**

1. **One decision or several?** One decision, with a dependent question underneath it (how to handle cold-start users). Sam Whitfield's layout questions are a separate decision and should not be in this memo.
2. **Door type:** One-way. Tomás, 27 Feb: "once the pipeline is off and the people are gone, bringing it back is a quarter of work."
3. **Natural owner:** Dana Okafor. Tagged by name, senior to all participants, and has not yet spoken.
4. **Prior decisions:** None found in the decision log on Recs v1, Recs v2 or recommendation systems. Entry #2 (transcript search, build vs. buy, January) is the closest and is unrelated.

*This draft contains no recommendation. All quotes link to the original messages. Positions not stated in the thread are marked as not stated.*

---

## What the owner changed

Dana Okafor accepted the draft with four edits before sharing it: she chose Option A and wrote the recommendation; set the decision date (14 March); turned Mei Lin's objection into a numeric guardrail (within 5% of v1 on week-one listens by 15 June) after a call with Mei; and removed Sam's layout questions into a separate thread. The memo was shared on 6 March and decided on 11 March. Logged as entry #4: six days.

Time from the trigger to a decision the team had been circling for nine days: one week.
