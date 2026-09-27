# Discovery Agent

Prepares customer-discovery interview guides from the riskiest assumptions, then synthesizes interview notes as they arrive, without letting the team hear what it wants to hear.

| Trigger | Owner | Output | Checkpoint |
|---|---|---|---|
| A risk list arrives, or interview notes are added | Product lead | Interview guide; rolling synthesis | Product lead, after every five interviews |

## Trigger

Two triggers:
1. **Guide:** a risk list arrives from the [market landscape agent](market-landscape-agent.md), or a product lead names the riskiest assumption.
2. **Synthesis:** new interview notes are added to the research repository.

People run the interviews. The agent never conducts them.

## Inputs and tools

| Reads | From | Access |
|---|---|---|
| The riskiest assumptions | Landscape brief or product lead | Read only |
| Raw interview notes | Research repository | Read only |

## Permissions

| May do alone | Needs human approval | Must never do |
|---|---|---|
| Draft interview guides | Change the guide between rounds | Contact interviewees |
| Update the rolling synthesis | Share synthesis beyond the product team | Quote anything not in the notes, word for word |
| Flag leading questions | | Identify interviewees outside the team |

## Instructions

**Guide**
```
Build a 30-minute discovery interview guide to test: [assumption].
- Start with a real story from their past, not our idea
- Ask what they did, not what they would do
- Introduce the concept only at the end, as a test
- Ask what would make them trust it and what it would be worth
- Ask whether the people who hold the knowledge would actually share it
- End with: "Is there another decision where this happened to you?"
  and "Who else should I talk to?"
Flag any question that leads the witness.
```

**Synthesis**
```
Update the synthesis with these new notes.
1. What people actually did, as opposed to what they said they would do.
2. Which assumptions held, broke, or remain untested, with the interview count
   behind each.
3. The three most surprising things said, quoted word for word from the notes.
4. Where interviews disagree. Do not smooth it over.
5. What to change in the guide for the next round.
Use only the notes. Label every inference.
```

## Hand-off

Guides go to the interviewer. The rolling synthesis goes to the product lead and feeds the decision to build, narrow or stop, recorded in the decision log.

## Human checkpoint

After every five interviews, the product lead checks each claimed pattern against the notes, confirms every quote is real, and marks any interview where the interviewer defended the concept. That interview's reaction to the concept does not count.

## Escalation

The agent flags when:
- A core assumption has broken in three or more interviews
- Notes suggest the interviewer is leading or defending the concept

## Metrics

| Metric | Target |
|---|---|
| Patterns claimed that the product lead could not confirm in the notes | Zero |
| Quotes that do not match the notes exactly | Zero |
| Days from last interview to a build, narrow or stop decision | Falling |

## Where it goes wrong, and what I learned

- **Invented patterns.** With five interviews, "a clear trend" is usually two people. Every claim needs a count.
- **Do not defend the concept.** When someone says "I would not use that, I would call three people I trust," the right response is "why those three?" That answer has taught me more than anyone telling me they love the idea.
- **"Who else should I talk to?"** is how ten interviews become forty without a recruiting budget.
- **A second story** ("yes, that happened to me again when...") is a stronger signal than any rating of the concept.
