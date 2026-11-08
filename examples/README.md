# Example outputs

What actually lands in a person's inbox when these agents run. Each example follows its agent's instructions literally, including the things the agent is not allowed to do, so you can judge the output before you deploy anything.

The company is **Lumen**, an invented subscription audio-learning app that also appears in the worked examples of [`product-operating-system`](https://github.com/utaknablein/product-operating-system/tree/main/examples). Nothing here describes a real company, person or dataset.

| Example | Agent | What to look for |
|---|---|---|
| [Decision memo agent output](decision-memo-agent-output.md) | [spec](../workflows/decision-memo-agent.md) | A stalled 31-message thread turned into a draft memo. Notice what the agent refuses to do: it quotes positions, lays out options, and stops short of recommending one |
| [Board pre-read agent output](board-pre-read-agent-output.md) | [spec](../workflows/board-pre-read-agent.md) | Misses first, every number with its source, a commitments check that names what was not delivered, and ten questions tied to this quarter's figures |
| [Scorecard, filled in](scorecard-filled.md) | [scorecard](../agent-scorecard.md) | One quarter of reviews for two live agents, with a Fix verdict and the reasoning behind it |

## Which agent to start with

The decision memo agent. It needs only read access to a chat tool and a template, it fires rarely (a handful of times a month in most organizations), and its output is reviewed by one person before anyone else sees it. If it is not useful after a quarter, you have lost very little. If it is, you have a decision log, and every other agent here reads from that log.

A one-week setup looks like this:

1. **Day 1:** Agree the trigger thresholds (20 messages or 7 days is a starting point; some teams use 15 and 5). Name the owner.
2. **Day 2:** Write the "must never do" column for your organization. Add anything specific: channels it may not read, people it may not quote.
3. **Day 3:** Run it manually on three past stalled threads. Read the drafts with the people who were in those threads. This is where you find the misquotes.
4. **Day 4:** Fix the instructions. Log the change.
5. **Day 5:** Switch the trigger on for one team's channels. Not the whole company.

Review on the [scorecard](../agent-scorecard.md) after a quarter. Then decide whether a second agent earns its place.
