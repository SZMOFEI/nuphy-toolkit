# Clarification workflow

## 1. Select the mode

- **Guided mode**: default when the request is vague or has blocking gaps.
- **Fast draft mode**: use when the user asks for an immediate draft or already supplied enough context.
- **Gap review mode**: use when the user provides an existing requirement or PRD and asks what is missing.

## 2. Normalize what is known

Silently map the user's material to the input schema. Do not force the user to speak in field names. Summarize what is understood in two to five bullets and separate explicit facts from inferences.

## 3. Ask by information gain

Choose the next unanswered question that most changes scope or acceptance. Typical order, adjusted to context:

1. **Business trigger and goal** — Why now, and what outcome matters?
2. **Current problem and evidence** — What happens today, for whom, and what shows it is a problem?
3. **Expected observable result** — What should users or operators be able to see or do afterward?
4. **Scope boundary** — Which page, market, locale, device, channel, campaign, or process is affected? What is explicitly out of scope?
5. **Timing** — What date matters and what happens if it slips?
6. **Acceptance** — What observable checks prove the request is complete?
7. **Constraints and dependencies** — Brand, legal, SEO, inventory, localization, analytics, or coordination constraints.

Avoid asking for a technical solution, priority label, engineering estimate, or project plan. If a user volunteers one, preserve it as a non-binding suggestion.

## 4. Completion gate

A requirement is `可进入评审` when all six items below are usable:

- goal or business trigger;
- current problem;
- expected observable result;
- affected scope;
- at least two testable acceptance criteria;
- no unresolved contradiction that changes the request.

A target date is recommended but not mandatory. If absent, write `未提供`; do not invent urgency.

## 5. Drafting rules

- Use concise operational language, not product-management jargon.
- Write observable outcomes, not implementation prescriptions.
- Each acceptance criterion must be independently testable and start with a condition or expected result.
- Keep facts, open questions, assumptions, and suggestions in separate sections.
- Include non-goals when scope creep is plausible.
- If evidence is anecdotal, say so.
- If a link cannot be opened, preserve the URL and state that its contents were not verified.

## 6. Stop conditions

Stop questioning and draft when any of these is true:

- the completion gate is met;
- the user requests a draft now;
- six question turns have been used;
- the remaining gaps are non-blocking.

Never block a useful draft merely because optional metadata is missing.
