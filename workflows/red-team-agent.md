# Red-Team Agent

Makes the strongest honest case against a plan before it is committed: a pre-mortem, the unchecked assumptions, and what a competitor would do next.

| Trigger | Owner | Output | Checkpoint |
|---|---|---|---|
| A plan is marked as a one-way door | Head of strategy or CPO | Red-team brief | The plan's owner, before approval |

## Trigger

Any plan marked as a one-way door (hard to reverse) before it goes for approval: a strategy for the board, a major launch, a pricing change, a public framework, a large investment. Runs automatically so that challenging a plan is not a political act someone has to choose to perform.

## Inputs and tools

| Reads | From | Access |
|---|---|---|
| The plan document | Document store | Read only |
| The numbers the plan depends on | Finance or analytics | Read only |
| Public sources on the market and competitors | Web search | Read only |
| Past decisions on related topics | Decision log | Read only |

## Permissions

| May do alone | Needs human approval | Must never do |
|---|---|---|
| Read the plan and its data | Share the brief beyond the plan's owner | Block or delay the plan |
| Research competitors and prior art | Add risks to the risk register | Soften findings to be diplomatic |
| Draft the red-team brief | | Present inferences as facts |

## Instructions

```
Critique this plan honestly. Do not reassure.

1. Pre-mortem: it is 18 months from now and this failed. The three most likely
   reasons, as specific to this plan as possible.
2. The strongest case for not doing this at all.
3. Every assumption the plan makes. Mark the ones that would sink it if wrong,
   and say which could be tested within 30 days.
4. Is the core idea new, or a familiar idea in new vocabulary? Name the closest
   existing examples, with sources.
5. What a competitor would do the day after we announce this.
6. What is genuinely strong in the plan and worth protecting.

Cite a source for every external claim. Label every inference.
```

## Hand-off

The brief goes to the plan's owner before the approval meeting, with enough time to respond. The owner decides what to change and attaches the brief, and their response, to the approval materials.

## Human checkpoint

The owner checks that step 2 genuinely argues against the plan, opens every source, and turns the top two testable assumptions into owners and dates before the plan moves forward.

## Escalation

The agent flags to the owner's manager, not just the owner, when:
- An assumption that would sink the plan has no evidence at all behind it
- The plan contradicts a decision already recorded in the decision log

## Metrics

| Metric | Target |
|---|---|
| Risks flagged that the owner confirmed were real and new | At least one per brief |
| Plans changed as a result of the brief | Tracked |
| Post-launch problems the brief had predicted, versus missed | Reviewed after 6 and 18 months |

The last metric is the real test. Keep every brief, and check it against what actually happened.

## Where it goes wrong

- **Soft critique.** Without an explicit instruction to argue against, models reassure. If step 2 is weak, the instructions need tightening.
- **Generic risks.** "Execution risk" is true of every plan. Only risks specific to this one count.
- **Confusing vocabulary with ideas.** A crowded term does not make the claim underneath it unoriginal, and a fresh term does not make an old idea new. Step 4 separates the two. This distinction changed how I position my own frameworks: cite the established problem, then state the specific contribution.
