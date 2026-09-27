# Agent Spec Template

> Fill this in before an agent runs for the first time. If you cannot fill in a section, the agent is not ready.

---

**Agent:** *Name*
**Purpose:** *One sentence: what decision or piece of work does it make better?*
**Owner:** *One named person who answers for its output*
**Status:** ☐ Pilot  ☐ Live  ☐ Under review  ☐ Retired

---

## Trigger

*The event that starts it. Be specific: "a thread passes 20 messages", not "when needed".*

## Inputs and tools

| Reads | From | Access |
|---|---|---|
| | | *Read only / Read and write* |

## Permissions

| May do alone | Needs human approval | Must never do |
|---|---|---|
| | | |

> The "never" column is the most important one. Write it first.

## Instructions

*The instructions the agent runs with. Keep them in version control and change them deliberately, like code.*

## Hand-off

*Who or what receives the output, and in what form.*

## Human checkpoint

*Where exactly a person reviews, decides or signs off. What they must check.*

## Escalation

*When the agent stops and asks a human instead of continuing. List the conditions.*

## Metrics

| Metric | Target | Reviewed |
|---|---|---|
| | | *Quarterly, on the [scorecard](agent-scorecard.md)* |

## Where it goes wrong

*Its predictable failure modes, and what is in place to catch each one.*

---

**Change log**

| Date | Change | Why | Approved by |
|---|---|---|---|
| | | | |
