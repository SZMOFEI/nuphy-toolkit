# NuPhy Toolkit product specification

## Product model

NuPhy Toolkit is a shared plugin container for focused NuPhy workflows. Each capability must remain an independently triggered and testable Skill. The plugin grows only when a repeated, real workflow has been validated; it does not attempt to copy ECC's full catalog.

The first capability is requirement clarification.

## Problem

NuPhy operations requests often begin as short, solution-shaped messages. PM and engineering must reconstruct the business trigger, current problem, scope, and acceptance criteria before work can be evaluated. That reconstruction is the bottleneck.

## First-principles outcome

The plugin succeeds when it converts an ambiguous request into evidence that another person can review without guessing:

- why the request exists;
- what is wrong today;
- what observable outcome is wanted;
- where the change applies;
- how completion will be verified;
- which facts are missing or assumed.

## MVP functions

1. Guided clarification with one high-information question at a time.
2. Existing-requirement gap review.
3. Fast draft when the user asks to skip the interview.
4. Copy-ready Feishu requirement entry.
5. Lightweight PRD draft.
6. Explicit separation of facts, gaps, and assumptions.
7. Chinese by default, with language switching on request.

## Non-goals

- No code generation or repository access.
- No automatic Feishu read/write.
- No task creation or team notification.
- No final priority or engineering complexity decision.
- No custom UI, analytics, account system, or external data retention.

## Success measures for the pilot

- At least 80% of pilot outputs can enter PM review without being returned for missing goal, scope, or acceptance criteria.
- Median clarification stays at six question turns or fewer.
- Operators report that copy-pasting to Feishu takes less than two minutes.
- Zero instances of fabricated dates, metrics, links, or stakeholder decisions in the reviewed sample.

Measure these manually over the first 10–20 real NuPhy requests before building Feishu automation.
