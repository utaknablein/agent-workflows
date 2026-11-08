# Agent scorecard: Lumen, Q1 2026

> Worked example for [`agent-scorecard.md`](../agent-scorecard.md). Lumen is a fictional company; see [examples/README.md](README.md). Two agents were live this quarter. The others were not deployed, and the scorecard says so rather than leaving blank rows.

## Quarterly review

| Agent | Owner | Acceptance | Catch | Errors | Escalation | Decision impact | Verdict |
|---|---|---|---|---|---|---|---|
| Decision memo | D. Okafor | 9 of 11 drafts accepted with minor edits (82%) | 2 prior decisions found in the log that the thread had forgotten; 1 "two decisions tangled" flag confirmed | 1 misattributed quote (January), fixed by requiring message links | 3 escalations, all justified (1 personnel thread, 1 remade decision, 1 thread with no decision in it); 0 missed | Agent-assisted decisions: median 7 days, 0 remade. Others: median 16 days, 1 remade. Small sample (4 vs 6). | ☒ Keep ☐ Fix ☐ Retire |
| Board pre-read | A. Brandt (CEO) | 1 of 1 draft used; section 1 rewritten by the CEO, sections 2 to 5 kept | 1 missed commitment not in any team update (Sleep Stories iOS); 1 unreported metric (agent refunds); 1 commitment with no trace (cohort analysis) | 1 number corrected by CFO (gross margin, preliminary accrual) | 1 escalation (the unreported miss), justified | 7 of 9 predicted questions asked by the board (78%). Decisions requested of the board: 2, both taken in the meeting. | ☐ Keep ☒ Fix ☐ Retire |
| Red-team | | Not deployed | | | | | |
| Roadmap coherence | | Not deployed; planned for the Q2 planning cycle | | | | | |
| Market landscape | | Not deployed | | | | | |
| Due diligence | | Not deployed | | | | | |
| Discovery | | Not deployed | | | | | |

## Why "Fix" for the board pre-read agent

The output was good and the catch rate was the highest of any agent. The verdict is Fix, not Keep, for one reason: the corrected gross margin number. The agent read a preliminary accrual as final because the finance warehouse does not label accrual status in the table it read. One wrong number in a board pack is one too many, and the CFO catching it is the checkpoint doing its job, not the agent doing its job.

The fix is in the inputs, not the instructions: the agent now reads only from the closed-books view, which is published after the CFO's close. It will be reviewed again after the Q2 meeting. If the error rate is zero for one quarter, the verdict becomes Keep.

## Reading this quarter

- **Decision memo agent, high acceptance and real catches.** The two forgotten prior decisions are exactly what the agent exists to find. The misattributed quote in January was serious and was treated as such: instructions changed, logged, no repeat since.
- **The decision impact number is encouraging and not yet evidence.** Four agent-assisted decisions in one quarter is an anecdote. The comparison is also biased: the agent only fires on threads that have already stalled, so it selects for decisions that were about to get attention. Two more quarters before this number goes anywhere near a board.
- **No agent was reviewed less rigorously than a person would be.** Both reviews were done by the named owner, with the checkpoint data, in the same week as the team's quarterly reviews.
- **What was not measured:** runs, pages, hours. On purpose.

## Decisions from this review

1. Decision memo agent: keep, extend the trigger from one team's channels to all product channels in Q2.
2. Board pre-read agent: fix the input to closed books only; re-review after the Q2 meeting.
3. Deploy the roadmap coherence agent for the Q2 planning cycle, with D. Okafor as owner. One new agent per quarter, not three.
