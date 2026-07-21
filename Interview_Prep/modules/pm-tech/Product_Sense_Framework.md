# Product Sense Framework

Use this framework for product design, product improvement, and open-ended user
problem questions. It is a guide for making decisions, not a script. A strong
answer follows a clear thread from objective to user need to product choice.

## The decision path

### Clarify the objective

Restate the prompt and ask only questions that could change your direction.

- What outcome matters?
- Is this a new product, an improvement, or a response to a change?
- What constraints or context are given?
- What is in scope for this discussion?

If information is unavailable, state a reasonable assumption and continue.

### Choose a user and context

Identify plausible user groups, then select one based on the objective.

- Who experiences the problem?
- In what situation does it occur?
- How often or how intensely does it matter?
- Who is underserved by current options?

Explain why you chose this user. Avoid listing many segments without committing
to one.

### Understand the problem

Walk through the user's current journey. Look for friction, unmet needs, and
workarounds.

- What is the user trying to accomplish?
- What happens before, during, and after the key moment?
- Where do effort, uncertainty, delay, or risk appear?
- Which pain is important enough to solve now?

Turn the selected pain into a concise problem statement:

```text
[User] needs a better way to [goal] when [context] because [current barrier].
```

Distinguish known facts from assumptions that would need validation.

### Define success and guardrails

Name the change you want for the user and how you would recognize it.

- What user behavior or outcome should improve?
- What product or organizational outcome should follow?
- What guardrails protect trust, quality, access, safety, or sustainability?

Choose a small set of success signals that fit the objective. Explain what each
signal would reveal and where it could mislead.

### Explore approaches

Generate meaningfully different approaches before selecting one. Consider:

- reducing a painful step
- improving guidance or confidence
- changing the workflow
- connecting people or resources
- removing the need for the task

Do not present a feature list. Tie each approach to the selected problem.

### Prioritize with explicit tradeoffs

Compare approaches using the factors most relevant to the prompt, such as user
value, confidence, effort, risk, reach, or strategic fit.

State:

- what you would do first
- why it is better for the chosen objective and user
- what you are not doing yet
- what new evidence could change the decision

### Make the product concrete

Describe the smallest coherent experience that tests the central idea.

- entry point
- key user steps
- moment of value
- important edge cases
- trust and accessibility needs

Keep implementation detail proportional to the prompt. The goal is enough
specificity to expose product choices.

### Learn and iterate

Explain how you would reduce the biggest uncertainty before expanding.

- What must be true for the idea to work?
- Which assumption is most dangerous?
- What evidence would support, change, or stop the approach?
- What would you learn from user feedback and behavior?

End by summarizing the thread: objective, user, problem, chosen approach,
tradeoff, and learning plan.

## Sample prompts

- Design a better way for shift workers to hand off unfinished tasks.
- Improve the first-use experience for people learning a complex tool.
- Build a product that helps community volunteers coordinate their work.
- Improve how households decide what to repair, replace, or postpone.
- Design an accessible way to navigate an unfamiliar public space.

## Self-check

- Did I choose a clear objective instead of solving every possible objective?
- Did I select a user and explain why?
- Did I identify a need rather than jump directly to features?
- Did each proposed approach address that need?
- Did I make a choice and name its tradeoffs?
- Did I define success signals and guardrails?
- Did I expose assumptions and explain how I would learn?
- Did my conclusion connect the full decision path?

## Notes-based coaching prompt

```text
Use only my human-authored practice notes. Map the decisions I actually wrote
to this framework. Identify where the thread is clear, where evidence is
missing, and one drill that would improve my next attempt. Label interpretations
as interpretations and do not fill gaps with invented details.
```
