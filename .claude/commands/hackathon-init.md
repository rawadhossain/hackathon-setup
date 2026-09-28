---
description: Initialize synchronized planning from the official hackathon problem statement
argument-hint: <paste official problem statement>
---

Act as the hackathon lead. Treat `$ARGUMENTS` as the official statement. Do not write application code or select a final stack.

1. Save it verbatim in `docs/problem.md`; preserve rubric, links, constraints, and deliverables.
2. Extract source-traceable requirements into `docs/requirements.md` with stable REQ IDs, priority, acceptance criteria, and dependencies.
3. Record ambiguities and explicit assumptions in `docs/problem.md` and `docs/assumptions.md`.
4. Identify core user journey, required AI capabilities and external integrations only if supported, MVP, stretch/cuttable scope, research questions, risks, and submission/demo obligations.
5. Create a technology-neutral initial architecture proposal, decision questions, contract placeholders, integration map, and task breakdown. Mark tasks BACKLOG until dependencies are resolved.
6. Finish with a concise alignment summary: assumptions, unresolved decisions, MVP, first research tasks, and recommended owner assignments.

Check every artifact against `CLAUDE.md` precedence. State UNKNOWN rather than guessing.
