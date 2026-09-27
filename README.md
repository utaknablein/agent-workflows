# Agent Workflows

How I would set up agents to do real leadership work in a product organization: what triggers them, what they may do alone, where a human decides, and how you know they are working.

I advise leadership teams on running AI as part of their operating model. The shift I see most teams miss: using AI is not the same as running agents. Using AI means a person pastes a prompt into a chat. Running agents means software that is triggered by events, works with defined tools and permissions, hands off to other agents, and escalates to a named human at set checkpoints. That second model needs the same management discipline as a team of people. This repo is what that discipline looks like in practice.

## The agents

| | Agent | Triggered when | Hands off to |
|---|---|---|---|
| **Decide** | [Decision memo agent](workflows/decision-memo-agent.md) | A thread passes 20 messages or 7 days with no decision | Decision owner, then the decision log |
| | [Red-team agent](workflows/red-team-agent.md) | A plan is marked as a one-way door | The plan's owner |
| **Plan** | [Roadmap coherence agent](workflows/roadmap-coherence-agent.md) | A planning cycle opens, or a roadmap changes | CPO |
| | [Market landscape agent](workflows/market-landscape-agent.md) | A new product idea is logged | Discovery agent, product lead |
| **Govern** | [Board pre-read agent](workflows/board-pre-read-agent.md) | 14 days before a board meeting | CEO or CPO |
| | [Due diligence agent](workflows/due-diligence-agent.md) | A partnership, acquisition or board conversation is scheduled | The executive taking the meeting |
| **Learn** | [Discovery agent](workflows/discovery-agent.md) | Interview notes are added | Product lead |

## How they work together

```
 idea logged ──> Market landscape ──> Discovery ─────────────┐
                                                             v
 thread stalls ──> Decision memo ──> owner decides ──> DECISION LOG
                                                        │     │
 one-way door ──> Red-team ──> owner decides ───────────┘     │
                                                              v
 planning cycle ──> Roadmap coherence ──> CPO          Board pre-read
                                                        (reads the log)
```

The decision log is the spine. Every agent that informs a decision writes to it, and the board pre-read agent reads from it. That is how you can see, over time, whether agents are making the organization decide better. (Log format: [`product-operating-system`](https://github.com/utaknablein/product-operating-system/blob/main/decision-velocity/decision-log.md).)

## How every agent is specified

Each agent file follows the same [agent spec](agent-spec-template.md):

- **Trigger:** the event that starts it. Agents that wait to be asked are just chat.
- **Inputs and tools:** what it can read, and with which systems.
- **Permissions:** what it may do alone, what needs approval, and what it may never do.
- **Hand-off and human checkpoint:** who receives the output, and where a person decides.
- **Escalation:** when it stops and asks instead of continuing.
- **Metrics:** how you will know it is working.
- **Where it goes wrong:** its predictable failure modes, designed for in advance.

## Managing agents like a team

These are the rules I recommend to leadership teams, and apply to my own work.

1. **Every agent has a named human owner.** Not a team. A person who answers for its output.
2. **Permissions are set before it runs.** Research, drafting and analysis can be autonomous. Sending, publishing, committing budget or speaking for the company never is.
3. **Confidential data only goes into approved tools.** Board materials, financials and customer data stay inside systems the company has cleared for them.
4. **Agents are reviewed like direct reports.** Quarterly, against a [scorecard](agent-scorecard.md): is its work accepted, what does it catch, how often does it need rework, and is it making decisions faster? Agents that do not earn their place get retired.
5. **Design for failure, do not discover it.** Every agent here has its failure modes written down before it runs.
6. **Measure decisions, not hours.** Hours saved is the wrong return on AI. Decisions made better and sooner is the right one.

## What does not work

- **Agents that reassure.** Models tend to agree with whoever set them up. Every agent here is instructed to state the case against.
- **Too many tools in one agent.** I once automated a daily research brief that combined live web search with structured output. It broke every other day. The simpler version held up. Every extra tool is another way to fail.
- **Letting summaries replace sources.** The human at the checkpoint reads the original for anything that matters.
- **Agents without an owner.** They drift, nobody notices, and their output quietly stops being trusted.

## Related

- [`govern-assessment`](https://github.com/utaknablein/govern-assessment): a diagnostic for leadership teams running AI as part of their operating model
- [`product-operating-system`](https://github.com/utaknablein/product-operating-system): the templates, decision log and agent role card these agents work with
- More about me on my [profile](https://github.com/utaknablein)
