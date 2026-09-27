# Market Landscape Agent

Maps who already solves a problem, where the real gap is, and why that gap might stay empty, before anyone spends time building.

| Trigger | Owner | Output | Checkpoint |
|---|---|---|---|
| A new product idea is logged | Product lead for the idea | Landscape brief and risk list | Product lead, before discovery starts |

## Trigger

A new idea is logged in the product intake, and again before any investment pitch. It runs before discovery interviews, so the interviews test the right risks.

## Inputs and tools

| Reads | From | Access |
|---|---|---|
| The idea, written from the customer's side | Product intake | Read only |
| Existing research and customer data | Research repository | Read only |
| Public sources on competitors, pricing, substitutes | Web search | Read only |

## Permissions

| May do alone | Needs human approval | Must never do |
|---|---|---|
| Research public sources | Share the brief beyond the product team | Contact competitors or their customers |
| Draft the landscape and risk list | Pass the risk list to the discovery agent | Present inferences as findings |
| Refresh pricing and examples | | Recommend building or not building |

## Instructions

```
Map the landscape for this problem, from the customer's point of view.

1. Every category of existing solution, including indirect ones, manual
   workarounds and "do nothing". How do people solve this today?
2. For each category: real examples, what they charge, what they do well.
3. Where is the gap? Be specific about what nobody does, and why.
4. Argue against the gap: the structural reasons it may stay empty
   (supply, frequency, trust, free substitutes, anything else).
5. If the gap is real, the narrowest starting point that would prove it.

Cite sources with dates. Label every inference.
```

## Hand-off

The brief goes to the product lead. With approval, the list of reasons the gap might stay empty goes to the [discovery agent](discovery-agent.md) as the risks to test in interviews.

## Human checkpoint

The product lead checks that the brief covers how people solve this without a product, opens the pricing sources, and confirms step 4 is substantial. A landscape with a gap and no reasons it might stay empty is a sales pitch, not research.

## Escalation

The agent flags when:
- It finds a direct competitor already doing the idea as described
- It cannot find enough public information to say anything reliable

## Metrics

| Metric | Target |
|---|---|
| Risks from step 4 later confirmed in discovery | Tracked |
| Competitors or substitutes found later that the brief missed | Zero |
| Ideas stopped or narrowed before build, based on the brief | Tracked |

The third metric is a success, not a failure. An idea stopped early is the cheapest decision a product org can make.

## Where it goes wrong, and what I learned

- **The gap is rarely the most valuable output.** The list of reasons the gap is empty is. It becomes the risk register and shapes the interview questions.
- **Broad ideas test badly.** "Narrow it to one specific, high-frequency decision" has been the recommendation more than once, and it is usually right.
- **Solution framing skews the research.** Framing the problem from the customer's side, not the solution's, changes what it finds.
