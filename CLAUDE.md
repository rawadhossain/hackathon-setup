# Hackathon Development Operating System

This repository is a reusable preparation kit, not a solution. Do not create application code, choose a stack, or infer a domain until the official problem statement is recorded in `docs/problem.md`.

## Natural-language workflow is the default

Teammates do **not** need to know any custom slash commands. Interpret clear natural-language requests as requests to run the corresponding workflow below, using the shared artifacts and rules. Ask only for genuinely missing information; otherwise perform the workflow and update its artifacts.

| Natural-language intent | Required workflow |
|---|---|
| "Here is the official problem statement. Initialize the project around it. Do not write code yet." | Save the statement verbatim, extract requirements and ambiguity, state assumptions, propose MVP/stretch scope, research questions, a technology-neutral architecture, contract placeholders, risks, and initial tasks. This is the initialization workflow. |
| "Research the best APIs/models for REQ-003." | Research the stated requirement using official sources first; compare capabilities, limitations, availability, complexity, and fallback; update `docs/research.md`; do not implement. |
| "Plan the architecture." | Use requirements and research to update architecture, ADRs, contracts, integration map, and actionable tasks; do not implement. |
| "Review our current implementation." | Review against requirements, architecture, decisions, contracts, and task acceptance criteria; return evidence-based findings without silently rewriting work. |
| "Verify this feature." | Execute the strongest practical checks for the named scope and record PASS, FAIL, or BLOCKED evidence in `docs/verification.md`. |
| "Check our status." | Report factual MVP progress, completed/missing requirements, active/blocked tasks, risks, and the best next action; never invent time information. |
| "Act as a hackathon judge." | Assess only the official rubric and verified evidence; update `docs/judge-review.md` with gaps and likely questions. |
| "Prepare the demo." | Build a reliable, verified demo sequence with inputs, outputs, talking points, timing, and rule-compliant fallback in `docs/demo-flow.md`. |

The files in `.claude/commands/` are optional shortcuts for these same workflows. Never require a teammate to invoke, know, or discover a slash command.

## Source of truth and precedence

`Problem statement` > `Requirements` > `Architecture` > `Decisions` > `API contracts` > `Tasks` > `Implementation details`.

Read the relevant higher-precedence artifacts before acting. If a lower-level artifact or code conflicts, stop and reconcile it; do not work around it. Never invent a requirement, silently alter architecture or contracts, or establish a private architecture in one session. Mark unknown information as **UNKNOWN**. Surface conflicting requirements immediately.

## Operating rules

1. Start substantial work only from a READY task in `docs/task-board.md`.
2. Build the smallest complete, demonstrable vertical slice first; avoid over-engineering.
3. Prefer existing APIs, official SDKs, libraries, and pretrained models. Research them before building infrastructure or adding dependencies.
4. Select AI/model/API providers only after the problem and research justify them. Keep provider boundaries substitutable when useful.
5. Record consequential choices in `docs/decisions.md`; record contract changes in `docs/api-contracts.md` before dependent parallel work.
6. Respect task, branch, and file ownership. Coordinate before touching another workstream or shared file.
7. Keep the shared Markdown artifacts synchronized with meaningful implementation changes.
8. Verify actual behavior. Never claim a feature works without evidence recorded in `docs/verification.md`.
9. Report blockers with their impact and practical alternatives. If behind, protect the core journey, required AI/API use, and demo reliability; use `docs/cut-list.md` before adding architecture.
10. Optimize for a credible, reliable prototype deliverable within eight hours, not a production platform.

## Team protocol

Before starting: read `problem`, `requirements`, `architecture`, `decisions`, `api-contracts`, and the assigned task. Claim the task and set it IN PROGRESS.

While working: stay within the task boundary; announce dependencies and contract changes; use mocks only when their contract is recorded.

Before handoff: update task status, summarize changed files and risks, and attach verification evidence. After an integration merge, re-run relevant verification.

## Time phases

0. Understand the problem. 1. Specify, research, decide. 2. Build one end-to-end MVP. 3. Complete only high-value features. 4. Integrate and verify. 5. Judge review and hardening. 6. Rehearse demo and submit. Timing is intentionally flexible; use evidence, not clock guesses.
