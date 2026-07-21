# Product Execution Framework

Use this framework for questions about diagnosing product outcomes, choosing
what to do next, managing delivery, and learning from results. It is
level-agnostic: demonstrate sound judgment at the scope provided by the prompt.

## Start with the decision

Clarify what decision must be made and when.

- What changed, or what outcome is at risk?
- Is the task to diagnose, prioritize, launch, recover, or improve?
- Who is affected?
- What constraints are fixed?
- What would make the decision reversible or difficult to reverse?

Restate the objective before analyzing causes or solutions.

## Build a simple system view

Describe how value is created from start to finish. Depending on the prompt,
this might be a user journey, workflow, funnel, service, or set of dependencies.

- Where could the outcome break down?
- Which users, surfaces, regions, or use cases may behave differently?
- Did the change begin suddenly or gradually?
- What else changed at the same time?

This view prevents random guessing and helps locate the problem.

## Separate facts, assumptions, and unknowns

Create three mental buckets:

- Facts: information explicitly provided.
- Assumptions: working beliefs you are using to move forward.
- Unknowns: questions whose answers could change the decision.

Check data quality and definitions before drawing conclusions. Look for
selection effects, delayed signals, seasonality, instrumentation gaps, and
changes outside the product.

## Form hypotheses

Develop a small, structured set of plausible explanations. Useful categories
include:

- user or market change
- product or experience change
- technical quality or reliability
- policy, trust, or access
- distribution or awareness
- measurement or data quality

For each leading hypothesis, name:

- why it could explain the observed outcome
- what evidence would support or weaken it
- the fastest responsible way to learn more

Prioritize hypotheses by plausibility, potential impact, urgency, and ease of
learning. Do not investigate everything equally.

## Choose an action

Match the action to the evidence and cost of being wrong.

- Act now when harm is clear and delay is costly.
- Run a bounded test when uncertainty is high and the choice is reversible.
- Gather targeted evidence when major commitments depend on an unknown.
- Stop or roll back when guardrails are breached.

Explain what you will do, what you will defer, and what evidence would change
your mind.

## Plan delivery

Turn the decision into an executable path.

- Define the intended outcome and owner.
- Identify key partners and decision rights.
- Surface dependencies and the critical path.
- Name major user, business, technical, operational, and trust risks.
- Reduce scope without removing the core value.
- Establish checkpoints for decisions, not just status.
- Plan communication for affected people.

For disagreement, return to the shared objective, evidence, constraints, and
tradeoffs. Escalate a decision with clear options rather than only describing
the conflict.

## Evaluate and learn

Before acting, define:

- primary success signal
- guardrail signals
- expected direction of change
- review point
- continue, adjust, expand, or stop criteria

Afterward, compare the result with the original hypothesis. Separate outcome
quality from decision quality: a sound decision can have an unfavorable result,
and a weak decision can get lucky.

End with a concise summary of the objective, leading evidence, decision,
tradeoff, delivery risk, and learning plan.

## Sample prompts

- A core workflow is being completed less often. How would you diagnose the
  change and decide what to do?
- A team must choose between improving reliability and adding a requested
  capability. How would you prioritize?
- A launch depends on several teams and a key dependency is late. What would
  you do?
- Users adopt a new feature but do not return to it. How would you respond?
- Two partners disagree about whether the available evidence supports a wider
  release. How would you reach a decision?

## Self-check

- Did I clarify the decision and objective?
- Did I map the system before proposing causes?
- Did I separate facts, assumptions, and unknowns?
- Did I prioritize hypotheses and say how to test them?
- Did my action match the evidence and cost of being wrong?
- Did I cover owners, dependencies, risks, and communication?
- Did I define success, guardrails, and decision criteria?
- Did I make tradeoffs explicit and conclude with a clear recommendation?

## Notes-based coaching prompt

```text
Using only my human-authored practice notes, evaluate the execution logic I
actually wrote. Separate direct evidence from interpretation. Point out one
strong prioritization choice, one unsupported assumption, and one focused drill
for next time. Do not reconstruct missing parts of my answer.
```
