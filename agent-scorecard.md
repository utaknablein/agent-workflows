# Agent Scorecard

> Agents are reviewed like direct reports: quarterly, by their named owner, against the same five questions. An agent that cannot show its value gets fixed or retired. Nobody keeps a direct report because they are busy.

## The five questions

| # | Question | Metric | How to measure |
|---|---|---|---|
| 1 | **Is its work used?** | Acceptance rate | Share of outputs the human at the checkpoint accepts without substantial rework |
| 2 | **Does it catch what we would miss?** | Catch rate | Issues, risks or conflicts it flagged that a person confirmed were real and had not already seen |
| 3 | **Is it getting things wrong?** | Error rate | Outputs with a factual error, invented source or misquote found at the checkpoint |
| 4 | **Does it know its limits?** | Escalation quality | Share of escalations that were justified, and any case where it should have escalated but did not |
| 5 | **Are decisions better or faster?** | Decision latency and rework | For decisions it informed: days from raised to decided, and how often they were remade, compared with decisions it did not inform |

Question 5 is the one that matters most. The first four tell you whether the agent is reliable. The fifth tells you whether it is worth having.

## Quarterly review

| Agent | Owner | Acceptance | Catch | Errors | Escalation | Decision impact | Verdict |
|---|---|---|---|---|---|---|---|
| Decision memo | | | | | | | ☐ Keep ☐ Fix ☐ Retire |
| Red-team | | | | | | | ☐ Keep ☐ Fix ☐ Retire |
| Roadmap coherence | | | | | | | ☐ Keep ☐ Fix ☐ Retire |
| Market landscape | | | | | | | ☐ Keep ☐ Fix ☐ Retire |
| Board pre-read | | | | | | | ☐ Keep ☐ Fix ☐ Retire |
| Due diligence | | | | | | | ☐ Keep ☐ Fix ☐ Retire |
| Discovery | | | | | | | ☐ Keep ☐ Fix ☐ Retire |

## Reading the scorecard

- **High acceptance, low catch rate:** the agent is doing work people would have done anyway. Useful, but check whether it is worth its cost.
- **Low acceptance:** the instructions, inputs or trigger are wrong. Fix one at a time, and log the change.
- **Any invented source or misquote:** treat as serious. Tighten the instructions and increase checkpoint scrutiny until it is clean for a full quarter.
- **No escalations at all:** suspicious. Either the agent's work is trivial, or it is continuing when it should stop.
- **No measurable effect on decisions after two quarters:** retire it, or narrow it to the part that does help.

## What not to do

- **Do not count activity.** Number of runs, pages produced and hours saved are not on this scorecard on purpose.
- **Do not let the agent grade itself.** Every metric comes from the human checkpoint or the decision log.
- **Do not review agents less rigorously than people.** They make mistakes at scale, and faster.
